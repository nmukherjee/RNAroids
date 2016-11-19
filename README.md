# RNA regulation of steroid metabolism



Steroid horomones produced by the adrenal cortex are potent molecules regulating important human physiology, including blood sugar levels, inflammation, blood pressure and volume. [The frequency of adrenal gland disorders in humans spans a wide range depending on the particular disorder.](https://www.nichd.nih.gov/health/topics/adrenalgland/conditioninfo/pages/risk.aspx)
For example, hyperaldasteronism occurs in up to 10% of hypertensive patients, while Cushing's Syndrome 1/100,000 people, though women are 5x more likely to be affected than men. 

![](https://upload.wikimedia.org/wikipedia/commons/c/ca/1818_The_Adrenal_Glands.jpg)

The goal of this research is to understand the RNA regulatory mechanisms controlling the metabolism of steroid hormone produced in the adrenal cortex.Our experiments are designed to quantify RNA metabolism, specifically, the kinetics of indvidual steps of RNA metabolism in human H295R cells during a timecourse response to a steroidogenic stimulus producing cortisol and aldosterone. The quantification relies on a combination of biochemical methods coupled to RNA-sequencing followed by principled computational analysis. We will use metabolic labeling to infer the kinetics of synthesis, processing, and degradation. Ribosome profiling will be utilized to assess translation. **The goal is to quantify the impact of post-transcriptional regulatory events and inferred putative regulators on steroidogenesis.**

## The workflow will be divided into the following sections:  
+ Generate human steroidogenic transcriptome.  
+ Infer synthesis, processing, and degradation rates from metabolic labeling.  
+ Identify ORFs with ribosome profiling evidence consistent with translation.  
+ Data integration (with emphasis on genes known to be important for steroidogenesis).  
  + Identify regulatory events.  
  + Infer putative regulators.  
  + Focus on ZFP36 family and/or miRNAs.  


## Steroid metabolism
![](http://www.pointinstitute.org/wp-content/uploads/2015/09/Zona-Glomerulosa.jpg)


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

## 2. Metabolic labeling: Kinetics of synthesis, processing, degradation

## 3. Ribosome profiling: Quantifying translation of ORFs

## 4. Data integration

