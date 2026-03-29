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







<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo4/jimkent.png" width="800"> <br>
</div>
<br>




```
# Installazione del pacchetto dplyr (da eseguire una sola volta)
install.packages("dplyr")
Caricamento del Pacchetto
Una volta installato, puoi caricare il pacchetto dplyr utilizzando library().
```
mtcars_sorted <- arrange(mtcars, desc(hp))
head(mtcars_sorted)
```
