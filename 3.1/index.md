# Caleydo Help - Overview

**Welcome to the help pages of the Caleydo Visualization Framework!**

Caleydo is a visualization framework for biomolecular data. Caleydo lets you load your own *tabular data* (in the form of csv or text files) for multiple datasets and analyze it using visualization an algorithms. Caleydo comes with *biological pathways* build-in, that you can explore by themselves or in the context of your own data. Caleydo also provides integrated access to all *[TCGA datasets](http://cancergenome.nih.gov/)*.


While designed for biological data, Caleydo is not limited to biomolecular data, so you may also try other forms of tabular data if you like!

This is the Help for Caleydo **Version 3.1**

Other help versions: 

 * [Caleydo 3.0](../3.0/index.html)
 * [Caleydo 2.0](http://www.icg.tugraz.at/project/caleydo/help/caleydo-2.0/caleydo-help)
 * [Caleydo 1.3](http://www.icg.tugraz.at/project/caleydo/help/caleydo-1.3)

## Supported Data
 * Caleydo lets you load multiple tabular datasets at the same time. Provided they have some common identifier you can analyze dataset interdependencies.
 * Datasets can be numerical or categorical.
 * You can load groupings or clusterings for your datasets, or you can cluster or group your data at runtime.
 * Caleydo supports a variety of genetic identifiers, including DAVID IDs, gene names, RefSeq IDs, ENSEMBL IDs, ENTREZ IDs or Biocarta IDs.
 * Caleydo can automatically download pathways from [KEGG](http://www.genome.jp/kegg/pathway.html) and [WikiPathways](http://wikipathways.org/), giving you the opportunity to map your experimental data onto them.
 * [TCGA data](http://cancergenome.nih.gov/) is provided pre-packaged for Caleydo.

## Analysis

Caleydo is made for two major tasks: analysis of stratifications (groupings, clusterings) of multiple datasets and pathway analysis. 

### Analyzing Stratifications

*[StratomeX](views/stratomex/stratomex.md)* is used to visualize tabular data with various visualization techniques such as heat maps, histograms, parallel coordinates, etc. The unique feature of StartomeX, however, is it's ability to analyze multi-dataset dependencies and differences between groupings/clusterings. 

Hint: This lets you, for example, compare the properties of patients across multiple datasets. You can compare an mRNA clustering to the copy number status of a gene, see if there is a relationship to clinical parameters such as gender, explore the effects of stratifications on clinical outcomes, etc.

### Analyzing Pathways

Caleydo includes sophisticated techniques to analyze *interdependencies between pathways* using the [Entourage](views/pathway/pathway.md#entourage) view and to analyze *experimental data in the context of pathways* using the [enRoute](views/pathway/pathway.md#enroute) view. 

Hint: This lets you, for example, identify the role of a gene in multiple pathways and compare the paths in similar pathways, or identify similar or other relevant pathways. Mapping experimental data onto pathways lets you reason about the effect of patient's or cell line's molecular profile on a pathway, or lets you judge the effect of a drug on a pathway for specific patients.  
 

Note: Help us improve this documentation!
The sources are hosted at our GitHub [caleydo-doc](https://github.com/Caleydo/caleydo-doc) repository and use Markdown - a simple syntax, that is then rendered using [mdwiki](mdwiki.info) for rendering. If you want to extend the help content or fix some typos, you are welcome to contribute.

