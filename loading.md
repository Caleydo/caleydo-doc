Loading Data
============

Dataset Principles
-------------------
A dataset in Caleydo is (in most cases) based on tabular data in matrix form. However, Caleydo never shows only a dataset, but always shows *perspectives* on a dataset. Perspectives are used for columns and rows of datasets separately, but you always need both, a perspective of rows and columns.

A perspectives contains rules on how to access a dataset. Specifically a perspective defines:

 * The **order** of the elements (e.g., different perspectives on one dataset can contain different sortings)
 * The **containment** of elements (e.g., a perspective can be filtered to contain only a subset of the data)
 * A **grouping** of elements, i.e., it's *stratification* (e.g., a clustering algorithm assigns elements to a shared group)

Attention: For example, if you'd like to filter and cluster your genes, this would create a new perspective of genes. If you would like to stratify your patients into four groups, this would create a new perspective for patients. To show your data in a heat map, you need both, the perspectives of genes and patients.

If you just load a dataset Caleydo automatically creates default perspectives containing all rows or columns for you. 

For virtually all operations in Caleydo you must specify, which dataset you want to use, which perspective you want to use for the rows in the dataset and which perspective you want to use for the columns. In many cases this might be implicit, for example, because there is only one possible combination, but sometimes you will have to specify these things yourself.

Startup
-------
Upon startup you are presented with choices for different ways to start Caleydo. These are:

 * **Load Demo Data** - with readily set-up sample projects
 * **TCGA Data** - provides access to pre-packaged TCGA data files. 
 * **Load Genetic Data** - load your own files that have a reference to a common genetic identifier. You can also access a sample gene expression file.
 * **Load Other Data** - load files that do not have a genetic identifier.
 * **Load Project** - load a project you previously saved, or continue after a previous session.
 
### Load Demo Data
This is the ideal choice if you want to explore the functionality of Caleydo but don't want to bother loading your own data. You can choose from two demo projects: The first project is especially suited to try out StratomeX for multi-dataset analysis, while the second project is recommended for pathway-centric analysis using enRoute.

You don't need to worry about data formats or how to load data, so you can skip to the next section.

### Load Genetic Data
Use this option if at least some of your data is from molecular biology.

When you load genetic data you need to specify the organism that the data is taken from. Currently Caleydo supports human and mouse data. You can load data from other organisms through the "Load Other Data" tab, but you won't have quite the same functionality as for these two organisms.

Note that you can't change the organism at runtime and that you can't load data from multiple organisms at a time. You can however combine "other data" with data from one organism.

When you choose to load genetic data, pathway maps are also loaded.

To get an idea of how the import of individual datasets works, you can also choose to load a sample gene expression dataset.

### Load Other Data
Use this option if none of the data you want to analyze is from sources other the molecular biology.

### Load Project
Here you can choose to load a Caleydo project file from your hard drive or continue where you left of when you last quit Caleydo.



Data Format
-----------

Here we discuss the format your data has to have if you want to load it into Caleydo.

You can load tabular data from delimited text files (or comma-separated files) into Caleydo. We refer to each of these files as one dataset. These files have to adhere to specific conventions, which we will explain in the following. Asides from text files for datasets, you can also load groupings (e.g., as calcualted by a clustering algorithm). Caleydo also loads pathway maps as datasets, but you can't load your own pathways.

Dataset Conventions
File Format: Caleydo supports delimited, or comma-separated files with the file extensions .csv, .txt, and .gct.
Delimiters: Any kind of delimiter is possible. The most common delimiters are TAB and Semicolon.
Identifiers The file must contain identifiers (headings, titles, captions) for both, rows and columns. You can choose which line and which row contains the identifiers.
Columns: The file may contain columns with data that you don't want to load. You can remove them before importing. All columns must be of equal length.
Rows: The file may contain a header, which can be ignored when loading. After the header, every row until the end must contain data.
Values: For categorical data, any value is legal. For numerical data, real values have to be provided, where the decimal symbol is period (.) not comma (,). 0.3445 is a legal value, 0,3445 is not. Empty cells are legal and are treated as NaN (not a number). Also, if you have some other, non-numerical value in a cell of a numerical dataset, it is treated as NaN.
Here is an example of a legal table of numerical data:

