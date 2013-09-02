# StratomeX: Multi-Dataset Analysis
StratomeX is a visualization technique for the analysis of multiple stratified datasets. For a general introduction please refer to the [StratomeX project page](http://stratomex.calyedo.org/). 

[StratomeX Elements](#StratomeX_Elements)
[TourGuide Wizard](#TourGuide Wizard)
[LineUp](#LineUp)

[](http://www.youtube.com/watch?v=UcKDbGqHsdE)

## StratomeX Elements
### Brick Columns
Each column in StratomeX consists of multiple data columns from one of the loaded datasets. The rows inside a brick column are grouped together to form so called bricks.

 * **Adding columns** Columns can be added using the [Data-View Integrator](dvi.md).
 * **Removing columns** Columns can be removed by either using the close icon that is appears when hovering over the header brick or by selecting the corresponding option in the right-click context menu of the header brick.
 * **Reordering columns** Columns inside StratomeX can be reordered by using drag-and-drop. Pick the header brick, hold the mouse button, move the column to the new position and release the mouse button.

### Bricks
A brick is a small rectangular view that visualized a certain subset of the dataset. There are two different kinds of bricks in StratomeX:

 * **Header bricks** The topmost brick in each brick column is called a header brick. Header bricks summarize the data contained inside the brick column in a histogram.
 * **Cluster bricks** Cluster bricks are groups of rows inside the brick column. The data inside a brick can be shown using different visualization techniques. By default, data inside a brick is visualized as a heatmap. The following interactive features are supported by bricks:
 * **Switching visualization** StratomeX represents cluster bricks using a heatmap representation and header bricks as a histogram. You can switch to other visualization techniques by hovering over the brick and clicking on one of the icons that appear above the brick.
 * **Resorting cluster bricks** The reordering of cluster bricks works similar to the column reordering. By using drag-and-drop the order of cluster bricks inside a brick column can be changed.
 * **Switching to detail mode** In order to present as much information at once, cluster and header bricks are usually rather small. The detail mode is a feature that allows you to show an enlarged version of any brick. The enlarged version of a brick can be activated by clicking on the small left or right pointing arrow that is shown when hovering over a brick.

### Connection Bands
Connection bands show the rows that are shared between connected cluster bricks. Therefore, connection bands help users to see which portion of each group is contained in other groups as well. You can select any connection band to interactively investigate to which group the selected rows belong to in any of the shown brick columns.

### Dependent Columns
Dependent columns are special brick columns that belong to an existing brick column because they derive their grouping. For instance, pathways or clinical data are represented as dependent columns. Note that dependent columns can currently only be added when the rows in StratomeX correspond to samples and the columns to genes. Dependent columns can be added by right-clicking on the header brick and selecting one of the following data types:

 * **Pathways** When choosing pathways as the type of the dependent column, Caleydo opens a list of pathways with a count how many genes from the brick column are contained in each of the pathways. After a particular pathway has been selected, a new column will be added, where a small pathway is shown for each group of the original brick column. The nodes inside the pathways are color coded according to the average gene expression value of each group.
 * **Clinical data** After choosing clinical data as the type of the dependent column, Caleydo opens a list of clinical parameters that can be added as a new dependent column. Note that clinical data needs to be loaded in order to use this feature. After selecting a particular clinical parameter, a Kaplan-Meier plot will be opened for each group of the original brick column.

[](include:stratomex/tourguide.md)
[](include:stratomex/lineup.md)
