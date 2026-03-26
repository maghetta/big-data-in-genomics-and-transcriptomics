---
title:
---

![modulo2](images/modulo2/modulo2.jpg)

<br>

## Argomenti

- Common *omics* data formats
<hr>

## Obiettivi conoscitivi

Al termine di questa attività dovresti essere in grado di:

- Descrivere le caratteristiche e gli scopi dei principali formati di dati omici (es. FASTQ, GTF/GFF e BED)


### Standard formats for *omics* data
In genomics and transcriptomics, **standard data formats** are essential for ensuring interoperability between tools, reproducibility of analyses, and ease of data sharing. Many types of omics data are stored in **simple text-based formats**, which are widely supported and human-readable. For example, nucleotide sequences are often stored in [**FASTA**](https://en.wikipedia.org/wiki/FASTA_format) or [**FASTQ**](https://en.wikipedia.org/wiki/FASTQ_format) files, genomic intervals in **BED**, and gene annotations in specialized formats such as **GFF/GTF** files. Using standardized formats allows researchers to efficiently analyze, visualize, and integrate diverse datasets.


<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo2/omics_data_formats.png" width="600">
</div><br><br>



> ❓ **Challenge question**: *How many sequences would you expect to find in a FASTA file containing the human genome? Why?*<br><br>
> ❓ **Challenge question**: *Knowing the size of the human genome and assuming ~1 byte per character, what is the expected size of a FASTA file containing the entire genome?*


**A small FASTQ file to play with**<br>
This is a microbiome sample from [Jacques et al. 2021](https://doi.org/10.24918/cs.2021.17).<br>
<a href="https://zenodo.org/record/3977236/files/female_oral2.fastq-4143.gz" target="_blank">Download gunzipped FASTQ file (]500kb) </a><br><br><br>

> ❓ **Challenge question**:
- Download and unzip the file
- Inspect the uncompressed file from a bash terminal (hint: use *head*, *tail*)
- *How many reads does the file contain?* (hint: use the bash command *wc -l*)

> ❓ **super-challenging question**:
- Download and install the [FASTQC software](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/) on your PC (see the instructions after clicking *Download Now*)
- Launch the FastQC application
- Load the FASTQ file you previously downloaded (select *File* > *Open*. You can then select the files you want to analyse.)
- Run the quality control analysis
- Evaluate results (see [here](https://hbctraining.github.io/Intro-to-rnaseq-hpc-salmon/lessons/qc_fastqc_assessment.html))

  
<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo2/sam_bam.png" width="600">
</div><br><br>
(see the instructions after clicking Download Now)


<br>
<a href="images/modulo2/17_22.pdf" target="_blank">Open PDF</a><br><br><br>

