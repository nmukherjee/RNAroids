# RNAroid Rage

"Roid rage can be defined as a condition in which people tend to act aggressively after taking unusual doses of anabolic steroids regularly. In recent years, several high profile murders and attacks have been attributed to roid rage."

The role of post-transcriptional regulation in roid rage unfortunately still remains unclear.

### Steroid horomones produced by the adrenal cortex are important physiologically regulators. The goal of this research is to understand the RNA regulatory mechanisms controlling steroid hormone metabolism. The experiments are designed to quantify RNA metabolism, specifically, the kinetics of indvidual steps of RNA metabolism in human H295R cells during a timecourse response to a steroidogenic stimulus. The quantification relies on a combination of biochemical methods coupled to RNA-sequencing followed by principled computational analysis. We will use metabolic labeling to infer the kinetics of synthesis, processing, and degradation. Ribosome profiling will be utilized to assess translation. **The goal is to quantify the impact of post-transcriptional regulatory events and inferred putative regulators on steroidogenesis.**

## The workflow will be divided into the following sections:  
+ Generate human steroidogenic transcriptome.  
+ Infer synthesis, processing, and degradation rates from metabolic labeling.  
+ Identify ORFs with ribosome profiling evidence consistent with translation.  
+ Data integration (with emphasis on genes known to be important for steroidogenesis).  
  + Identify regulatory events.  
  + Infer putative regulators.  
  + Focus on ZFP36 family and/or miRNAs.  


Need to include a table describing the data:  
6 timepoints (including untreated) in replicate.

## 1. Generate human steroidogenic transcriptome.
1. STAR 2-pass mapping strategy  
  + Map each sample using GENCODEv25 index  
  + Concatenate all new junctions (some filtering).  
  + Re-map all sample including new junctions.  
2. Run stringtie with default parameters on each sample
3. Merge stringtie-generated GTF using the following samples:
  + All samples
  + Total RNA samples only
  + 4sU samples only
4. Assess utility of new transcripts.
  + Probably filter out "intronic sense" transcripts since these could interfere with quantification of both primary and mature RNA levels.
  + Many divergent transcripts that will not interfere with quantification and are likely to be filtered out due to low expression in later steps in the analysis.

