<img src="https://i.imgur.com/UHs2ojK.png" width=300px/>

## Overview
In examining the diversity of life, we're often directed to the sequence of an organism's DNA as the source of variation. Differences in these genomes are directly correlated with changes in genetic products, regulatory affects, and molecular interactions--all of which contribute to the great phenotypic variety observed in our world.

However, in this paper, we wish to look beyond the genome. Instead, we introduce the topic of epigenomics, the analysis of gene expression that is not attributable to mutations to the DNA sequence of a genome. Rather, epigenetic expression alteration is caused by biochemical interactions with various proteins and other compounds.

We will breifly describe the biology of the two most well-known epigenomic modifications: [DNA Methylation](#Biology-DNA-Methylation) and [Histone Modifications](#Biology-Histone-Modifications). Then, we will describe in detail the analytical techniques and technologies used to quantify each epigenomic modification.

## Biology: DNA Methylation
### Please note the DNA Methylation section is incomplete, and more will be added.
### Introduction
The first epigenomic modification was discovered as early as the identification of DNA as the genetic material by Rollin Hotchkiss in 1984: DNA methylation.

DNA Methylation is a process by which methyl group are added to DNA molecules. It's catalyzed by family of DNA methyltransferases (Dnmts), enzymes which can transfer methyl groups from S-adenosyl methionine (SAM) to the fifth carbon of a cytosine residue to form 5-methylcytosine (5mC).

### I. Location of DNA Methylation
The most of the DNA methylation happens on cytosines that precede a guanine nucleotide, which is also called CpG sites. Most of the CpG sites are heavily methylated expected for CpG island. 

In Mammals, region called CpG island is GC- and CpG-rich sequences that are not methylated. The definition of CpG region contains

1. sequence length longer than 200bp.
2. G+C contents is more than 50%.
3. a ratio of observed to expected CpG greater than 0.6.

In human genome, there are around 25,000 CpG islands, 75% of which being less than 850bp long. Around 50% of CpG islands contain transcription starting site. Also, because lots of binding sites of transcription factor are GC rich, CpG islands are considered to enhance binding of transcription factor.

### II. Supporting Protein
The addition of the methyl group is modified in diffrent levels in body with work of protein family called DNA methyltransferases (DNMTs). There are three types of DNMTs including DNMT1, DNMT3a and DNMT3b. Those three DNMTs are required for establishment and keeping the DNA methylation patterns. Another two proteins in DNMT family, DNMT2 and DNMT3L, also doing some related but more specific work in methylation. DNMT3a and 3b works in establish of new or de novo methylation while DNMT1 works to do the maintenance work for already established methylation.

### III. DNA methylation in Cancer
DNA methylation is one of the important driver for the cancer development. In cancer cells, CpG islands are abnormally hypermethylated, which lead to silences of genes including tumor suppressor gene. Also, there are hypomethylation in some oncogenes. Those abnormal methylation would be able to be inherited by daughter cells, which would lead to growth of tumor. Moreover, microRNA expression in tumor cells is also altered a lot from normal cells.

### IV. DNA methylation in Aging
Epigenetic Clock is a major of age from DNA methylation level in human body. There was a longitudinal study with two genetically identical twins, which showed that methylation patterns changed and diverged a lot because of environment even in childhood. Also other studies show that DNA methylation level of some genes, like CD4+ T cells, will change proportionally to the age. DNA methylation is one of the keys to unravel the mystery of aging of human.

## Biology: Histone Modifications
### Introduction
Histones are proteins found in eukaryotic cell nuclei that order DNA into nucleosomes. These components of chromatin are subject to post-translational modifications including methylation, acetylation, phosphorylation, ubiquitylation, and others still being researched. The histone code hypothesis suggests that these modifications to chromatin structure along with epigenetic markers influence the recruitment of proteins responsible for regulating gene expression. Multiple modifications work together simultaneously to regulate and change chromatin state and gene expression.

<img src="/assets/Histone_Background.png" width=450px/>
<i><b>Figure</b> General structure of a DNA-histone complex. The two most common modifications (acetylation) and (methylation) are shown.</i>


### I. Histone Acetylation
Acetylation connects a negative charge acetyl group to lysine residues of the N-terminal histone tails (specifically H3 and H4) by histone acetyltransferase (HAT). By doing so, negatively charged DNA is repelled, causing the chromatin to relax into euchromatin and allow for transcription factors to bind and increase gene expression. Deacetylation by histone deacetylase (HDAC) however condenses chromatin into heterochromatin, therefore deactivating gene activity.

<br />

<img src="/assets/Histone_Acetylation.png" width=450px/>
<i><b>Figure</b> Acetylation of histones, leading to relaxation of DNA into euchromatin. Note the larger regions of exposed DNA open for transcription after acetylation.</i>

### II. Histone Methylation/Demethylation
Unlike histone acetylation, methylation is a post-translational epigenetic modification that does not directly change histone charge or histone-DNA interactions. Instead, a methyl group is added to lysine or arginine residues of histone tails, each impacting transcription differently. Arginine methylation activates transcription and transcriptional activities, while Lysine methylation’s effect depends on the methylation site and length. Methylation of sites such as H3K4, K36, and K79 result in transcriptional activation, while methylation of H3K9, K27, and H4K20 silence gene activity/expression. 

<img src="/assets/Histone_Methylation.png" width=450px/>
<i><b>Figure</b> Histone methylations at various locations. Notice both activation and repression is possible depending on methylation type.</i>

### III. Histone Phosphorylation
Unique from histone methylation and acetylation, histone phosphorylation employs interaction between other histone modifications and binding proteins. Chromatin remodeling happens by attaching a phosphoryl group to histone tails, occuring on all histone core proteins, having distinct effects on each. This process plays a huge role in cell division, transcriptional regulation, and DNA damage repair. 

<img src="/assets/Histone_Phosphorylation.png" width=450px/>
<i><b>Figure</b> One example of histone phosphorylation. Various possible signals caused by this particular phosphorylation are described.</i>

## Analysis Techniques: DNA Methylation
### Background
The goal of DNA Methylation analysis is fairly obvious: we wish to detect what parts of the genome are methylated to identify, confirm, or analyze downregulated regions.

Let's take an example: We have two bacterial samples that should both be expressing a gene that turns them blue. However, one culture appears blue while the other appears white. Given what we've learned, we may hypothesize that, for some reason, the white colony of bacteria have methylated the region containing the gene, thus downregulating it. How can we test this hypothesis?

Indeed, genetic sequencing shows the DNA sequence of both bacteria to be identical, yet the white colony shows little to no transcription of this gene. What we've just mentioned sets the context for DNA methylation analysis: **genetic sequencing is unable to distinguish methylated and non-methylated cytosine**. Therefore, we require other analysis technqiues, one that allows us to differentiate between these two:

### I. Bisulfite Sequencing
#### Overview
Bisulfite sequencing is the most widely-used and popular DNA Methylation analysis technique. The core idea is to convert non-methylated cytosine into uracil, but keep methylated cytosine unchanged. Then, run a sequencing analysis. The converted cytosine (now uracil) will be detected during sequencing as thymine, so every detected cytosine will be a methylated cytosine, giving a clear indication of which regions are methylated.

![Bisulfite Conversion](assets/Bisulfite_Conversion.png)  
<i><b>Figure</b> The conversion of non-methylated cytosine into uracil, which are read as thymines by sequencing technology. Notice that methylated cytosine are unchanged and remain sequenced as cytosines.</i>

#### Lab Technique
The first milestone in a bisulfite sequencing analysis is the treatment of DNA with [bisulfite](https://en.wikipedia.org/wiki/Bisulfite). There are three major steps in this protocol:

1. Denaturation of DNA into single strands.
2. Incubation with bisulfite solution at high temperature.
3. Cleaning of DNA; removal of bisulfite and residues

The product of this will be DNA with non-methylated cytosine converted into uracil. Although [whole genome bisulfite sequencing](https://en.wikipedia.org/wiki/Whole_genome_bisulfite_sequencing) (WGBS) is becoming increasingly viable, it is not yet a common method. Thus, we will only describe the lab technique for region-specific analysis. However, we will mention one WGBS analysis method [below](#Bonus---Whole-Genome-Bisulfite-Sequencing-Analysis).

Having used bisulfite to convert all non-methylated cytosine to uracil, the next step is to use a [Polymerase Chain Reaction](https://en.wikipedia.org/wiki/Polymerase_chain_reaction) (PCR) to amplify the region of interest. Traditionally, primers must be selected carefully (such as selecting for low cytosine or non-CpG island rich areas) so potentially converted cytosine do not inhibit PCR amplification. Additionally, in parallel, a PCR for the same region is run on DNA that has *not* been treated with bisulfite.

Both PCR products (bisulfite-treated and native DNA) are cleaned and sequenced using any modern sequencing technique. This yields two digital sequence files:
1. A bisulfite-treated sequence where each cytosine is a methylated cytosine.
2. A native DNA sequence that is true to the original sequence. 

We now move to computational analyses conducted on these data files.

#### Computational Analysis
The simplest analysis possible with these two files is aligning the two sequences, and identifying where there is a C-T mismatch. For example, take the two sequences below:
```
Bisulfite:  GTATCTAT
Native:     GCATCTAC
```

We see the bisulfite sequence identifies the cytosines at positions 2 and 9 as thymines, but the cytosine at position 5 remains a cytosine. We would conclue that the cytosines at positions 2 and 9 were not methylated, while the cytosine at position 2 was.

A related but more interesting analysis than a base-by-base comparison is one that answers, "What areas of this region of interest are methylation-rich?" Tools such as [MethylCoder](https://github.com/brentp/methylcode) provide the answer by aggeregating the results of the base-by-base comparison, determining locales with high aggregate values, and reporting the raw and aggregated results.

#### Bonus - Whole Genome Bisulfite Sequencing Analysis
The quintessential question asked of WGBS is, "What regions of the whole genome are methylation-rich?" Here, the data required for analysis are slightly different than before:

1. Bisulfite sequencing data (FASTQ)
2. Reference genome of interest (FASTA)

Recently developed [EPIC TABSAT](https://tabsat.ait.ac.at/) is one excellent tool for such an analysis. Given these inputs, the following general analysis steps are performed:

1. Quality assessment of raw data
2. Read alignment to reference genome
3. Methylation site analysis and grouping

The tool will then output information about methylation-rich sites, relative methylation level, and more (shown below).

<img src="/assets/WGBS.jpg"/>
<i><b>Figure</b> Summary of various data outputs by EPIC TABSAT (click above for clearer image). Note in particular 1) the lollipop plot that shows % methylation arranged according to samples' accurate chromosomal coordinates and 2) the patternmap showing methylation significance by sample.</i>

### II. HELP Assay
#### Overview
The HpaII tiny fragment Enrichment by Ligation-mediated PCR (HELP) Assay leverages restriction enzyme digestion analysis to determine DNA methylation patterns.

Two restriction enzymes are used:
1. HpaII, which cuts DNA at `CCGA` sites where the inner cytosine is *not* methylated
2. MspI, which cuts DNA at `CCGA` sites regardless of cytosine methlyation

This results in MspI cutting DNA into some number of additional fragments compared to HpaII, and calculating the magnitude of this difference provides a relative measurement of DNA methylation.

<img src="/assets/HELP_Overview.png" width=450px/>
<i><b>Figure</b> Overview of two variations of the HELP assay. Note that overall idea is identical.</i>

#### Lab Technique
Two DNA samples are isolated and, in parallel, subjected to either HpaII or MspI digestion. We assume the HpaII sample has been digested at only `CCGA` sites where the inner cytosine is *not* methylated, resulting in some number of fragments. Additionally, we assume the MspI sample has been digested at all of the sites that HpaII was, but additionally at `CCGA` sites where the inner cytosine *is* methylated.

Each sample is then subjected to ligation-mediated PCR (LM-PCR). This protocol first links fluorescently labeled sequences to every fragment. These sequences are complementary to the PCR primers, so each fragment is amplified without worry of complementarity/primer specificity. This yields a fluorescently detectible pool of DNA which has a quantity relative to the initial number of fragments. Importantly, the HpaII and MspI PCR reactions use different fluorescent labels.

<img src="/assets/LM_PCR.jpg" width=450px/>
<i><b>Figure</b> caption here</i>

Next, a microarray is set up such that it contains binding sites for expected `CCGA` site cuts (determined using reference sequence analysis). Equal amounts of each PCR product is added evenly across the microarray, creating a mosaic of MspI and HpaII bound sequences. The microarray is then scanned twice, once for each type of fluorescent label used. The difference in fluorescence between the two is representative of the methylation level.

#### Computational Analysis
One of the key benefits of this technique is that it's fairly light on dry-lab analysis. Though results are generally more qualitative and inexact, it is a far simpler and easier protocol than bisulfite sequencing.

However, there have been attempts to increase the quantitative power of the assay. A data analysis pipeline in R was developed to take signal intensity data of the microarrays and run various normalizations and to quantify the differences. This pipeline, hoever, is *not* packaged as a tool, but contains a series of computational steps in R that are beyond the scope of this introductory epigenomics lesson. The detailed paper, however, is linked [here](https://academic.oup.com/bioinformatics/article/24/9/1161/207143) for reference.

### Review of DNA Methylation Analysis Techniques
As mentioned before, bisulfite sequencing generally provides more quantifiably solid results than the HELP assay, but also requires greater wetlab and computational power. Indeed, the computational tools for bisulfite sequencing are plentiful, and will generate robust analyses. However, the HELP assay provides a great low-effort alternative for determining DNA methylation levels in a generic context.

From a broader perspective, a recurring limitation of DNA methylation analysis is that any given result is only a snapshot of a single cell at a given point in time. This means repeating an experiment on the same organism may yield vastly different results given that a different cell in a different point in time is used. 

A better method would be one that uses continual measurement of methylation instead of endpoint analysis; this way, we may get a better glimpse into the dynamic mechanisms of true genomic methylation. Such tools and techniques are being developed and implemented today.

## Analysis Techniques: Histone Modifications
### Background
More to come--researching!

### I. ChIP-Seq
#### Overview
Chromatin Immunoprecipitation (ChIP) is a powerful tool used to analyze protein interactions with DNA. Specific antibodies are utilized to isolate a specific protein or modification factor of interest. This can then be used to identify the location and abundance of the protein or modification is within the genome, giving us insight into chromatin structure and gene expression.


<img src="/assets/ChIP_Seq.png" width=450px/>
<i><b>Figure</b> caption here</i>

Let’s take an example: We have two samples of DNA, one for clear cell renal carcinoma and one for regular kidney cells. We want to find sites where expression is higher in the clear cell renal carcinoma sample in order to potential histone modification sites. For this example, we will be using H3K27ac, meaning that there is an acetylation at histone 3, at location 27. Given what we’ve learned about histone acetylation and ChIP-seq, how do we find these modification sites? 

We know that histone acetylation happens when acetyl group attaches to the histone tails of certain proteins by HAT. So by using ChIP, we can find where on our DNA sequence these acetyl groups are using protein specific antibodies in our case, we will use anti-histone H3K27ac.

#### Lab Technique
Here is the basic protocol for both samples:

1. Crosslink cells with formaldehyde 
2. Isolate and shear DNA into chromatin fragments 
3. Immunoprecipitate with protein-specific antibody 
4. Reverse-crosslinks and purify DNA for sequencing 

Next, we prepare the sequence libraries by attaching sequence adaptors to both ends of each fragment. We must then perform PCR to amplify the library and check its concentration. The next step is sequencing. Many sequencing techniques can be used in this step. 

We now move to computational analyses conducted on these data files.

#### Computational Analysis
Before jumping into the fun stuff we must:

1. Clean the raw reads by removing adaptors and PCR duplicates
2. Computationally align fragments to the reference genome 

Next we use peak-calling which utilizes different algorithms that identify regions where there are more reads than background. There are many different programs that generate these calls, popular softwares include: MACS, PeakSeq, SICER, CCAT, etc. From here, your data can be visualized on a genome browser. 

<img src="/assets/ChIP_Visualization.png" width=450px/>
<i><b>Figure</b> caption here</i>

We can clearly see that the bottom two rows (clear cell renal carcinoma) are higher levels of binding than the top two rows (regular kidney cells). This ChIP-seq shows an active ZNF395 super-enhancer only in the clear cell renal carcinoma cells. From this we can see where and which gene is overexpressed. 

### II.
#### Overview

#### Lab Technique

#### Computational Analysis

### Review of Histone Modification Analysis Techniques

## Citations
1. [Darst, Russell P et al. “Bisulfite sequencing of DNA.” Current protocols in molecular biology vol. Chapter 7 (2010): Unit 7.9.1-17. doi:10.1002/0471142727.mb0709s91.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3214597/#S2title)  
2. [Gardiner-Garden M, Frommer M. "CpG islands in vertebrate genomes". Journal of Molecular Biology. 196 (2): 261–82. July 1987. doi:10.1016/0022-2836(87)90689-9.](https://www.sciencedirect.com/science/article/pii/0022283687906899?via%3Dihub)
3. [Krainer, Julie, et al. “EPIC-TABSAT: Analysis Tool for Targeted Bisulfite Sequencing Experiments and Array-Based Methylation Studies.” Nucleic Acids Research, vol. 47, no. W1, 2019, doi:10.1093/nar/gkz398.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6602470/)
4. [Kurdyukov, Sergey, and Martyn Bullock. “DNA Methylation Analysis: Choosing the Right Method.” Biology vol. 5,1 3. 6 Jan. 2016, doi:10.3390/biology5010003.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4810160/)  
5. [Oda, Mayumi, and John M. Greally. “The Help Assay.” Methods in Molecular Biology DNA Methylation, 2009, pp. 77–87., doi:10.1007/978-1-59745-522-0_7.](https://link.springer.com/10.1007/978-1-59745-522-0_7)
6. [Pedersen, B., et al. “MethylCoder: Software Pipeline for Bisulfite-Treated Sequences.” Bioinformatics, vol. 27, no. 17, 2011, pp. 2435–2436., doi:10.1093/bioinformatics/btr394.](https://www.ncbi.nlm.nih.gov/pubmed/21724594)
7. [Thompson, Reid F., et al. “An Analytical Pipeline for Genomic Representations Used for Cytosine Methylation Studies.” Bioinformatics, vol. 24, no. 9, 2008, pp. 1161–1167., doi:10.1093/bioinformatics/btn096.](https://www.ncbi.nlm.nih.gov/pubmed/18353789)
8. [Yao et al. (2017). VHL Deficiency Drives Enhancer Activation of Oncogenes in Clear Cell Renal Cell Carcinoma. Cancer Discovery. 7. CD-17. 10.1158/2159-8290.CD-17-0375.](https://www.ncbi.nlm.nih.gov/pubmed/28893800)
