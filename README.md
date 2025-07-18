# KY-INBRE-Essential-Bioinformatics-Workshop
## Training Materials and Background Information 
<details>
<summary><strong>DAY 1</strong></summary>

## PRE-WORKSHOP SURVEY
Please complete the following [Pre-workshop survey](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.google.com%2Fforms%2Fd%2Fe%2F1FAIpQLSc9Wg7b1Vzz-D5bdjEmG955jCwQiMDIelXFvC1YcpiwVC0oWA%2Fviewform%3Fusp%3Dsharing%26ouid%3D111233545817712152156&data=05%7C02%7Cmark.farman%40uky.edu%7C849cb2881507477b935a08ddc3a50579%7C2b30530b69b64457b818481cb53d42ae%7C0%7C0%7C638881835727713398%7CUnknown%7CTWFpbGZsb3d8eyJFbXB0eU1hcGkiOnRydWUsIlYiOiIwLjAuMDAwMCIsIlAiOiJXaW4zMiIsIkFOIjoiTWFpbCIsIldUIjoyfQ%3D%3D%7C0%7C%7C%7C&sdata=aamCFEEiN4fbHdCG8aowh%2FR9Mzppqt2xOHN1ijRaVnY%3D&reserved=0) which seeks information about your academic background, your familiarity with bioinformatics, and motivation for attending the workshop.

### Presentation 1. [Introduction to the Workshop](/LECTURES/Presentation1_Intro.pptx)
Motivation, goals, and workshop structure.
### MODULE 1. Learning to work in the UNIX command line environment
[MODULE1_UNIX Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_1_Unix.pdf).

Here is a handy [Unix Cheat Sheet](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/Unix_Cheat_Sheet.pdf) that includes most of the commands necessary to perform a wide range of bioinformatic data processing tasks.
</details>

---

<details>
<summary><strong>DAY 2</strong></summary>

### MODULE 2. Sequence Quality Assessement and Trimming

### Presentation 2. [Sequence Data: Acquisition and Processing](/LECTURES/Presentation2_Sequences.pptx)

