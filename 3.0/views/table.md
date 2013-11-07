## Table
The table view is a scalable raw data viewer that can be used to display arbitrary table perspectives.

![](views/i/table.png "The table viewer")

The table view supports:

* **Record / dimension groupings**
  If the selected table perspective contains record or dimension stratifications, the table view groups the corresponding rows / columns together, similar to the MS Excel grouping feature.

* **Scalability**
  The viewer internally uses [Nattable](http://www.eclipse.org/nattable/) for rendering and therefore scales to very large tables. 

* **Different data representations**  
  In addition to the raw data, the normalized data can be shown.

* **Selection** 
  The selection of table cells is synchronized with the global selection mechanism, such that selections from other views are highlighted in the table and vice versa.

* **Selection only** 
  In this mode, only the currently selected rows and columns are shown in the table.

* **Variable formatter** 
  The number of decimal places can be changed via the view menu.
