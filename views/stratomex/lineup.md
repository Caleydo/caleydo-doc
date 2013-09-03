##LineUp
LineUp is visualization technique for analyzing multi-attribute rankings. If you want to find out more about this general visualization technique, take a look at the [LineUp project page](http://lineup.caledydo.org). 

![](i/lineup_explained.png "explanation of the LineUp interface used in Caleydo")

In StratomeX LineUp is used as a selection interface for Block Columns. LineUp can be categorized in three areas: 

1. **dataset selection** 
   The first area is used to include and exclude datasets from the ranking query. In addition, clinical and categorical datasets supports simple filtering operations that can be used to filter specific categories and/or specific clinical variable data types. Last but not least a context menu of the dataset items provides additional features including the loading of external grouping and scores.

2. **ranking table** 
   The central area is the original LineUp visualization technique that can be used to rank, filter, browse, and select the contained dataset items in a flexible way.

3. **Memo Pad** 
   The last area of the LineUp interface can be used to persist scores over multiple wizards instances. Please take a look at the [LineUp project page](http://lineup.caledydo.org) for details about the Memo Pad.
   
###Ranking table
The ranking table is the central part of LineUp. It itself consists of multiple columns, which can be freely reordered using drag-and-drop. Each column provides its own menu, e.g. for filtering, searching data. Following different column types are available:

1. **Rank column** 
  showing the rank of the current item

2. **Stratification column** 
  showing the name and the dataset type indicated by color. The column supports simple filtering and search operations.

3. **Score column** 
  depending on the current query zero, one or more score query columns are shown in the ranking table for ranking the dataset items.

4. **General metric columns** 
  This group of columns presents simple statistics about an item, including the number of elements, the number of groups, and a simple group distribution visualization

5. **Data type specific metric columns** 
  For each included categorical datasets additional metric columns are displayed showing the distribution of the contained categories. In addition, dimension stratifications are automatically added as categorical grouping columns.

6. **Externally loaded score columns** 
  Besides automatically created and computed query scores during the TourGuide process, external scores can be imported to the LineUp interface. The import process can be triggered by using the context menu of a dataset. 

###Interaction
Rows can be selected by clicking on it. LineUp also supports navigation via keyboard using up/down keys and page up/down keys and scrolling by mouse wheel. Sorting by a column can be done by double clicking its header. The current sort criterion is indicated by a small triangle glyph above the column header. 

*Expert Note*: Adding an item to StratomeX without having an open TourGuide wizard can be done by double-clicking the item.

Attention: If a TourGuide wizard instance is open, previews will only be shown, when the wizard is in the correct state, otherwise the selection will be ignored. 

###Visual Attributes
The current selected row will be highlighted in orange. Grey rows indicate items that are already visible in StratomeX. An orange dashed border will be used within StratomeX and LineUp to indicate the currently previewed item. 

Score queries based on a parameter (e.g. find similar to a displayed stratification) are colored according the dataset color of the selected parameter, allowing simpler association.