Header Line with some Information not loaded
ColumnID1	ColumnID2	ColumnID3	ColumnID4		ColumnID6	ColumnID7
Some Text	RowID1	1.3	null	1.4	0.2	0.5	0.2	0.6
Some Text	RowID2	1.3	1.5	0	0.24	0.5	 	1.7
Some Text	RowID3	 	0.2	0.4	3.2	1.4	1.5	NaN


Grouping Data Format
Groupings contain groups of identifiers. Groupings allow you to classify your data values into discrete groups. For example, a grouping into two groups of the columns of the above table would be [ColumnID1, ColumnID3] [ColumnID2, ColumnID6], containing two groups both of size two. Groupings make sense for both, columns as well as rows.

Caleydo lets you calculate groupings on the fly by using clustering algorithms at runtime. You can, however, also load external groupings. The grouping data format is very similar to the dataset format. However, it contains information on groups instead on data. In a grouping file, each grouping (you can have only one, or as many as you like in a single file) is represented in a column. A special column contains the ids of the entries you want to group. A grouping is then defined by identical strings in a column. Here is an example using the IDs of the previous example.

Grouping Header Line with some Information not loaded
Grouping 1	Grouping 2	Grouping 3
ColumnID1	1	TypeA	1
ColumnID3	2	TypeB	1
ColumnID2	1	TypeA	Class 2
ColumnID7	1	TypeA	1
ColumnID4	2	TypeA	Class 2
ColumnID6	3	TypeB	Class 2
This example gives 3 groups for Grouping 1 (in this case: [ColumnID1, ColumnID2, ColumnID7] [ColumnID3, ColumnID4] [ColumnID6]), 2 groups for Grouping 2 and 2 groups for Grouping 3.

Again, this works equally for columns and rows of the dataset file. The only requirement is that the IDs between the files match.



Loading Data
Here we discuss how datasets and groupings are loaded from the delimited text file and what options you have to process your data. A wizard guides you through the individual steps of data loading.

The Import Data Dialog
Loading a Dataset
The picture on the right shows a correctly configured import dialog. The first step is to press the "Open Data File" button and select a delimited text file from your hard drive. Once you loaded the data file it will appear in the preview table. As "TAB" is selected as the default delimiter, you may have to adjust the delimiter until you see a correct table.

You can enter a custom dataset name or go with the one that was automatically selected.

Next, you have to choose, whether the dataset is homogeneous or inhomogeneous. A dataset is considered homogeneous, if all of its columns have the same type, meaning, and bounds. An example of a homogenous numerical dataset would be a file that only contains gene expression values with the same bounds for all columns. A file of categorical data is homogeneous, if the same categories are used in all columns. In contrast, an inhomogeneous dataset may contain both categorical and numerical columns with different categories and bounds.

As Caleydo only considers columns for determining the homogeneity of a dataset, you can swap rows and columns by clicking the "Transpose" button on the top left of the preview table if your data file encodes this information in the rows.

You also have to configure the IDs of rows and columns. If you are loading a genetic dataset, chances are that everything is already in order, because Caleydo tries to guess the IDs in the file.

If that is not the case you will have to select or create ID Types and Identifiers by yourself. We will briefly explain the ID mapping concept in Caleydo, so that you will know what to do here.

ID Mapping
Caleydo uses a "foreign key" principle for mapping between multiple datasets, between datasets and groupings, as well as between datasets and online databases. The following two tables are an example for the approach:

Sample 1	Sample 2	Sample 3
Gene 1	1	1.1	0.4
Gene 2	2	0.5	1.2
Gene 3	1.4	0.2	0.5
Gene 4	0.3	0.5	0.7
Gene 3	Gene 87	Gene 2
Sample 2	1	1.1	0.4
Sample 1	2	0.5	1.2
Sample 6	1.4	0.2	0.5
The Import Data Dialog
Both tables contain the same Identifiers, "Sample ID" and "Gene ID". By telling Caleydo which identifier the file has in the columns and in the rows of the file, we can later resolve relationships between multiple datasets. In the example above, we can, because of we know that for the left table Sample is the identifier for the columns, while it is the row's identifier for the right table.

