##LineUp
LineUp is visualization technique for analysing multi-attribute rankings. If you want to find out more about this general visualization technique, take a look at the [LineUp project page](http://lineup.caledydo.org). 

![](i/lineup_explained.png "explaination of the the LineUp interface used in Caleydo")

In StratomeX LineUp is used as a selection interface for Brick Columns. 

LineUp consists of three columns: 

1. dataset selection 
   The first column is used to include and exclude dataset from the ranking query used to select data. In addition, clinical and categorical datasets supports simple filtering operations thats can be used to filter specific categories and/or specific clinical variable data types
2. LineUp ranking table
   The central columns is the main LineUp visualization technique that can be used to rank, filter, browse and select the contained dataset items. 
3. Memo Pad
   The last columns of the LineUP interface can be used to persist scores over multiple wizards. Please take a look at the [LineUp project page](http://lineup.caledydo.org) for details. 
   
###Ranking table
The ranking table itself consists of multiple columns. Following different column types are available:

1. **Rank column** 
  showing the rank of the current item

2. **Stratification column** 
  showing the name and the dataset type indicated by color. The column support simple filtering and search operations

3. **Score column** 
  Depending on the current query zero, one or more score query columns are shown in the ranking table.

4. **General metric columns** 
  This group of columns present simple statistics about the item, including the number of elements the number of groups and a simple group distribution visualization

5. **Data type specific metric columns** 
  For each included categorical datasets additional metric columns are displayed showing the distribution of the contained categories. In addition, dimension stratifications are automatically added as categorial groupoing columns.

6. **Externally loaded score columns** 
  Besides automatically created and computed query scores during the TourGuide process, external scores can be imported to the LineUp interface. The import process can be triggered by using the context menu of a dataset. 

###Interaction
Rows can be selected by clicking on it. LineUp also supports navigation via keyboard using up/down keys and page up/down. 

Attention: WRITE ME