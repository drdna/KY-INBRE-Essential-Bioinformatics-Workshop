# KY-INBRE-Essential-Bioinformatics-Workshop
Training Materials and Background Information 
## DAY 1
### [Introduction to the Workshop]()
Motivation, goals, and structure
### MODULE 1. Learning to work in the UNIX command line environment
[MODULE1_UNIX Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_1_Unix.pdf).

Here is a handy [Unix Cheat Sheet](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/Unix_Cheat_Sheet.pdf) that includes most of the commands necessary to perform a wide range of bioinformatic data processing tasks.
---
## DAY 2
### MODULE 2. Sequence Quality Assessement and Trimming
We will use [FASTQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/) to analyze sequence quality and visualize in a convenient browser. Poor quality sequence, as well as contaminating adpators, will then be trimmed using [Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic) ([Bolger et al. 2014](https://academic.oup.com/bioinformatics/article/30/15/2114/2390096).

[MODULE2_SEQUENCES Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_2_Sequences.pdf)
### MODULE 3. De Novo Genome Assembly
First we will explore the use of [Velvet Advisor](https://dna.med.monash.edu/~torsten/velvet_advisor/) to identify a starting k-mer value for assembling a bacterial genome. We will then apply [VelvetOptimiser](https://github.com/tseemann/VelvetOptimiser) to generate assemblies over a range of suitable k-mer values using [velvet](https://github.com/dzerbino/velvet) software ([Zerbino & Birney, 2008](https://pmc.ncbi.nlm.nih.gov/articles/PMC2952100/pdf/nihms-234285.pdf); [Zerbino et al. 2010](https://pmc.ncbi.nlm.nih.gov/articles/PMC2952100/pdf/nihms-234285.pdf))and report on the k-value (as well as other parameters) that produce an "optimal" genome.

[MODULE3_GENOME_ASSEMBLY Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_3_Assembly.pdf)

We will then learn how to use [Bandage](https://academic.oup.com/bioinformatics/article/31/20/3350/196114) to explore genome assembly graphs to gain insights into connectivity between genomic contigs that are not accessible from the genome assembly itself.
---
## DAY 3
### MODULE 4. Sequence Comparison using Local BLAST
Most participants will be familiar with using [BLAST]([Altshul et al. 1990](https://www.sciencedirect.com/science/article/pii/S0022283605803602?via%3Dihub); Camacho et al. 2009](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-10-421)) to search for sequence similarities by using NCBI's [BLAST web portal](https://blast.ncbi.nlm.nih.gov/Blast.cgi). We will first (re)familiarize ourselves with the search caoabilities of the online service. Then, we will learn how to perform BLAST searches on a local computer, which allows querying of both remote and local sequence databases.

[MODULE4_BLAST Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_4_BLAST.pdf)
### MODULE 5. De Novo Gene Prediction
[MODULE5_GENE_PREDICTION Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_5_Gene_Prediction.pdf)
---
## DAY 4
### MODULE 6. Transcript Assembly and Differential Gene Expression Analysis
[MODULE6_RNASEQ Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_6_RNAseq.pdf)
### MODULE 7. Identifying Genetic Variants
[MODULE7_VARIANT_CALLING Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_7_Variant_Calling.pdf)
### MODULE 8. Visualizing data in a Genome Browser
[MODULE8_IGV Training Manual](https://github.com/actapia/uky-ngs-workshop-user-install/blob/main/docs/nocopy/Module_8_IGV.pdf)
