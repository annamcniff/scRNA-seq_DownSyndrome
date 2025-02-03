
# scRNA-seq_DownSyndrome
## BMSIP Organoid Project
Work for BMSIP summer internship at the Zeldich lab. ScRNA-seq analysis of ipsc stem cell derived cortical organoids. 

## Plots.zip
Compressed directory containing the following subdirectories: 
    marker_plots: directory containing plots of canonical marker genes used for cluster annotation
    DE_foldchange_plots: directory containing plots of log2foldchange of differentially expressed genes 
    maturation_plots: directory containing subdirectories of 5 different sets of channel associated genes relevant to neural cell maturation and development. 

## Cellranger 
Folder containing qsubs to demultiplex and align paired end reads to Hg38 with 10x genomics CellRanger count

## Seurat_Analysis 
Folder containing the following: 
### Seurat_Analysis.rmd 
Markdown file containing analysis performed in R including: 
    - Creation of Seurat object from samples
    - Data Filtration and Normalization 
    - PCA, Jackstraw, UMAP and tSNE
    - Clustering 
    - Marker gene identification 
### gsea.rmd 
Markdown file containing analysis performed in R including: 
    - imports seurat object saved as .rds by Seurat_Analysis.rmd 
    - more stringent mitochondrial gene filtration to focus results 
    - exports csvs of marker genes by cluster for use in external programs like DAVID
    - plots of maturation genes of interest 
    - exploratory fgsea of Hallmark pathways and other MSigDb pathway groups
    - fold change plots of DE genes overall and by cluster 
### final_analysis.rmd 
Markdown file containing analysis performed in R including: 
    - imports seurat object saved as .rds by Seurat_Analysis.rmd 
    - more stringent mitochondrial gene filtration to focus results 
    - fgsea of Hallmark Pathways and Senescence Gene sets by cluster 
    - outputs plots and .tsvs of fgsea results by cluster 
