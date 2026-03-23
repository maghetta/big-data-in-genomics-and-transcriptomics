---
title:
---

![modulo1](images/modulo1/modulo1.jpg)

<br>

## Topics

- High-Throughput Sequencing (HTS) technologies
- The sequencing-by-synthesis approach
- Common *omics* data formats
- Typical data analysis workflow

<br>
<br>

## Learning Objectives

By the end of this activity, you should be able to:
<br>
- Distinguish between genomics and transcriptomics by defining their objects of study and providing examples of their applications
- Describe the principles of the “sequencing-by-synthesis” process
- Describe genomic sequencing using Illumina technology
- Outline the main features that distinguish first-, second- (“Next Generation Sequencing”), and third-generation sequencing technologies
- Describe the scope of mapping sequencing reads to the reference genome
- Explain why the FASTQ data format is preferred for storing HTS raw data compared to FASTA
- Explain the minimum information required to define a genomic coordinate
- List at least three common applications of high-throughput sequencing in biomedical research
  

<br>

<br>

## High-throughput sequencing technologies (HTS): a historical overview, basic principles, sequencing generations, and common applications

<br>

### 👉 “You are here”
<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/ANSA_19.10.2025.png" width="600">
</div>
___


### 👉 The turning point: where everything changed
<br>
**The Human Genome Project (HPG): 1990-2003**<br>
<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/June26.2000.Monday.png" width="600">
</div>

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/hpg_infographic.png" width="600">
</div>


<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/hpg_parimerito.png" width="600">
</div>

- [The White House announcement of the first draft of the human genome](https://clintonwhitehouse4.archives.gov/WH/Work/062600.html)<br>
- [A narrative history of the HGP (video in italiano intitolato "Storia di una rivoluzione: sequenza del genoma svelata"](https://outreach.cnr.it/risorsa/112/approfondimenti-su-biotecnologie-e-genoma-umano)
<br>


> ❓ **A question for you**: *What fraction of the human genome was considered “junk DNA” until about 20 years ago?* <br>

>> a. ~10%  <br>
>> b. ~50% <br>
>> c. ~100% <br>




> ❓ **Challenge question**: *How many genes are currently annotated in the human genome? How many transcripts?* <br>
>
> **Hint**: To answer these questions, visit the **GENCODE** website (just *Google* it), go to the **Human** section, and check the **Statistics** page.

___


### 👉 The omics revolution: a flood of sequencing data
<br>
<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/UnMilioneDiVolteMenoCaro.png" width="600">
</div>


___


### 👉 NGS technologies driving the flood of sequencing data
<br>
<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/cost_X_humanGenome_and_technologies.png" width="800"> <br>
  <em>Image credits.(Left)<a href="https://www.genome.gov/about-genomics/fact-sheets/Sequencing-Human-Genome-cost"> NIH-NHGRI - The Cost of Sequencing a Human Genome</a>; (right) <a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC4494749/">Mol Cell. 2015 May 21</a></em>
</div>
<br>
<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/NGS_technologies.png" width="600">
</div>
<br>

[Check Hayden, E. Technology: The $1,000 genome. Nature 507, 294–295 (2014). https://doi.org/10.1038/507294a](https://www.nature.com/articles/507294a#citeas)

[At the following link, table 1 lists the different generations of sequencing technologies, along with their key characteristics.](https://www.mdpi.com/2079-7737/12/7/997)<br>


___

👉 **Take-Home Message (so far):** <br>
In the aftermath of the Human Genome Project, a major push toward the development of high-throughput sequencing technologies - driven largely by U.S. government funding initiatives such as the $1,000 Genome Project - led to a dramatic reduction in sequencing costs and an exponential growth in *omics* data available to the scientific community.
Sequencing the human genome led to a reassessment of the number of protein-coding genes and, for the first time, revealed the existence of tens of thousands of non-protein-coding genes.

___

## Typical data analysis workflow: data preprocessing → quality control → analysis → visualization → interpretation

___

## Svolgimento tutorial in R: "Introduzione alla Console R"
<br>

## Svolgimento tutorial in R: "Vettori in R"
<br>

## Svolgimento tutorial in R: "Fattori in R"
<br>



### References and resources

- <span style="color:blue;"> A couple of reviews on first-, second-, and third-generation sequencing technologies:</span> <br>
-- [The sequence of sequencers: The history of sequencing DNA. Genomics. 2016 Jan;107(1):1-8. doi: 10.1016/j.ygeno.2015.11.003. Epub 2015 Nov 10. PMID: 26554401; PMCID: PMC4727787.](https://pmc.ncbi.nlm.nih.gov/articles/PMC4727787/) <br>
-- [Slatko BE, Gardner AF, Ausubel FM. Overview of Next-Generation Sequencing Technologies. Curr Protoc Mol Biol. 2018 Apr;122(1):e59. doi: 10.1002/cpmb.59. PMID: 29851291; PMCID: PMC6020069.](https://pmc.ncbi.nlm.nih.gov/articles/PMC6020069/) <br>
- <span style="color:blue;">NHGRI resource on the evolution of human genome sequencing costs</span> [https://www.genome.gov/about-genomics/fact-sheets/Sequencing-Human-Genome-cost](https://www.genome.gov/about-genomics/fact-sheets/Sequencing-Human-Genome-cost)
-- [Reuter JA, Spacek DV, Snyder MP. High-throughput sequencing technologies. Mol Cell. 2015 May 21;58(4):586-97. doi: 10.1016/j.molcel.2015.05.004. PMID: 26000844; PMCID: PMC4494749.](https://pmc.ncbi.nlm.nih.gov/articles/PMC4494749/) <br>
- <span style="color:blue;"> RNA-Seq Data Analysis in Galaxy: [Batut B, van den Beek M, Doyle MA, Soranzo N., Methods Mol Biol. 2021;2284:367-392. doi: 10.1007/978-1-0716-1307-8_20. PMID: 33835453.](https://pubmed.ncbi.nlm.nih.gov/33835453/)</span>
- <span style="color:blue;"> Galaxy Project video documentation and training resources: [official YouTube channel for the Galaxy Project](https://www.youtube.com/@GalaxyProject)</span>

