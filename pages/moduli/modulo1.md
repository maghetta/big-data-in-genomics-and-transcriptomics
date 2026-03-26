---
title:
---

![modulo1](images/modulo1/modulo1.jpg)

<br>

## Topics

- High-Throughput Sequencing (HTS) technologies
- Generations of sequencing technologies
- The sequencing-by-synthesis approach
- Typical data analysis workflow

<br>
<br>

## Learning Objectives

By the end of this activity, you should be able to:
<br>
- Describe the principles of the “sequencing-by-synthesis” process
- Describe genomic sequencing using Illumina technology
- Outline the main features that distinguish first-, second- (“Next Generation Sequencing”), and third-generation sequencing technologies
- Describe the scope of mapping sequencing reads to the reference genome
- Explain why the use of paired-end sequencing for miRNA sequencing represents a poor experimental choice
- Explain how Phred scores reflect the quality of a sequencing read
- List at least three common applications of high-throughput sequencing in biomedical research
  

<br>

<br>

## High-Throughput Sequencing (HTS) technologies a historical overview

<br>

### 👉 “You are here”
<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/ANSA_19.10.2025.png" width="600">
</div><br><br><br>


### 👉 The turning point: where everything changed
<br>
**The Human Genome Project (HPG): 1990-2003**<br>
<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/June26.2000.Monday.png" width="600">
</div><br><br>

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/hpg_infographic.png" width="600">
</div><br><br>


<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/hpg_parimerito.png" width="400">
</div><br><br><br>

