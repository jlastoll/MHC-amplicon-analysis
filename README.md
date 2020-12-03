# MHC-amplicon-analysis
Analysis of targeted amplicon sequencing data with DADA2


This repository contains an R project file for the complete analysis, as well as an updated pdf document outlining this workflow and expected results in detail. 
The PDF can be recreated with the dada2_HIGT_analysis-primer-trimmed.rmd file.
There are two additional .rmd files: the first dada2_HIGT_analysis.rmd uses the least amount of filtering, and primers were not entirely trimmed here. The second is dada2_HIGT_analysis-stricter-filtering.rmd which also still includes primers, but implements the stricter filters present in the file workflow. I've included both to document various methods we tried and how these impact results.


The input files for this workflow are fastq files from targeted amplicon sequencing data, trimmed of adaptor sequences. We trimmed our sequences with sickle and scythe programs on the command line.
When cloning this repository, make a folder within your local repository that contains fastq files for the analysis.

The workflow in the dada2_HIGT_analysis-primer-trimmed.rmd and dada2_MHC.R files both contain the final workflow we decided on. 
This should run easily just by changing the fastq input files at the beginning of the workflow, with the exception of the section on amino acid analysis. For this analysis section, data from the ScoreCons program needs to be pulled in and is not generated in R.
There are a few points throughout the script where the column subsetting values needs to be changed based on the number of samples in the dataset.