Sometimes, however, things are a little more complicated. As we often have more complex relationships between identifiers we need to introduce ID Types. ID Types define a family of identifiers which can be mapped among each other. In most cases you won't need to define more complex relationships by yourself, but the predefined "GENE" ID Type is an example: it contains various identifiers such as "Refseq", "Gene Symbol", "David ID", "Ensemble ID", etc., which can all be mapped to each other.

That's why you have to define both, ID Types and identifiers for rows and columns (except the dataset is inhomogeneous, because in this case an ID Type or identifier makes no sense for columns). If you have an ID Type, or and an identifier, which is not yet available in the drop-down menu, you can easily create a new one. If you later load another dataset with the same ID Type or identifier, Caleydo will be able to analyze relationships between them.

If you do not want or need to map rows or columns to other datasets, groupings, or databases, you can select "" in the dropdown menu for the Row or Column Type.

Asides from specifying the type of IDs, you also have to specify where the IDs are by selecting the correct column that contains the row IDs at the "Column with Row IDs" respectively the "Row with Column IDs" fields. The selected column and row are highlighted in green in the preview table.

For rows, you have to make sure that you excluded possible leading lines in the file. In the picture above, the line containing the heading "Signal" in all columns is grayed out, because the fields "Number of Header Rows" was set to 2. The row with the ID types is part of the headers.

For columns, you can exclude individal columns by deselecting the checkbox at their headers.

In some cases you might want to map identifiers from two datasets, which are stored in a slightly different format. For example in dataset A the ID of an entity is "TCGA_001-03" whereas in dataset B the ID of the same entity is "tcga.001.03". In order to make Caleydo match them, you can define how to parse row or column identifiers by pressing the corresponding "Define Parsing" button. Doing so will open up the dialog shown on the right. First, you can choose, whether the case of the IDs should be modified, i.e., whether to keep the case unchaged, to make it upper case, or to make it lower case. Second, you can use a regular expression (see reference) to replace all occurrences of a certain string with a different string. Third, you can specify a regular expression to split an ID around matches into several substrings and use the first substring as resulting ID. This dialog also shows a preview of all applied changes to an ID taken from the dataset.

After you have adjusted all necessary settings, you can now or continue to the next wizard page.

Specifiying the Data Type for Homogeneous Datasets
If you have selected your dataset to be homogeneous on the first wizard page, you can set whether the data within this homogeneous dataset is numerical or categorical on the second page. Depending on your choice you can continue to the next page for specifying numerical or categorical properties for the whole dataset.

Specifying Properties for Inhomogeneous Datasets
If you have selected your dataset to be inhomogeneous on the first wizard page, you can set individual data properties for each column on the second page, which is shown to the right. The displayed table contains all columns that were selected on the first page. Caleydo automatically tries to determine the data type (numerical/categorical) and properties for each individual column. The currently set data type of a column is displayed in its header. To check or change the data type and properties of a column you can click on the "Properties" button in its header. This will open up a dialog, where you can choose whether the column contains numerical or categorical data and set numerical and categorical data properties respectively.

After the properties of all individual columns have been specified, you can either finish dataset loading, or optionally load additional groupings for the dataset on the next page.

Properties for inhomogeneous datasets
Numerical Data Properties
Depending on whether the dataset is homogeneous or inhomogeneous, numerical data properties are either set for the whole dataset or for individual columns. The figure on the right shows the available options.

Data Type
Choose, whether the numerical values are integers or real numbers.

Data Scale
In some cases, it can be beneficial to use a logarithmic scale instead of a linear scale. You can choose to use a logarithmic scale for the visualizations in Caleydo by specifying one of the provides logarithms, where log2 is the most common choice. Note that Caleydo will not transform the data itself, so you will always see the original values when they are printed, but will scale the visualizations.

