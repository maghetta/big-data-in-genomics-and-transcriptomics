---
title: Modulo 4
---

![modulo4](images/modulo4/modulo4.jpg)

<br>

## Topics

Exploring the UCSC Genome Browser and Associated Tools



## Learning objectives

By the end of this activity, you should be able to:

    Retrieve the HGNC symbol for a given human gene
    Retrieve a list of all human genes annotated with a given GO (Gene Ontology) term
    Describe the scope of a differential expression analysis
    Describe the scope of a functional enrichment analysis
    Identify differentially expressed genes in the GSE8671 dataset
    Retrieve enriched functional annotations for a gene list of interest using the gProfiler webtool





## UCSC and the Birth of the Genome Browser

The University of California, Santa Cruz (UCSC) Genome Browser was developed by graduate student Jim Kent, and its development is intertwined with the final and crucial steps of the Human Genome Project.
The first version of this graphical tool, designed to navigate the newly released draft of the human genome, was published on July 7, 2000.

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo4/jimkent.png" width="800"> <br>
  <em> A still from a short video on the history of the UCSC Genome Browser and its role in the Human Genome Project, available <a href="https://youtu.be/_6caCfvMIiY?si=pmTY4fWuTc1i1nmV">here: https://youtu.be/_6caCfvMIiY?si=pmTY4fWuTc1i1nmV</a>
</div>
<br>


## Navigating Genomic Information: the UCSC Genome Browser



## Tools at the UCSC Genome Browser: BLAT, Table Browser, Custom Tracks, In-Silico PCR, LiftOver 


```
# Installazione del pacchetto dplyr (da eseguire una sola volta)
install.packages("dplyr")
Caricamento del Pacchetto
Una volta installato, puoi caricare il pacchetto dplyr utilizzando library().
```
mtcars_sorted <- arrange(mtcars, desc(hp))
head(mtcars_sorted)
```
