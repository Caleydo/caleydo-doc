# Caleydo Help - Overview

**Welcome to the help pages of the Caleydo Visualization Framework!**

Caleydo is a visualization framework for biomolecular data. The most important feature of Caleydo is that you can load tabular data (in the form of csv or text files) and analyze it using visualization an algorithms. That said, Caleydo is not strictly limited to biomolecular data, so you may also try other forms of tabular data if you like!

This is the Help for Caleydo **Version 3.0**

Other help versions: 

 * [Caleydo 2.0](http://www.icg.tugraz.at/project/caleydo/help/caleydo-2.0/caleydo-help)
 * [Caleydo 1.3](http://www.icg.tugraz.at/project/caleydo/help/caleydo-1.3)

## Supported Data
 * Caleydo lets you load multiple tabular datasets at the same time. Provided they have some common identifier you can analyze dataset interdependencies.
 * Datasets can be numerical or categorical.
 * You can load groupings or clusterings for your datasets, or you can cluster or group your data at runtime.
 * Caleydo supports a variety of genetic identifiers, including DAVID IDs, gene names, RefSeq IDs, ENSEMBL IDs, ENTREZ IDs or Biocarta IDs.
 * Caleydo can automatically download pathways from KEGG and WikiPathways, giving you the opportunity to map your experimental data onto them.
 * TCGA data is provided pre-packaged for Caleydo.

## Analysis
The most important view in Caleydo is [StratomeX](views/stratomex/stratomex.md), which you can use to analyze your data using heat maps, histograms, parallel coordinates, etc. Most importantly, however, is StartomeX' ability to analyze multi-dataset dependencies and differences between groupings/clusterings.

For pathway analysis Caleydo includes a pathway view and [enRoute](views/pathway/enroute.md), which in combination enable you to explore pathways from KEGG and WikiPathways in the context of your own experimental data. 
 

Note: Help us improve this documentation!
The sources are hosted at our GitHub [caleydo-doc](https://github.com/Caleydo/caleydo-doc) repository and use Markdown - a simple syntax, that is then rendered using [mdwiki](mdwiki.info) for rendering. If you want to extend the help content or fix some typos, you are welcome to contribute.

