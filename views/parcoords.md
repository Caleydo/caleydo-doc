## Parallel Coordinates
 
Attention: The information on this help page is outdated. Use with care.

Parallel coordinates visualize multidimensional data by drawing lines between a set of axis. Each line represents one entity, typically a gene. Each axis a dimension, typically an experiment. When one gene is viewed in the parallel coordinates, all it's expression values for the experiments are visible simultaneously. By drawing multiple lines at the same time, trends in a dataset can be identified. In the screen-shot a dense (dark) area around the bottom shows that many genes have expression values in this area. In parallel coordinates you can select the polylines as well as the axis. The current selection will be shown in the [Selection Info](#Selection_Info).
![](views/i/parcoords_example.png "Screenshot of the parallel coordinates view") 

### Rearranging axis
To make an accurate comparison between two different experiments it is often necessary to place them side by side. Therefore it is important to be able to re-arrange and duplicate, possibly also remove unneeded experiments.
![](views/i/parcoords_drop.png "")

![](views/i/parcoords_reset_axis_spacing.png "") 
The parallel coordinates use a drop below the axis, shown in the picture on the right to achieve this task. By default the drop is shown in a small, simplified version. Once the mouse is placed over it, it changes to the version containing three buttons. By clicking the left button, the associated axis is **duplicated**. By clicking the right button, the axis is **removed**. By dragging the central button to the sides, the axis is dragged along and consequently **rearranged**. When dragging around axes, the spacing between the axes can become uneven. To balance the spacing between the axes again, click the icon shown on the left in the tool bar.

### Filtering
The parallel coordinates view supports three types of filters, a one-dimensional filter, a global filter and an angular filter. 

The **one-dimensional filter** allows you to remove all genes that are smaller and/or larger then a specified value. To activate the brush for a particular axis click the small drop on top of the axis (shown on the right). This makes the filter, as shown on the left appear.
![](views/i/parcoords_gate.png "") 
![](views/i/parcoords_drop_gate.png "") 

To change the height of the filter, click the black labels with the caption and drag them up or down. This adjusts the size of the filter an thereby adds or removes polylines. By dragging the body of the filter the top and the bottom are moved simultaneously.

To remove the brush click the handle right of the top label.

The **global filter** works excatly the same, but has different consequences. To activate the global filter, click the drop at the tip of the line on the far left of the parallel coordinates. Again, the filter appears.

This filter allows to remove all lines that never leave a specified corridor. This helps to remove those genes, that are neither over- nor underexpressed in any experiment. It removes all polylines that don't leave the spanned region in any of the experimental conditions currently visible. So, if you set this filter to span the region between 1 and 3, all genes, that only have expression values between 1 and 3 are removed. If only one value for that gene is smaller or bigger, the gene is not removed.

![](views/i/parcoords_angular_brush.png "")  Angular FilterThe **angular filter** can be used to identify discontinuities between two experiments. It allows you to remove all lines, that are not similar to a certain slope of a master line. First click on the icon for the angular brush in the toolbar (shown on the left). Then click on a polyline, between two axis where it has a slope which you would like to use as the basis for your filter. Once you clicked the polyline, the brush appears, as shown on the right.

By dragging the legs up or down, you can adjust the level of tolerance for matching the slope of other polylines.

![](views/i/parcoords_clear_selections.png "") To **clear selections and filters** press the clear selections icon. This will remove all filters, mouse-over and clicked selections you previously applied.

![](views/i/parcoords_save_selections.png "") The **save filters** feature allows you to actually remove all items that you currently filtered out. This is useful, if you handle a lot of data and want to continue working with a subset. Also, if you want to export your filtered data you have to press this button first. The same is true for swapping dimensions and bookmarking genes, which will be explained later.

### Resetting the View
![](views/i/parcoords_reset_view.png "") By clicking the reset button, the view is reset to its initial state. All re-arranged axes, all removed polylines are added again.