### Activities
We will use [FASTQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/) to analyze sequence quality and visualize in a convenient browser. Poor quality sequence, as well as contaminating adaptors, will then be trimmed using [Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic) ([Bolger et al. 2014](https://academic.oup.com/bioinformatics/article/30/15/2114/2390096). 

#### Resources
[MODULE2_SEQUENCES Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_2_Sequences.pdf).

Link to [Illumina Cycle Sequencing Video](https://www.youtube.com/watch?v=fCd6B5HRaZ8).

Link to [ASCII Table](https://i0.wp.com/pediaa.com/wp-content/uploads/2018/08/Difference-Between-ASCII-and-EBCDIC_Figure-1.png?resize=600%2C500).

---

### MODULE 3. De Novo Genome Assembly

### Presentation 3. [Genome Assembly](/LECTURES/Presentation3_Assembly.pptx)

### Activities
First we will explore the use of [Velvet Advisor](https://dna.med.monash.edu/~torsten/velvet_advisor/) to identify a starting k-mer value for assembling a bacterial genome. We will then apply [VelvetOptimiser](https://github.com/tseemann/VelvetOptimiser) to generate assemblies over a range of suitable k-mer values using [velvet](https://github.com/dzerbino/velvet) software ([Zerbino & Birney, 2008](https://pmc.ncbi.nlm.nih.gov/articles/PMC2952100/pdf/nihms-234285.pdf); [Zerbino et al. 2010](https://pmc.ncbi.nlm.nih.gov/articles/PMC2952100/pdf/nihms-234285.pdf)). VelvetOptimiser will report the k-value (as well as other parameters) that produced the "optimal" genome assembly (depending on the criteria we set).

We will then learn how to use [Bandage](http://rrwick.github.io/Bandage/) ([Wick et al. 2015](https://academic.oup.com/bioinformatics/article/31/20/3350/196114)) to explore genome assembly graphs to gain insights into connectivity between genomic contigs that are not accessible from the genome assembly itself.

#### Resources
[MODULE3_GENOME_ASSEMBLY Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_3_Assembly.pdf).

</details>

---

<details>
<summary><strong>DAY 3</strong></summary>

### MODULE 4. Sequence Comparison using Local BLAST

### Presentation 4. [BLAST](/LECTURES/Presentation4_BLAST.pptx)

#### Activities
Most participants will be familiar with using [BLAST]([Altshul et al. 1990](https://www.sciencedirect.com/science/article/pii/S0022283605803602?via%3Dihub); [ Camacho et al. 2009](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-10-421)) to search for sequence similarities by using NCBI's [BLAST web portal](https://blast.ncbi.nlm.nih.gov/Blast.cgi). We will first (re)familiarize ourselves with the search capabilities of the online service. Then, we will learn how to perform BLAST searches on a local computer, which allows querying of both remote and local sequence databases.

#### Resources

[MODULE4_BLAST Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_4_BLAST.pdf)

Link to the [NCBI BLAST manual](https://www.ncbi.nlm.nih.gov/books/NBK569839/) that explains all available options.

---

### MODULE 5. _De Novo_ Gene Prediction

### Presentation 5. [GENE PREDICTION](/LECTURES/Presentation5_Gene_Prediction.pptx)

### Activities
Here, we will use an existing genome annotation for one strain (FH) of the fungus, _Pyricularia oryzae_ to generate a training set for predicting genes in a second strain (70-15). This training set will be used to generate gene predictions using two software programs, [SNAP](https://github.com/KorfLab/SNAP) ([Korf, 2014](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-5-59)) and [AUGUSTUS](https://github.com/Gaius-Augustus/Augustus) ([Stanke et al. 2006](https://academic.oup.com/nar/article/34/suppl_2/W435/2505582)). Lastly, we will integrate the two gene predictions along with supporting evidence - including BLAST matches to known proteins and RNASeq data - using a program called [MAKER](https://www.yandell-lab.org/software/maker.html) ([Cantarel et al. 2008](https://genome.cshlp.org/content/18/1/188)), which produces a consensus set of gene models.

#### Resources

[MODULE5_GENE_PREDICTION Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_5_Gene_Prediction.pdf)
</details>

---

<details>
<summary><strong>DAY 4</strong></summary>
<br>

### MODULES 6 & 7. RNASeq and Variant Calling
### Presentation 6. [RNASeq and Variant Calling](/LECTURES/Presentation6_RNAseq_Variants.pptx)

### Activities
#### Transcript Assembly
Our goal is to perform a reference-guided transcript assembly for _Pyricularia oryzae_. First, we will use [HISAT2](http://daehwankimlab.github.io/hisat2/) ([Siren et al, 2014](https://dl.acm.org/doi/10.1109/TCBB.2013.2297101)) to align RNASeq reads from two strains (70-15 and FR13) to the 70-15 reference assembly. We will then use [Stringtie] (https://github.com/skovaka/stringtie2) ([Pertea et al. 2016](https://www.nature.com/articles/nprot.2016.095)) to assemble transcripts for each of the individual datasets, using the 70-15 reference annotation as a guide. Next, we'll employ the _stringtie merge_ function to merge the individual transcript assemblies into a single, comprehensive set of transcript models.

---

#### Differential Expression Analysis
Once we have generated a comprehensive genome annotatation, we will use it to compare expression levels of the constituent transcripts between _P. oryzae_ colonies growing in liquid culture versus those growing inside rice plants. Typically, the results from Stringtie are analyzed using the [Ballgown](https://git.bioconductor.org/packages/ballgown) ([Frazee et al. 2016](https://pmc.ncbi.nlm.nih.gov/articles/PMC4792117/)) package. However, we could spend a whole day (or more) learning how to work in R. For this reason, we will use the legacy program [cuffdiff](http://cole-trapnell-lab.github.io/cufflinks/cuffdiff/) ([Trapnell et al. 2013](https://pmc.ncbi.nlm.nih.gov/articles/PMC3334321/)), which can be run entirely on the command line and generates a simple, tabular output.

---

#### The Integrated Genomics Viewer
Over the past two daya we have generated a large number of output files: gene predictions, transcript assemblies, RNASeq read alignments, and variant calls. Although we have learned how to query the outputs using the command line, the large volumes of data and the limits of the tabular format makes it hard to conceptualize how these various features are related and are organized. Fortunately, we can visualize and explore the datasets altogether in a graphical "genome browser" that lays out features according to their chromosomal positions. For this exercise, we will use the [Integrated Genomics Viewer (IGV)](https://igv.org) ([Robinson et al. 2011](http://www.nature.com/nbt/journal/v29/n1/abs/nbt.1754.html)) - a free browser that is easy to install and easy to use.

---

## POST-WORKSHOP SURVEY
Please complete the following [Post-workshop survey](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.google.com%2Fforms%2Fd%2Fe%2F1FAIpQLSd8bn31TzFz9-_AezSgmSAPCjdVDJVySRzNLKJYpYx7GE3QTg%2Fviewform%3Fusp%3Dsharing%26ouid%3D111233545817712152156&data=05%7C02%7Cmark.farman%40uky.edu%7C849cb2881507477b935a08ddc3a50579%7C2b30530b69b64457b818481cb53d42ae%7C0%7C0%7C638881835727753645%7CUnknown%7CTWFpbGZsb3d8eyJFbXB0eU1hcGkiOnRydWUsIlYiOiIwLjAuMDAwMCIsIlAiOiJXaW4zMiIsIkFOIjoiTWFpbCIsIldUIjoyfQ%3D%3D%7C0%7C%7C%7C&sdata=7H2GsgXHTGfmtM5X%2FUXZn%2BsZLyMgq7b48ilbuGs4RMw%3D&reserved=0) to let us know how much your understanding of the command line and Bioinformatics Data Analysis has improved after attending the workshop.

---

### Resources

### MODULE 6. Transcript Assembly and Differential Gene Expression Analysis
[MODULE6_RNASEQ Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_6_RNAseq.pdf)

### MODULE 7. Identifying Genetic Variants
[MODULE7_VARIANT_CALLING Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_7_Variant_Calling.pdf)

### MODULE 8. Visualizing data in a Genome Browser
[MODULE8_IGV Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_8_IGV.pdf)

The [General Feature Format](https://gmod.org/wiki/GFF3)

The [SAM/BAM Alignment Format](https://samtools.github.io/hts-specs/SAMv1.pdf)

The [Variant Call Format](https://samtools.github.io/hts-specs/SAMv1.pdf)

[Ballgown Manual] (https://www.bioconductor.org/packages/devel/bioc/manuals/ballgown/man/ballgown.pdf)

</details>



---

Link to GitHub page with instructions for [Workshop Installation](https://github.com/actapia/uky-ngs-workshop-user-install).
