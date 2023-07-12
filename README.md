# Differential Methylation in Placental Tissue from Patients with IUGR & Pre-Eclampsia 
https://doi.org/10.3390%2Fcells12081130

## Introduction
This was an end-to-end methylation analysis of 18 placenta samples, 6 from women with Intrauterine Growth Restriction (IUGR), 6 with Pre-Eclampsia, and 6 without pathologies. After DNA extraction, DNA was bisulfite converted, and hybridized to Illumina's Infinium EPIC array, which interrogates ~850,000 CpG sites across the methylome. Data was generated by the array in the form of raw IDAT files. 

## Data Preprocessing
IDAT files were SWAN normalized to beta values using the Minfi package in R. Density plots were generated to identify contamination, and one sample was excluded. A clustermap of all samples was used to identify any global trends in methylation. 

![HeatMap](https://github.com/carternorton11/placenta-methylation/assets/99043737/a40f3eb4-fbe7-47cd-83c2-bf74b94364c2)

## USEQ Analysis
A sliding window analysis was performed using The MethylationArrayScanner and EnrichedRegionMaker from the Useq toolkit.(https://github.com/HuntsmanCancerInstitute/USeq)
Only regions meeting stringent Log2fold and Wilcoxon FDR benchmarks were selected for further analysis. Barplots were generated demonstrating methylation differences at each region between test and control groups. 
<img width="929" alt="Screen Shot 2023-07-12 at 10 35 05 AM" src="https://github.com/carternorton11/placenta-methylation/assets/99043737/14bfc023-dd25-40db-af4a-269de278db30">

## GREAT Analysis
The Genomic Regions Enrichment of Annotations Tool (GREAT - https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4840234/ ) was used to probe for any biological significant pathways associated with the regions of interest. Two biological pathways and one cellular component were identified for the PE regions. 

<img width="875" alt="PE GREAT( 40)" src="https://github.com/carternorton11/placenta-methylation/assets/99043737/4eb18689-5ea4-41cc-af16-c251d5bffeaa">

<img width="826" alt="PE GREAT2( 40)" src="https://github.com/carternorton11/placenta-methylation/assets/99043737/831c6dc3-82c9-414a-83e6-b8c994b27ab4">

## Checking Correlation with Maternal Age and Gestational Age
Correlation analyses were performed to check for possible confounding by maternal and/or gestational age. 

![New_Fig4](https://github.com/carternorton11/placenta-methylation/assets/99043737/dc445cbd-739e-4211-9745-a63e10309bdb)