- [The White House announcement of the first draft of the human genome](https://clintonwhitehouse4.archives.gov/WH/Work/062600.html)<br>
- [A narrative history of the HGP (video in italiano intitolato "Storia di una rivoluzione: sequenza del genoma svelata"](https://outreach.cnr.it/risorsa/112/approfondimenti-su-biotecnologie-e-genoma-umano)
<br><br><br>


> ❓ **A question for you**: *What fraction of the human genome was considered “junk DNA” until about 20 years ago?* <br>

<ol type="a">
 <li>~10%</li>
 <li>~50%</li>
 <li>~100%</li>
</ol>



> ❓ **Challenge question**: *How many genes are currently annotated in the human genome? How many transcripts? Is the total number of transcripts less than, greater than, or equal to the number of genes? Why?* <br>
>
> **Hint**: To answer these questions, visit the **GENCODE** website (just *Google* it), go to the **Human** section, and check the **Statistics** page.


**Further points for reflection:** <br>
<ul>
  <li> The importance of noting and recording the version of any resource queried (<em>Which version of the GENCODE database do the statistics refer to?</em>). </li>
  <li> The sequence data in the major global repositories (GenBank at NCBI, ENA – European Nucleotide Archive, DDBJ – DNA Data Bank of Japan) are daily synchronized. (<em>What is the current version of the human genome assembly listed in the <a href="https://www.ncbi.nlm.nih.gov/datasets/genome/">NCBI Genome database</a>?</em>; <em>Does it matches the genome assembly listed for human on the <a href="https://www.ensembl.org/index.html">EMBL-EBI Ensembl database?</a></em>)</li>
  <li> Gene annotations curated by each major repository (e.g., NCBI, EMBL-EBI) may differ due to differences in bioinformatic prediction pipelines and the stringency applied to annotations supported by experimental evidence (e.g., <a href="https://www.ncbi.nlm.nih.gov/refseq/">RefSeq</a> vs. <a href="https://www.ncbi.nlm.nih.gov/genbank/">GenBank</a>; <a href="https://vega.archive.ensembl.org/index.html">Vega</a> vs. <a href="https://www.ensembl.org/index.html">Ensembl</a>). (<em>Do the <a href="https://www.ensembl.org/Homo_sapiens/Info/Annotation">EMBL‑EBI Vega database</a> and the <a href="https://www.ncbi.nlm.nih.gov/refseq/annotation_euk/Homo_sapiens/GCF_009914755.1‑RS_2025_08/">NCBI RefSeq</a> list the same number of annotated human genes?</em>; <em>Do these counts match the GENCODE annotated genes?</em>)</li>
<br><br><br>
</ul>

### 👉 The omics revolution: a flood of sequencing data

<br>
<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/UnMilioneDiVolteMenoCaro.png" width="600">
</div><br><br><br>





### 👉 NGS technologies driving the flood of sequencing data
<br>
<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/cost_X_humanGenome_and_technologies.png" width="800"> <br>
  <em>Image credits.(Left)<a href="https://www.genome.gov/about-genomics/fact-sheets/Sequencing-Human-Genome-cost"> NIH-NHGRI - The Cost of Sequencing a Human Genome</a>; (right) <a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC4494749/">Mol Cell. 2015 May 21</a></em>
</div>
<br>

<a href="https://www.nature.com/articles/507294a#citeas">Check Hayden, E. Technology: The $1,000 genome. Nature 507, 294–295 (2014). https://doi.org/10.1038/507294a</a> <br>
<a href="https://www.mdpi.com/2079-7737/12/7/997">At the following link, table 1 lists the different generations of sequencing technologies, along with their key characteristics.</a> <br><br><br>



👉 **Take-Home Message (so far):** <br>
<ul>
  <li>In the aftermath of the Human Genome Project, a major push toward the development of high-throughput sequencing technologies - driven largely by U.S. government funding initiatives such as the $1,000 Genome Project - led to a dramatic reduction in sequencing costs and an exponential growth in <em>omics</em> data available to the scientific community.</li>
 <li>Sequencing the human genome led to a reassessment of the number of protein-coding genes and, for the first time, revealed the existence of tens of thousands of non-protein-coding genes.</li>
 <li>The sequencing data produced served as the foundation for databases that collect and organize this information. In the world of biomedical databases, two primary portals stand out: the <a href="https://www.ncbi.nlm.nih.gov/">NIH-NCBI (USA)</a> and the <a href="https://www.ebi.ac.uk/">EMBL-EBI (EU)</a>. Each hosts multiple databases dedicated to primary genome sequences and covers all types of annotations, including genes, proteins, regulatory sequences, clinical variants, disease associations, and experimental data contributed by individual researchers and large consortia. These portals also provide supporting resources, such as analytical tools and extensive documentation (more on this in the next lessons).</li>
</ul>

<hr style="border: 1px solid gray; width: 50%;"><br><br><br>



## Generations of sequencing technologies

👉 **The first generation:**

Walter Gilbert and Frederick Sanger shared the 1980 Nobel Prize in Chemistry for developing the first-generation DNA sequencing methods. <br><br>

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/sanger_maxgil.png" width="800">
  <em>Image credits.<a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC4727787/"> Genomics. 2016 Jan;107(1):1–8.</a>. First-generation DNA sequencing technologies. Example DNA to be sequenced (a) is illustrated undergoing either Sanger (b) or Maxam–Gilbert (c) sequencing. (d): Fragments generated from either methodology can then be visualized via electrophoresis on a high-resolution polyacrylamide gel: sequences are then inferred by reading ‘up’ the gel, as the shorter DNA fragments migrate fastest. </em>
</div><br><br><br>


<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/sanger_seq.png" width="650">
  <em>Image credits.<a href="https://www.instagram.com/p/CVi1JH5B-xM/">Applied Biological Materials (abm), Instagram post, Oct. 27, 2021.</a></em>
</div><br><br><br>

**Sanger sequencing:** <br><br>
How does it work? 🤔It uses a high fidelity DNA-dependent polymerase to generate a complementary copy to a single stranded DNA template.

1️⃣ In each reaction a single primer, complementary to the template, initiates a DNA synthesis reaction from its 3' end. <br>

2️⃣ A, G, T and C di-deoxynucleotides are added in a template-dependent manner one after the other. These di-deoxynucleotides are modified so that they terminate polymerization when incorporated and also fluoresce to allow detection. <br>

3️⃣ After each reaction,  many copies of different-length DNA fragments are generated that are terminated at all of the nucleotide positions of the template molecule by one of the di-deoxynucleotides. <br>

4️⃣The reaction mixtures are loaded on the sequencing machine, either manually onto slab gels or automatically with capillaries, and are electrophoresed to separate the DNA molecules by size. <br>

5️⃣The DNA sequence is read through the fluorescent emission of the di-deoxynucleotide as it flows through the gel. <br><br><br>


**Fun fact:**: With Sanger sequencing, a single reaction could read only **about 400 bases per week**, which made sequencing even a small genome like baker’s yeast a months‑long task!<br><br><br>

> ❓ **A question for you**: *How big is the baker's yeast (Saccharomyces cerevisiae) genome?* <br>
Hint: try to find your answer by querying the NIH-NCBI Genome database. To do so:<br>
1. Open a browser and go to the NIH-NCBI data portal: <a href="https://www.ncbi.nlm.nih.gov/">https://www.ncbi.nlm.nih.gov</a> <br>
2. Select the Genome database from the drop-down menu on the left side of the search box <br>
3. Enter a relevant keyword to access the baker's yeast (Saccharomyces cerevisiae) genome <br>
4. Click the search button.  <br><br><br>



> ❓ **A question for you**: *What happens if you place a DNA molecule in an electric field, what will it do, and why?* <br>
<ol type="a">
 <li>nothing</li>
 <li>migrate towards the negative pole</li>
 <li>migrate towards the positive pole</li>
</ol><br><br><br><br>


👉 **The second (*next*) generation:**<br>
</div>
<br>
<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/454_illumina.png" width="600">
</div><br><br><br>



<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/clonal_amplification.png" width="650"> <br>
  <em>Image credits.<a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC4727787/"> Genomics. 2016 Jan;107(1):1–8.</a>. Next-generation DNA sequencing parallelized amplification.(a) 454 sequencing: clonal amplification on beads (emulsion PCR); (b) Illumina/Solexa sequencing: bridge amplification on a flow cell. </em>
</div><br><br><br>


<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/454.png" width="650"> <br>
  <em>Image credits.<a href="https://www.instagram.com/p/CVi1JH5B-xM/">Applied Biological Materials (abm), Instagram post, Oct. 27, 2021.</a></em>
</div><br><br><br>


<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/illumina.png" width="800"> <br>
  <em>Image credits.<a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC4727787/"> Genomics. 2016 Jan;107(1):1–8.</a>. First-generation DNA sequencing technologies. Example DNA to be sequenced (a) is illustrated undergoing either Sanger (b) or Maxam–Gilbert (c) sequencing. (d): Fragments generated from either methodology can then be visualized via electrophoresis on a high-resolution polyacrylamide gel: sequences are then inferred by reading ‘up’ the gel, as the shorter DNA fragments migrate fastest. </em>
</div><br><br><br>

**key features:** massive parallel sequencing; short reads (50-200 bp); hundreds of millions–billions of reads per run <br><br><br>


👉 **The third generation:**

Third-generation sequencing technologies, such as the **Pacific Biosciences (PacBio)** and **Oxford Nanopore Technologies (ONT)**, prioritize read length over read count. Today sequencers can output long reads (typically 10–100 kb) and ultlong reads exceeding 100 kb and extreme cases over 1 Mb. <br><br><br>

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/third_generation.png" width="650"> <br>
  <em>Image credits.<a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC4727787/"> Genomics. 2016 Jan;107(1):1–8.</a>. Third-generation DNA sequencing technologies. (a): Nucleotide detection in a zero-mode waveguide (ZMW), as featured in PacBio sequencers. DNA polymerase molecules are attached to the bottom of each ZMW, and target DNA and fluorescent nucleotides are added. As the diameter is narrower than the excitation light's wavelength, illumination rapidly decays travelling up the ZMW: nucleotides being incorporated during polymerisation at the base of the ZMW provide real-time bursts of fluorescent signal, without undue interference from other labelled dNTPs in solution. (b): Nanopore DNA sequencing as employed in ONT's MinION sequencer. Double stranded DNA gets denatured by a processive enzyme which ratchets one of the strands through a biological nanopore embedded in a synthetic membrane, across which a voltage is applied. As the ssDNA passes through the nanopore the different bases prevent ionic flow in a distinctive manner, allowing the sequence of the molecule to be inferred by monitoring the current at each channel.</em>
</div><br><br><br>

**New possibilities enabled by long-read sequencing** <br><br><br>
The combined use of two third-generation sequencing technologies—specifically, the PacBio HiFi DNA sequencing method, which can read about 20,000 bases with nearly perfect accuracy, and the Oxford Nanopore DNA sequencing method, which can read up to 1 million bases at a time with more modest accuracy — made it possible to obtain the first complete human genome sequence in March 2022. Thanks to the long reads generated by these technologies, the final 8% of the human genome, consisting primarily of highly repetitive sequences that could not be resolved during the Human Genome Project and were long considered unreachable, has now been completed. In total, nearly 200 million bases were added to the human genome in this effort.

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/filling_the_gaps.png" width="700"> <br>
  <em><a href="https://pubmed.ncbi.nlm.nih.gov/35357919/"> Science. 2022 Apr;376(6588):44-53.</a>.</em>
</div><br><br><br>

Long-read sequencing has enabled personalized, haplotype-resolved cancer genomics, supporting allele-specific analyses of mutations, including the confirmation of biallelic inactivation, the detection of allele-specific methylation and expression, and the resolution of complex structural variants.

<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/LRS_in_cancer.png" width="700"> <br>
  <em><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC12047254/"> [...] Genome Res. 2025 Apr;35(4):599–620.</a></em>
</div><br><br><br>


<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/LRS_in_cancer.png" width="700"> <br>
  <em><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC12047254/"> [...] Genome Res. 2025 Apr;35(4):599–620.</a></em>
</div><br><br><br>


**key features:** direct sequencing (no amplification); long reads (up to 30.000 bp)  <br><br><br>

<hr style="border: 1px solid gray; width: 50%;"><br><br><br>



## The sequencing-by-synthesis approach


🎥 <a href="https://www.youtube.com/watch?v=fCd6B5HRaZ8"> Short video illustrating the Illumina sequencing technology <a>




<hr style="border: 1px solid gray; width: 50%;"><br><br><br>

## Typical data analysis workflow: data preprocessing → quality control → analysis → visualization → interpretation


## Quality of sequencing reads: the Phred score
<br>

A **[Phred score (Q score)](https://en.wikipedia.org/wiki/Phred_quality_score)** is a numerical measure of base-calling quality in a sequencing read. 
It represents the probability that a base call is incorrect on a logarithmic scale, as defined by the following formula:

```
Q = -10 log₁₀(P), where P represents the probability of an incorrect base call.

```

For instance: a score of Q20 indicates a 1% error rate (99% accuracy), while Q30 indicates a 0.1% error rate (99.9% accuracy).  <br>
Higher scores indicate greater confidence in the base call. Q30 is generally considered the standard for high-quality. <br>

**Scale**: Scores typically range from 0 to 60+.
- Q10: 1 in 10 error rate (90% accuracy).
- Q20: 1 in 100 error rate (99% accuracy).
- Q30: 1 in 1,000 error rate (99.9% accuracy).
- Q40: 1 in 10,000 error rate (99.99% accuracy).



**Commonly Used Thresholds:** <br>
- less than 20: Poor quality <br>
- betwee 20 and 28: Reasonable quality  <br>
- over 28: Good quality  <br>

<hr style="border: 1px solid gray; width: 50%;"><br><br><br>



<div style="border:1px solid #ccc; padding:10px; display:inline-block;">
  <img src="images/modulo1/Genomics_Transcriptomics_Proteomics_Metabolomics.png" width="700"> <br>
  <em>Image credits.<a href="https://doi.org/10.3390/fermentation4040092"> Pinu, F.R. Fermentation 2018, 4, 92.</a></em>
</div><br><br><br>



### References and resources

- <span style="color:blue;"> A couple of reviews on first-, second-, and third-generation sequencing technologies:</span> <br>
-- [The sequence of sequencers: The history of sequencing DNA. Genomics. 2016 Jan;107(1):1-8. doi: 10.1016/j.ygeno.2015.11.003. Epub 2015 Nov 10. PMID: 26554401; PMCID: PMC4727787.](https://pmc.ncbi.nlm.nih.gov/articles/PMC4727787/) <br>
-- [Slatko BE, Gardner AF, Ausubel FM. Overview of Next-Generation Sequencing Technologies. Curr Protoc Mol Biol. 2018 Apr;122(1):e59. doi: 10.1002/cpmb.59. PMID: 29851291; PMCID: PMC6020069.](https://pmc.ncbi.nlm.nih.gov/articles/PMC6020069/) <br>
-- [Reuter JA, Spacek DV, Snyder MP. High-throughput sequencing technologies. Mol Cell. 2015 May 21;58(4):586-97. doi: 10.1016/j.molcel.2015.05.004. PMID: 26000844; PMCID: PMC4494749.](https://pmc.ncbi.nlm.nih.gov/articles/PMC4494749/) <br>
- <span style="color:blue;">NHGRI resource on the evolution of human genome sequencing costs</span> [https://www.genome.gov/about-genomics/fact-sheets/Sequencing-Human-Genome-cost](https://www.genome.gov/about-genomics/fact-sheets/Sequencing-Human-Genome-cost)
- <span style="color:blue;"> RNA-Seq Data Analysis in Galaxy: [Batut B, van den Beek M, Doyle MA, Soranzo N., Methods Mol Biol. 2021;2284:367-392. doi: 10.1007/978-1-0716-1307-8_20. PMID: 33835453.](https://pubmed.ncbi.nlm.nih.gov/33835453/)</span>
- <span style="color:blue;"> Galaxy Project video documentation and training resources: [official YouTube channel for the Galaxy Project](https://www.youtube.com/@GalaxyProject)</span>

