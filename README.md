**Evaluating the Impact of Read Length on RNA-seq Based Differential Expression Using Galaxy and Searchlight**

**Overview**

This project investigates the effect of different read lengths on RNA-seq-based differential gene expression (DGE) analysis using the Galaxy platform and Searchlight tool. The goal is to evaluate whether shorter reads like 2x59bp and 2x34bp can replace the golden standard 2x75bp paired-end reads without compromising accuracy. The study is conducted on Arabidopsis thaliana under salt stress conditions.
**Study Highlights**

    Organism: Arabidopsis thaliana
    Genotypes: Histone Deacetylation Complex 1 (HDC1) and Knockout (KO)
    Conditions: Salt vs Control
    Replicates: 3 biological replicates per condition (12 samples in total)
    Accession Number: GEO GSE205893 (available publicly in June 2024)

**Tools Used**

    Galaxy: Open-source platform for RNA-seq analysis, quality control, trimming, mapping, and DGE analysis.
    Searchlight: Tool for visualizing RNA-seq data and performing downstream analysis.
    Reference Genome: Arabidopsis thaliana TAIR10.1.

**Objectives**

    Evaluate whether 2x59bp and 2x34bp reads can serve as cost-effective alternatives to the golden standard 2x75bp paired-end reads.
    Assess how well single-end reads (1x75bp, 1x59bp, 1x34bp) perform in comparison to paired-end reads.

**Methodology**

    Preprocessing:
        Quality control using FastQC.
        Trimming reads to lengths of 75bp, 59bp, and 34bp using Trimmomatic.

    Read Alignment:
        HISAT2 was used to map reads to the reference genome.

    Differential Expression Analysis:
        DESeq2 was employed to identify DEGs between salt and control conditions for each read length.

    Gene Ontology:
        Enrichment analysis using Searchlight to evaluate biological functions.

**Results**

    PCA Analysis: PCA plots showed consistent clustering across different read lengths, suggesting minimal impact of read length on sample clustering.

    DEG Analysis: The number of differentially expressed genes (DEGs) identified with 2x59bp was almost identical to those detected with 2x75bp, indicating that 2x59bp reads can reliably substitute for 2x75bp paired-end reads.

    Gene Ontology: The 2x59bp reads closely matched the biological functions and pathways identified with the 2x75bp reads, confirming the accuracy of shorter paired-end reads.

**Key Findings**

    2x59bp reads offer a cost-effective alternative to 2x75bp paired-end reads with no compromise in accuracy.
    Single-end reads, particularly 1x75bp, exhibited more variation and are less reliable for RNA-seq analysis compared to paired-end reads.

**Limitations**

    The study is limited to a single dataset and organism (Arabidopsis thaliana). Further validation on different organisms and larger genomes is needed.

**Future Directions**

    Extend this analysis to other datasets and model organisms to confirm the generalizability of the findings.
**Acknowledgments**

    Supervisor: Dr. Pawel Herzyk
    Special thanks to Dr. John Cole and Dr. David McGuinness for their support throughout this project.
