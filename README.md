# RNAroids

Steroid horomones produced by the adrenal cortext are physiologically important messengers. The goal of this research is to understand the gene regulatory mechanism underlying steroid hormone metabolism by quantifying RNA metabolism. The experiments are designed quantifying the rates of indvidual steps of RNA metabolism in human H295R cells dueing a timecourse response to a steroidogenic stimulus. This relies on the combination of biochemical methods coupled to RNA-sequencing methods followed by principled computational analysis. We quantify RNA regulatory proceses using metabolic labeling of RNA and ribosome profiling.

1. Generate the genome with annotations.
2. Map all the different samples, SE and PE separately, without using any 2-pass options.
3. Concatenate all SJ.out.tab files. Remove junctions on chrM (false positives, may slow down the 2nd pass).
4. Re-map all sample including new junctions.



mkfifo test_R1_A
mkfifo test_R2_A

gunzip -c test_R1_A.fastq.gz > test_R1_A &
gunzip -c test_R2_A.fastq.gz > test_R2_A &

umi_tools extract -I test_R1_A --read2-in=test_R2_A \
  --bc-pattern=NNNNNNNN   --bc-pattern2=NNNNNNNN \
  --stdout=processed.1.fastq --read2-out=processed.2.fastq \
  -L stats.log 
  
rm test_R1_A test_R2_A stats.log

gunzip -c test_R1
