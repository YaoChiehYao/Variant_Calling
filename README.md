##  BINF 6309 Assignment 5 Variant Calling 
Author: Yao Chieh Yao


## Description
In this assignment 5, we use the genome analysis tool kit(GATK) workflow, 
a standard industrial toolkit  designed for the whole human genome and 
exome data. The process includes NGS data processing, genotyping and 
variant discovery, and variant filtering and evaluation. In the variant 
discovery process, we use DeepVariant, using the convolutional neural 
network (CNN) learning method to train AI for variants calling and 
generating "vcf" and "gvcf" files for further filter & annotation, which 
is not covered in this assignment. 


## Getting Started
* Hi, this is the documentation for assignment five of the bio-computational
  method course, BINF6309.
* Please read my Rmarkdown "MethodsVariantCalling.Rmd" in the GitHub link  
  chunk by chuck to understand the variant calling pipeline and the methods 
  to generate sam/bam  and vcf/gvcf files. 
 
  Here is the link to the files: 
```
https://github.com/NU-Bioinformatics/module05-YaoChiehYao.git
```


## Method 
We use a tool called Trimmomatic for quality trimming the raw sequence data to 
avoid adapter sequences, and low-quality reads for the NGS data processing. 
After that, we download the reference genome from EBI and use the Burrows-Wheeler 
Aligner (BWA) mem method, a recommended latest version for a better quality 
alignment for the reads with reference, and generate a bam file. Finally, we 
apply DeepVariant for variant calling using Docker.  


## References
Bolger, Anthony M., Marc Lohse, and Bjoern Usadel. 2014. “Trimmomatic: A Flexible 
Trimmer for Illumina Sequence Data.” *Bioinformatics* 30 (15): 2114–20..

Li, Heng, and Richard Durbin. 2009. “Fast and Accurate Short Read Alignment with 
Burrows-Wheeler Transform.” *Bioinformatics* 25 (14): 1754–60..

McKenna, Aaron, Matthew Hanna, Eric Banks, Andrey Sivachenko, Kristian Cibulskis, 
Andrew Kernytsky, Kiran Garimella, et al. 2010. “The Genome Analysis Toolkit: 
A MapReduce Framework for Analyzing Next-Generation DNA Sequencing Data.” *Genome 
Res* 20 (9): 1297–1303..

Poplin, Ryan, Pi-Chuan Chang, David Alexander, Scott Schwartz, Thomas Colthurst, 
Alexander Ku, Dan Newburger, et al. 2018. “A Universal SNP and Small-Indel Variant 
Caller Using Deep Neural Networks.” *Nature Biotechnology* 36 (September): 983.
