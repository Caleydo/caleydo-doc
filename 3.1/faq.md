# Caleydo Help FAQ - Frequently Asked Questions

## Reporting Problems

**Q: I found a bug! What should I do?**

- Please file a bug at [github](https://github.com/Caleydo/caleydo/issues), be as clear as you can about your situation and include a the log.

**Q: Where do I find the logs?**

- You can find your log file in the *.caleydo_3.0/logs* folder which is stored in your home directory (e.g. *C:\Users\USERNAME\.caleydo_3.0* on Windows).

## Problems Running Caleydo

**Q: Caleydo fails to start after updating to a new version.**

- Try deleting the caches of the old version by removing *.eclipse* and *.caleydo\_3.0* folders from your home directory (e.g. *C:\users\USERNAME\.eclipse* and *C:\users\USERNAME\.caleydo\_3.0*)

**Q: Caleydo fails to start with the message: Failed to create Java Virtual Machine.**

- It seems that your machine has not enough main memory. However, you can try to reduce the initial Java Virtual Machine memory impact by manipulating the *Caleydo.ini* file. Reduce the two entries: *-Xms512m* and *-Xmx2048m* by a factor of two and try it again.

**Q: Caleydo does not start with the following error message on the console:**

    !SESSION 2013-05-06 17:22:06.045 -----------------------------------------------
    eclipse.buildId=unknown
    java.version=1.7.0_21
    java.vendor=Oracle Corporation
    BootLoader constants: OS=macosx, ARCH=x86_64, WS=cocoa, NL=en_US
    
    !ENTRY org.eclipse.equinox.ds 4 0 2013-05-06 17:22:09.266
    !MESSAGE [SCR] Exception while activating instance org.eclipse.e4.ui.css.swt.internal.theme.ThemeEngineManager@3c867009 of component 
    org.eclipse.e4.ui.css.swt.theme  
    !STACK 0
    java.lang.NoClassDefFoundError: org/eclipse/swt/widgets/Display
           at java.lang.Class.getDeclaredMethods0(Native Method)
           at java.lang.Class.privateGetDeclaredMethods(Class.java:2451)

- This error occurs when running Caleydo with the wrong system architecture, meaning that you are, for example, trying to run a 32 bit version on a 64 bit computer.

**Q:** **Caleydo still doesn't start, doesn't load my data, or fails somehow else. What can I do?**

- Please [file a bug](https://github.com/Caleydo/caleydo/issues) or send us an e-mail (caleydo at icg dot tugraz dot at) with the latest log file and, if possible, the dataset you tried to use. 


## Data 

**Q: Can I load my own data sets into Caleydo?**

- Yes, Caleydo has extensive support for loading data from a variety of file formats.

**Q: Can I load my own pathways into Caleydo?**

- No, Caleydo currently does not provide a user interface for adding pathways.

**Q: Do you support organisms other than mouse and humans?**

- Not at the moment. You can load arbitrary data into Caleydo, but you won't be able to map other organisms' data to pathways. We consider adding support for more organisms in the future. 

## About the Project

**Q: What is Caleydo, what are StratomeX, enRoute and Entourage?**

- Caleydo is a framework for biomolecular data visualization and StratomeX, enRoute and Entourage are tools built on top of the Caleydo framework.

**Q: What does Caleydo mean?**

- Caleydo is a word-play on Kaleidoscope. Like a Kaleidoscope, Caleydo lets you look at the same thing in many different ways. 

**What does "StratomeX" mean?**

- "StratomeX" stands for "Stratome Explorer" and we define the "stratome" as the set of all possible patient stratifications with a particular type of cancer.

**Q: What are the licensing terms for Caleydo?**

- Caleydo is open source software licensed under the new BSD License.

**Q: How should I cite StratomeX?**

- Please cite: Alexander Lex, Marc Streit, Hans-Jörg Schulz, Christian Partl, Dieter Schmalstieg, Peter J. Park and Nils Gehlenborg: StratomeX: Visual Analysis of Large-Scale Heterogeneous Genomics Data for Cancer Subtype Characterization. Computer Graphics Forum (EuroVis '12), pp. 1175-1184, 31(3), June 2012

**Q: How should I cite Entourage?**

- Please cite: Alexander Lex, Christian Partl, Denis Kalkofen, Marc Streit, Anne Mai Wasserman, Samuel Gratzl, Dieter Schmalstieg and Hanspeter Pfister: Entourage: Visualizing Relationships between Biological Pathways using Contextual Subsets. IEEE Transactions on Visualization and Computer Graphics (InfoVis '13), vol. 19, no. 12, pp. 2536–2545, 2013.

**Q: How should I cite enRoute??**

- Please cite: Christian Partl, Alexander Lex, Marc Streit, Denis Kalkofen, Karl Kashofer and Dieter Schmalstieg: enRoute: Dynamic Path Extraction from Biological Pathway Maps for Exploring Heterogeneous Experimental Datasets. BMC Bioinformatics, vol. 14, no. Suppl 19, p. S3, Nov. 2013


## The Cancer Genome Atlas (TCGA) Datasets

**Q: How does Caleydo support TCGA data?**

- Caledyo pre-packages data for all TCGA tumor types from the TCGA project's Firehose pipeline and makes it available through a download interface visible when running Caleydo. 

**Q: What is Firehose?**

- Firehose is a data analysis pipeline developed and maintained by the TCGA Genome Data Analysis Center at the Broad Institute. The GDAC website and the Firehose FAQ provides important background information the operation of the system.

**Q: Where does the data come from?**

- Data packages are generated monthly from the publicly available Firehose "Data Analysis Run" results. Additional data is loaded from the corresponding Firehose "Standardized Data Packages", which are also public.

**Q: How was the data analyzed?**

- Due to the complexity of the Firehose analysis pipeline we refer to the Nozzle analysis reports we link to for each data package, i.e. for each tumor type in a given "Data Analysis Run". As of Novemer 2012 we use results from the "MutSig" (Mutations), "GISTIC 2" (Copy Number), "Consensus Hierarchical Clustering" (mRNA, mRNA-seq, microRNA, microRNA-seq, Methylation, RPPA) and "Consensus NMF Clustering" (mRNA, mRNA-seq, microRNA, microRNA-seq, Methylation, RPPA) pipelines for our data packages.

**Q: What is the difference between m(icro)RNA and m(icro)RNA-seq?**

- mRNA and microRNA data sets were generated using microarray technology, whereas mRNA-seq and microRNA-seq were generated using next-generation sequencing technology.

**Q: What is RPPA?**

- RPPA stands for "Reverse Phase Protein Array". Some background about the technique is available on the website of the MD Anderson Cancer Center website.


**Q: Why are the number of patient samples in Caleydo different from the numbers on website of the TCGA Genome Data Anaylsis Center at the Broad Institute?**

- We only report the number of patient samples that we are able to include in the data packages, while the website at the Broad Institute reports the number of patient samples downloaded from the TCGA Data Coordination Center.


