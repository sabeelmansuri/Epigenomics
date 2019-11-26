# Epigenomics
## Overview
In examining the diversity of life, we're often directed to the sequence of an organism's DNA as the source of variation. Differences in these genomes are directly correlated with changes in genetic products, regulatory affects, and molecular interactions--all of which contribute to the great phenotypic variety observed in our world.

However, in this paper, we wish to look beyond the genome. Instead, we introduce the topic of epigenomics, the analysis of gene expression that is not attributable to mutations to the DNA sequence of a genome. Rather, epigenetic expression alteration is caused by biochemical interactions with various proteins and other compounds.

We will describe the biology two most well-known epigenomic modifications: [DNA Methylation](#Biology-DNA-Methylation) and [Histone Modifications](#Biology-Histone-Modifications). We will also describe the analytical techniques used to quantify each epigenomic modification and its affect on gene expression.

## Biology: DNA Methylation
### Introduction

## Biology: Histone Modifications
### Introduction

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


#### Downsteam Analyses


#### Challenges




### II. HELP Assay
#### Overview
The HpaII tiny fragment Enrichment by Ligation-mediated PCR (HELP) Assay leverages restriction enzyme digestion analysis to determine DNA methylation patterns.

More to come--researching!
#### Lab Technique

#### Downsteam Analyses

#### Challenges


## Analysis Techniques: Histone Modifications
### Background
More to come--researching!

## Citations