Data Clipping
You can choose to clip the data at a specified maximum or minimum. This can make sense to handle some outliers, which would otherwise ruin the distribution, but when you don't want to use logarithmic scaling.

Data Center
A data center can be set to define a neutral center point of the data. If set, the value range of the dataset is assumed to be equal in positive and negative direction from the center point. So, for a dataset whose values range from -0.3 to 0.5 with a data center of 0, the value range will be set to -0.5 to 0.5.

Data Transposition
By default, Caleydo treats the column in the files as the "columns" in the visualizations. For example, in a paralle coordinates view, each column would correspond to an axis. If you choose to "Swap Rows and Columns" then the columns of the input file would correspond to a polyline in the parallel coordinates view.

This makes a lot of sense when you want to analyze very many columns. Also, it is common that in genetic data files the patients or samples are stored as columns while the genes or other entities are stored in the rows. This would always leave the patients/samples in the table as the columns in the visualizations. Here's a rule of thumb: If you want to focus your analysis on relationships between genes, don't select this. If you want to compare patients or samples, choose this.

Numerical data properties
Categorical Data Properties
As for numerical properties, depending on whether the dataset is homogeneous or inhomogeneous, categorical data properties are either set for the whole dataset or for individual columns.

At first you have to define whether the categories are ordinal or nominal. Ordinal categories have an inherent order, whereas nominal categories don't. For example, the categories "child", "adult", and "senior" for population groups would be ordinal, whereas gender with categories "male" and "female" would be nominal.

The table in this interface shows all categories as rows that have been automatically detected by Caleydo. For each category it shows the value of that category within the data file, the number of occurrences of that category, the name of the category, and an assigned color. The name of a category can be changed in-place within the table cell. You can also add new categories or remove existing categories using the buttons on the right. If the categories are ordinal, you can change the order of categories by moving individual rows up or down using the buttons in the row header.

You can also apply color schemes to the categories by clicking "Select Color Scheme". Depending on the category type, you can choose from a range of qualitative color schemes for nominal categories, from sequential color schemes for ordinal categories without neutral category, and from diverging color schemes for ordingal categories with a neutral category. You can define one of the categories to be neutral using the corresponding dropdown box on the right side. Use the "Reverse Color Scheme" button to apply the scheme's colors bottom-up instead of top-down.

If you want to specify your own color for a category, you can do so using a color dialog that appears when double clicking the category's color.

Categorical data properties
Loading Groupings for a Dataset
As already discussed, you can load groupings independently for columns and for rows. Note that columns and rows here refers to the columns and rows as they are oriented in the original dataset. A possible transformation is ignored.

First you will see the dialog on the left, where you can add, edit or remove groupings for rows and columns independently.

The Import Data Dialog

The Import Data Dialog
Once you click one of the "Add" buttons, you will see the dialog on the right. The dialog on the right resembles the data import dialog you have seen before. As groupings also use identifiers for their rows, you have to choose an identifier. You can't choose an ID Type, since that is already determined by your choice of columns or rows for the dataset.

Again select the "Number of Header Rows" to be excluded and identify the "Column with Row IDs", the column that contains the IDs for the rows, which is highlighted in green.

In the example here, we have loaded a file that contains two groupings. You can choose which grouping of the file to load by checking or unchecking the columns.

You can specify a "Grouping Name" for each grouping. If you choose "Use Grouping Names from Header Row", yaou can specify a row within the header rows of the file, which contains the grouping names (highlighted in green). Alternatively, you can choose "Use Custom Grouping names" to directly enter the name of individual groupings within a special row of the preview table.

You can add an arbitrary number of groupings.

Once you press finish the dataset will be loaded and Caleydo will be started. First you will see a map of the datasets loaded and the open views.

Adding Datasets and Groupings at runtime
You can add more datasets once Caleydo is running. To do so, go to "File > Import Data" which brings you right back to the import wizards. Alternatively, click the "Import Data Icon" in the toolbar.

To add more groupings to an existing dataset, right-click on the dataset in the Data-View Integrator and select the appropriate choice.
