# RNAroid Rage

## Steroid horomones produced by the adrenal cortext are important physiologically regulators. The goal of this research is to understand the RNA regulatory mechanisms, controlling steroid hormone metabolism. The experiments are designed to by quantifying RNA metabolism, specifically, the kinetics of indvidual steps of RNA metabolism in human H295R cells dueing a timecourse response to a steroidogenic stimulus. This relies on the combination of biochemical methods coupled to RNA-sequencing methods followed by principled computational analysis. We will use metabolic labeling to infer the kinetics of synthesis, processing, and degradation. Ribosome profiling will be utilized to assess translation. **The goal is to identify post-transcriptional regulatory events, as well as infer putative regulators of these events.**

## The workflow will be divided into the following sections:  
## Generate human steroidogenic transcriptome.  
## Infer synthesis, processing, and degradation rates from metabolic labeling.  
## Identify ORFs with ribosome profiling evidence consistent with translation.  
## Data integration (with emphasis on genes known to be important for steroidogenesis)  
### + Identify regulatory events  
### + Infer putative regulators  
###  + focus on ZFP36 family and/or miRNAs  


Need to include a table of the data
6 timepoints (including untreated) in replicate.

## 1. Generate human steroidogenic transcriptome.
1. STAR 2-pass mapping strategy  
  + Map each sample using GENCODEv25 index  
  + Concatenate all new juctions (some filtering).  
  + Re-map all sample including new junctions.  
2. Run stringtie with default parameters on each sample
3. Merge stringtie-generated GTF:
  + All samples
  + Total RNA samples only
  + 4sU samples only
4. Assess utility of new transcripts.
  + Probably filter out "intronic sense" transcripts since these could interfere with quantification of both primary and mature RNA levels.
  + Many divergents that will not interfere with quantification and likely to be filtered out due to low expression in later steps.

