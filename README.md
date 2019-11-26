<img src="https://i.imgur.com/UHs2ojK.png" width=300px/>

## Overview
In examining the diversity of life, we're often directed to the sequence of an organism's DNA as the source of variation. Differences in these genomes are directly correlated with changes in genetic products, regulatory affects, and molecular interactions--all of which contribute to the great phenotypic variety observed in our world.

However, in this paper, we wish to look beyond the genome. Instead, we introduce the topic of epigenomics, the analysis of gene expression that is not attributable to mutations to the DNA sequence of a genome. Rather, epigenetic expression alteration is caused by biochemical interactions with various proteins and other compounds.

We will describe the biology two most well-known epigenomic modifications: [DNA Methylation](#Biology-DNA-Methylation) and [Histone Modifications](#Biology-Histone-Modifications). We will also describe the analytical techniques used to quantify each epigenomic modification and its affect on gene expression.

## Biology: DNA Methylation
### Introduction
More to come--researching!

## Biology: Histone Modifications
### Introduction
Histones are proteins found in eukaryotic cell nuclei that order DNA into nucleosomes. These components of chromatin are subject to post-translational modifications including methylation, acetylation, phosphorylation, ubiquitylation, and others still being researched. The histone code hypothesis suggests that these modifications to chromatin structure along with epigenetic markers influence the recruitment of proteins responsible for regulating gene expression. Multiple modifications work together simultaneously to regulate and change chromatin state and gene expression.

### I. Histone Acetylation
Acetylation connects a negative charge acetyl group to lysine residues of the N-terminal histone tails (specifically H3 and H4) by histone acetyltransferase (HAT). By doing so, negatively charged DNA is repelled, causing the chromatin to relax into euchromatin and allow for transcription factors to bind and increase gene expression. Deacetylation by histone deacetylase (HDAC) however condenses chromatin into heterochromatin, therefore deactivating gene activity.

<br />

<img src="/assets/Histone_Acetylation.png" width=450px/>
Acetylation of histones, leading to relaxation of DNA into euchromatin. Note the larger regions of exposed DNA open for transcription after acetylation.

### II. Histone Methylation/Demethylation
Unlike histone acetylation, methylation is a post-translational epigenetic modification that does not directly change histone charge or histone-DNA interactions. Instead, a methyl group is added to lysine or arginine residues of histone tails, each impacting transcription differently. Arginine methylation activates transcription and transcriptional activities, while Lysine methylation’s effect depends on the methylation site and length. Methylation of sites such as H3K4, K36, and K79 result in transcriptional activation, while methylation of H3K9, K27, and H4K20 silence gene activity/expression. 

### III. Histone Phosphorylation
Unique from histone methylation and acetylation, histone phosphorylation employs interaction between other histone modifications and binding proteins. Chromatin remodeling happens by attaching a phosphoryl group to histone tails, occuring on all histone core proteins, having distinct effects on each. This process plays a huge role in cell division, transcriptional regulation, and DNA damage repair. 

### III. Histone Ubiquitylation
More to come--researching!

## Analysis Techniques: DNA Methylation
### Background
The goal of DNA Methylation analysis is fairly obvious: we wish to detect what parts of the genome are methylated to identify, confirm, or analyze downregulated regions.

Let's take an example: We have two bacterial samples that should both be expressing a gene that turns them blue. However, one culture appears blue while the other appears white. Given what we've learned, we may hypothesize that, for some reason, the white colony of bacteria have methylated the region containing the gene, thus downregulating it. How can we test this hypothesis?

Indeed, genetic sequencing shows the DNA sequence of both bacteria to be identical, yet the white colony shows little to no transcription of this gene. What we've just mentioned sets the context for DNA methylation analysis: **genetic sequencing is unable to distinguish methylated and non-methylated cytosine**. Therefore, we require other analysis technqiues:

### I. Bisulfite Sequencing
#### Overview
Bisulfite sequencing is the most widely-used and popular DNA Methylation analysis technique. The core idea is to convert non-methylated cytosine into uracil, but keep methylated cytosine unchanged. Then, run a sequencing analysis. The converted cytosine (now uracil) will be detected as thymine, so every detected cytosine will be methylated, giving a clear indication of which regions are methylated.

![Bisulfite Conversion](assets/Bisulfite_Conversion.png)  
The conversion of non-methylated cytosine into uracil, which are read as thymines by sequencing technology. Notice that methylated cytosine are unchanged and remain sequenced as cytosines.
#### Lab Technique
The first milestone in a bisulfite sequencing analysis is the treatment of DNA with [bisulfite](https://en.wikipedia.org/wiki/Bisulfite). There are three major steps in this protocol:

1. Denaturation of DNA into single strands.
2. Incubation with bisulfite solution at high temperature.
3. Cleaning of DNA; removal of bisulfite and residues

The product of this will be DNA with non-methylated cytosine converted into uracil. Although [whole genome bisulfite sequencing](https://en.wikipedia.org/wiki/Whole_genome_bisulfite_sequencing) is becoming increasingly viable, it is not yet a common method. Thus, we will not focus on this here and will instead continue with the more common analysis pipeline: region-specific analysis.

#### Computational Analyses
More to come--researching!

#### Challenges
More to come--researching!


### II. HELP Assay
#### Overview
The HpaII tiny fragment Enrichment by Ligation-mediated PCR (HELP) Assay leverages restriction enzyme digestion analysis to determine DNA methylation patterns.

More to come--researching!
#### Lab Technique
More to come--researching!

#### Computational Analyses
More to come--researching!

#### Challenges
More to come--researching!


## Analysis Techniques: Histone Modifications
### Background
More to come--researching!

## Citations
1. [Darst, Russell P et al. “Bisulfite sequencing of DNA.” Current protocols in molecular biology vol. Chapter 7 (2010): Unit 7.9.1-17. doi:10.1002/0471142727.mb0709s91.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3214597/#S2title)  
2. [Kurdyukov, Sergey, and Martyn Bullock. “DNA Methylation Analysis: Choosing the Right Method.” Biology vol. 5,1 3. 6 Jan. 2016, doi:10.3390/biology5010003.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4810160/)  
3. [Oda, Mayumi, and John M. Greally. “The Help Assay.” Methods in Molecular Biology DNA Methylation, 2009, pp. 77–87., doi:10.1007/978-1-59745-522-0_7.](https://link.springer.com/10.1007/978-1-59745-522-0_7)
