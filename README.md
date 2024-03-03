# Differential Expression Part 2

Volcanoes don't really look like that, do they?

## Problem Statement

In the field of bioinformatics, R has been widely utilized for various analyses, including differential expression analysis. This assignment focuses on performing differential expression analysis using three different packages: DESeq2, edgeR, and Limma. The goal is to compare the results obtained from these packages and explore their differences.

## Learning Objectives

- Understand the basic operations of ggplot and "The Grammar of Graphics".
- Learn to use differential gene expression analysis packages to generate data for plotting.
- Gain proficiency in creating simple plots and customizing colors and themes.
- Learn to combine multiple plots into one image using facet_wrap().

## Skill List

- Intermediate understanding of R's most popular plotting package, ggplot.
- Further understanding of differential expression analysis and its plotting.
- Ability to create high-quality plots using ggplot and customize them according to requirements.

## Instructions

Complete the main.R script to satisfy all the tests in test_main.R. Follow the instructions provided in the function descriptions for main.R and refer to the test descriptions in test_main.R for details on the expected functionality. These functions will be used to generate figures in the report.Rmd file.

## Function Details

### 1. load_n_trim()

The load_n_trim() function loads a counts file into R and selects only the columns corresponding to the samples of interest (P0 and Adult). The gene names are stored as row names in the data frame. This function returns a data frame with the filtered columns and gene names as row names.

### 2. run_deseq()

The run_deseq() function performs differential expression analysis using the DESeq2 package. It takes the counts data and experimental design information as input, conducts the analysis, and returns the results as a DESeqResults object.

### 3. run_edger()

Similar to run_deseq(), the run_edger() function performs differential expression analysis using the edgeR package. It takes the counts data and group information as input, conducts the analysis, and returns the results.

### 4. run_limma() and run_voom()

These functions utilize the Limma package to perform differential expression analysis. The run_limma() function directly uses Limma, while run_voom() applies the voom workflow to refine the data before analysis.

### 5. combine_pval()

The combine_pval() function coerces the results from different packages into a long format, which is suitable for facet wrapping. It combines the p-values from DESeq2, edgeR, and Limma results for visualization.

### 6. create_facets()

This function prepares data for volcano plot visualization. It creates separate data frames for log2 fold-change and adjusted p-values from the results obtained using different packages and combines them for plotting.

### 7. theme_plot()

Finally, the theme_plot() function creates customized plots using ggplot. It allows for experimentation with different colors, themes, and styles to make the plots visually appealing.

## References

- Reference papers and documentation for DESeq2, edgeR, and Limma packages.
