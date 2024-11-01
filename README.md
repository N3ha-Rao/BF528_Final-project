# bf528-individual-project-NB-Rao

**Project Proposal: RNAseq Analysis**


**Introduction:** In this project, I will perform a comprehensive analysis of RNAseq data derived from 6 samples, including 3 wild-type (WT) and 3 knock-out (KO) samples from a human source. The primary objective is to conduct a basic differential expression analysis comparing the WT and KO conditions. Additionally, I will perform quality control (QC) at both the read and alignment levels, followed by exploratory data analysis and functional enrichment analysis to elucidate biological insights.


**Methods:**

`Quality Control (QC):`
- Utilize FastQC (version 0.11.9) [1] and MultiQC (version 1.20) [2] for initial read quality assessment.
- Perform trimming and filtering using Trimmomatic (version 0.39) [3] to remove low-quality bases and adapters. 
- Assess read quality post-trimming with FastQC (version 0.11.9) [1] and MultiQC [2].
- Use STAR (version 2.7.9a) [4] for read alignment against the human reference genome.
- Evaluate alignment statistics including mapping rates, duplication rates, and coverage using SAMtools (version 1.9) [5].

`Differential Expression Analysis:`
- Generate count matrices using Verse v2.0.5 [6].
- Conduct differential expression analysis using EdgeR v3.26.0 [7].
- Determine appropriate fold change and false discovery rate (FDR) thresholds.
- Subset significant differentially expressed (DE) genes based on chosen statistical thresholds.

`Exploratory Data Analysis:`
- Perform principal component analysis (PCA) or sample-to-sample distance plot using DESeq2 (version 1.30.1).
- Interpret the plot to understand sample relationships and potential batch effects.

`Functional Enrichment Analysis:`
- Employ enrichR (version 3.0) [8] for functional annotation and enrichment analysis.


**Deliverables:**

`Quality Control Assessment:`
- Address any concerns regarding sequencing read quality and alignment statistics.
- Decide on sample exclusion based on QC results.

`PCA Plot:`
- Provide PCA plot.
- Interpret the plot to understand potential batch effects.

`Differential Expression Analysis Results:`
- Provide a CSV containing DE analysis results.
- Generate a histogram showing the distribution of log2FoldChanges.
- Create a volcano plot distinguishing significant DE genes.

`Functional Enrichment Analysis Results:`
- Perform enrichR analysis.
- Provide analysis results summarized in a table or figure.
- Discuss implications of results on biological functions related to the factor of interest.



[1] Andrews, S. (2010). FastQC:  A Quality Control Tool for High Throughput Sequence Data [Online]. Available online at: http://www.bioinformatics.babraham.ac.uk/projects/fastqc/

[2] Philip Ewels, Måns Magnusson, Sverker Lundin, Max Käller, MultiQC: summarize analysis results for multiple tools and samples in a single report, Bioinformatics, Volume 32, Issue 19, October 2016, Pages 3047–3048, https://doi.org/10.1093/bioinformatics/btw354

[3] Bolger AM, Lohse M, Usadel B. Trimmomatic: a flexible trimmer for Illumina sequence data. Bioinformatics. 2014 Aug 1;30(15):2114-20. doi: 10.1093/bioinformatics/btu170. Epub 2014 Apr 1. PMID: 24695404; PMCID: PMC4103590.

[4] Dobin A, Davis CA, Schlesinger F, Drenkow J, Zaleski C, Jha S, Batut P, Chaisson M, Gingeras TR. STAR: ultrafast universal RNA-seq aligner. Bioinformatics. 2013 Jan 1;29(1):15-21. doi: 10.1093/bioinformatics/bts635. Epub 2012 Oct 25. PMID: 23104886; PMCID: PMC3530905.

[5] Petr Danecek, James K Bonfield, Jennifer Liddle, John Marshall, Valeriu Ohan, Martin O Pollard, Andrew Whitwham, Thomas Keane, Shane A McCarthy, Robert M Davies, Heng Li, Twelve years of SAMtools and BCFtools, GigaScience, Volume 10, Issue 2, February 2021, giab008, https://doi.org/10.1093/gigascience/giab008

[6] Zhu Q, Fisher SA, Shallcross J, Kim J. VERSE: a versatile and efficient RNA-Seq read counting tool. bioRxiv; 2016. DOI: 10.1101/053306.

[7] Robinson MD, McCarthy DJ, Smyth GK. edgeR: a Bioconductor package for differential expression analysis of digital gene expression data. Bioinformatics. 2010 Jan 1;26(1):139-40. doi: 10.1093/bioinformatics/btp616. Epub 2009 Nov 11. PMID: 19910308; PMCID: PMC2796818.

[8] Chen, E.Y., Tan, C.M., Kou, Y. et al. Enrichr: interactive and collaborative HTML5 gene list enrichment analysis tool. BMC Bioinformatics 14, 128 (2013). https://doi.org/10.1186/1471-2105-14-128
