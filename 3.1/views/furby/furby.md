# Caleydo Help - Furby: Fuzzy Force-Directed BiCluster Visualization

Furby is a visualization technique for the analysis of soft biclustering results. For a general introduction please refer to the [Furby project page](http://furby.caleydo.org/). 

## Concept

![](views/furby/i/bicluster_concept.png "Furby concept")

Furby interprets and visualizes a biclustering result as a graph in which nodes are the bicluster and edges represents shared rows and/or columns between the bicluster. 

![](views/furby/i/overview.png "Screenshot of Furby")


## Interaction

### Toolbar
![](views/furby/i/parameter_toolbar.png "Explained Parameter Toolbar")

The image shown on top, presents an annotated version of the main toolbar of Furby. 
It contains of following sections: 

 * **Data Order**
   The data order within a bicluster node can be defined independently for the record (gene) and column (sample) dimension. Several different sorting criteria are provided, including by membership level, original data order, and by an additional attached categorical metadata.
 * **Presentation**
   In this section of the main toolbar several different visual settings can be changed. Like the visibibility of the sample or gnee bands or the overall used visualization technique to present a bicluster. Besides a common Heatmap representation, additional methods exists including a Barplot style and an histogram highlighting the distribution of the bicluster elements. 
   
   A scalability related feature of Furby is letting the analyst focus on the local neighborhood of a bicluster node. This is realized by fading out unrelated cluster and bands. To decide which nodes are unrelated to the current hovered one, the max distance parameter is used, such that a node is related to the node, if it is reachable within N hops in the underlying graph. 
 * **Fuzzy Treshold**
   Furby can be used to analyze soft/fuzzy biclustering results. A important step in the analysis of soft biclustering results is the tranformation of the soft bicluster into hard ones, by settings a threshold in the soft membership values. The thresholds can be defined using the sliders, where in the background the distribution of the membership values is shown. In addition, the maximum number of elements per bicluster can be restricted to the top M elements. It allows you to show e.g. just the top 20 matching rows and columns. 
 * **Miscellaneous**
   Bicluster can be hided by pressing the close button in the bicluster specific toolbar. This list will contain the hidden elements an by clicking on the bicluster name, it will again become visible.	
   

## Detailed View
![](views/furby/i/single.png "Annotated detail view of a focussed bicluster")

