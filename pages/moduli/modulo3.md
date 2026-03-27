---
title: Modulo 3
---

![modulo3](images/modulo3/modulo3.jpg)

## Topics
Explore selected bioinformatics resources:

- NCBI Gene and Ensembl (gene annotation databases)
- BioMart (retrieve gene list information without programming)
- NCBI GEO (experimental data repository)
- GEO2R (differential expression analysis tool)
- gProfiler (functional enrichment analysis tool)
  

## Learning Objectives

By the end of this activity, you should be able to:

- Retrieve the HGNC symbol for a given human gene
- Retrieve a list of all human genes annotated with a given GO (Gene Ontology) term.



# Gene Annotations: NCBI Gene e Ensembl

Using the two databases mentioned above ([NCBI Gene](https://www.ncbi.nlm.nih.gov/gene/) and [Ensembl](https://www.ensembl.org/)), try to answer the following questions about the **human gene ZFP36**.

Note: Use this activity as an opportunity to explore the databases visually, taking your time and browsing through the different sections available for a gene of interest. Be curious and pay attention to the various types of information provided.

- *On which chromosome is this gene located?*
- *What type of protein does it encode?*
- *What is its identifier (ID) in the NCBI Gene database? And in Ensembl? Are they the same?*
- *What is its official name (HGNC symbol)?*
- *How many transcripts are annotated for this gene in Ensembl? Are they all protein-coding?*
- *How many transcripts are annotated for this gene in NCBI Gene? Are they all protein-coding?*


**Take-home messages from the above activity:** <br>
- The role of identifiers in a database  
- The main gene identifiers used in core gene annotation databases such as NCBI Gene, Ensembl, and, for human genes, [HGNC](https://www.genenames.org/) symbols
- The meaning of [MANE](https://www.ncbi.nlm.nih.gov/refseq/MANE/) flags in annotated transcripts

❓ **A challenge for you**: *What is the official gene symbol (i.e., HGNC symbol) for the NUP475 gene?*


# Gene Functional Annotations: Gene Ontology (GO) and KEGG

## Gene Ontology

The **Gene Ontology (GO)** provides a rigorously defined set of concepts that describe the functions of gene products. GO develops a computational model of biological systems, ranging from the molecular to the organism level, across all species in the tree of life. GO aims to **provide a comprehensive representation of the current scientific knowledge** about the functions of gene products, namely, proteins and non-coding RNA molecules. 
  
GO is organized in three aspects. 
- **GO Molecular Functions (MF)** describe activities that occur at the molecular level, such as “DNA binding transcription factor activity” or “histone deacetylase activity”.
- **Biological Processes (BP)** represent the larger processes or ‘biological programs’ accomplished by multiple molecular activities. Examples of broad biological process terms are “transcription” or “signal transduction”.
- **Cellular Components (CC)** are the cellular structures in which a gene product performs a function, either cellular compartments (e.g., “nucleus” or “chromatin”), or stable macromolecular complexes of which they are parts (e.g., “RNA polymerase II”).

Together, annotations of a gene to terms from each of those aspects **describe what specific function a gene product plays in a process and where this activity occurs in the cell**.




## the BioMart tool @ EBI: 

The Ensembl BioMart datamining tool offers a single and harmonized access point to a huge amount of information gathered together from hundreds data resources from the EBI-EMBL suite as well as from third-party databases (e.g. miRBase, HUGO, GO). It allows to perform complex queries with **no need for computational or programming knowledge**.

You can use BioMart to **collect gene information** or gene mapping among different databases in tabular format, or to get gene sequences. 
You can do so **for all genes in a genome** at once, or **for just a subset of them** (such as only genes on one specific region of a chromosome, or genes on one region of a chromosome associated with a given protein domain).

🎥 [Short video from the Ensembl Training channel introducing BioMart](youtube.com/watch?v=QvGT2G0-hYA&feature=youtu.be)


### Core arguments of any BioMart search

- **Mart**: the combination of database (e.g. Ensembl Genes version XX) and dataset (e.g. human genes for genome build GRChYY) to be queried
- **Filters**: define which genes (or entries) you want to retrieve
- **Values**: identifiers to be used along with the filters
- **Attributes**: the fields/columns returned in the results table (or in sequence headers for sequence outputs)


### Where to start with BioMart
- Open [BioMart](https://www.ensembl.org/biomart) in a browser. (Alternatively, go to the Ensembl website and select “BioMart” from the top menu.)
- Follow the BioMart tutorial available among the Ensembl training materials [here](https://grch37.ensembl.org/info/website/tutorials/module5_feb2009_ensembl.pdf):

A new version of the Ensembl database is released approximately every three months, incorporating updated genome annotations. The tutorial above is based on an older Ensembl release (version 52, from 2009). While the overall structure and logic of BioMart remain consistent, some details—such as filter and attribute names—may differ in current releases. You may therefore need to adapt parts of the tutorial to match the latest version of the database.


❓ **A challenge for you**: *How many human genes are annotated as having DNA-binding transcription factor activity (i.e., GO term GO:0003700)* *Find their official gene symbols (HGNC)*
  









**References:**

- [*Gene Ontology representation for transcription factor functions*. Volume 1864, Issues 11–12, November–December 2021, 194752](https://www.sciencedirect.com/science/article/pii/S1874939921000705)
