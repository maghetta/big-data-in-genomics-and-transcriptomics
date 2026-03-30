---
title: Modulo 4
---

![modulo4](images/modulo4/modulo4.jpg)

<br>

## Topics

Exploring the UCSC Genome Browser and Associated Tools



## Learning objectives

By the end of this activity, you should be able to:

    - Visualize a genomic locus in the UCSC Genome Browser and identify key genomic features (e.g., genes, exons, regulatory elements)
    - Customize the genomic view by selecting desired annotation tracks (e.g. variation, genes annotated by GENCODE) and deselecting unwanted ones (e.g.  
    - Map an unknown DNA sequence to a reference genome using a genome browser and interpret its genomic context (e.g., gene location, nearby features)
    - Load and visualize a custom track of genomic intervals in the UCSC Genome Browser
    - Assemble a custom BED file for selected genomic features of interest




## UCSC and the Birth of the Genome Browser

The University of California, Santa Cruz (UCSC) Genome Browser was developed by graduate student Jim Kent, and its development is intertwined with the final and crucial steps of the Human Genome Project.
The first version of this graphical tool, designed to navigate the newly released draft of the human genome, was published on July 7, 2000.

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo4/jimkent.png" width="800"> <br>
  <em> A still from a short video on the history of the UCSC Genome Browser and its role in the Human Genome Project, available <a href="https://youtu.be/_6caCfvMIiY?si=pmTY4fWuTc1i1nmV">here.</a><em> 
</div><br><br><br>


## Navigating Genomic Information: the UCSC Genome Browser


<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo4/ucsc1.png" width="800"> <br>
  <em> Access the UCSC Genome Browser data portal <a href="https://genome.ucsc.edu">here.</a><em> 
</div><br><br><br>


## Core Tools at UCSC:

- **Genome Browser**: The main visualization tool that displays any portion of a genome at any scale with aligned annotation tracks showing genes, regulatory elements, conservation, variants, and other genomic features.<br>

- **BLAT (BLAST-Like Alignment Tool)**: A rapid sequence alignment tool developed by Jim Kent for finding sequence matches in genomes. Faster than BLAST for closely related sequences and useful for locating mRNA/EST alignments.<br>

- **LiftOver**: A tool for converting genomic coordinates between different genome assemblies (e.g., hg19 to hg38). Requires chain files that map regions between assemblies.<br>

- **In-Silico PCR**: A tool for virtually testing PCR primer pairs against a genome to verify specificity and predict amplicon locations.<br>

- **Table Browser**: A web interface for querying, filtering, and downloading data from the underlying MySQL databases. Allows intersection of data tables and export in multiple formats. See below for more related terms, or our documentation.<br><br><br>



### **Genome Browser**
See an overview of the Genome Browser interface, highlighting its layout, navigation, and key functional elements at [this link](.



<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo4/Screenshot from 2026-03-30 11-11-29.png" width="800"> <br>
</div><br><br><br>

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo4/Screenshot from 2026-03-30 10-59-59.png" width="800"> <br>
</div><br><br><br>

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo4/Screenshot from 2026-03-30 11-00-08.png" width="800"> <br>
</div><br><br><br>

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo4/Screenshot from 2026-03-30 11-00-44.png" width="800"> <br>
</div><br><br><br>

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo4/Screenshot from 2026-03-30 11-01-02.png" width="800"> <br>
</div><br><br><br>

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo4/Screenshot from 2026-03-30 11-01-24.png" width="800"> <br>
</div><br><br><br>

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo4/Screenshot from 2026-03-30 11-01-58.png" width="800"> <br>
</div><br><br><br>

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo4/Screenshot from 2026-03-30 11-02-25.png" width="800"> <br>
</div><br><br><br>

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo4/Screenshot from 2026-03-30 11-02-39.png" width="800"> <br>
</div><br><br><br>

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo4/Screenshot from 2026-03-30 11-03-02.png" width="800"> <br>
</div><br><br><br>


## How to: find sequence matches to the genome (BLAT) and create and upload a custom BED file to the UCSC Genome Browser<br><br>
See [here](https://sites.google.com/uniroma1.it/laboratorio-di-bioinformatica/moduli-tematici/modulo-4)<br><br>


**References**<br><br>

- **UCSC Genome Browser – video tutorials and training materials** <a href="https://genome.ucsc.edu/training/">https://genome.ucsc.edu/training/</a>

