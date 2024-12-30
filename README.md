# pbmc analysis using Seurat Objects

This repository contains R code for analyzing Peripheral Blood Mononuclear Cells (PBMC) data using the Seurat package. The pipeline demonstrates a complete workflow from loading raw data to identifying biomarkers and visualizing clusters.

Contents

Dependencies  
Workflow Steps  
Output Files  
Usage Instructions  
Visualization Examples  
1. Dependencies

The analysis requires the following R packages:

dplyr
Seurat
patchwork
ggplot2
Ensure these packages are installed before running the script.

2. Workflow Steps

Load PBMC Dataset
Load raw data from the specified directory using Read10X() and create a Seurat object.
Quality Control (QC)
Calculate mitochondrial gene percentage.
Generate violin plots for QC metrics like gene counts, RNA counts, and mitochondrial gene percentage.
Subset data to remove low-quality cells.
Normalization and Scaling
Normalize and scale the data to prepare for feature identification.
Variable Feature Selection
Identify highly variable genes and visualize them.
Dimensionality Reduction
Perform PCA and examine results.
Create PCA heatmaps and an elbow plot.
Clustering and Visualization
Use UMAP for dimensionality reduction.
Identify clusters and assign meaningful cluster labels.
Cluster Biomarkers
Identify biomarkers for individual clusters.
Visualize biomarkers using violin plots and feature plots.
Create a heatmap for top cluster markers.
Save Outputs
Save intermediate and final Seurat objects along with visualizations.
3. Output Files

PBMC Seurat Objects
../output/pbmc_tutorial.rds: Intermediate results.
../output/pbmc3k_final.rds: Final annotated dataset.
Images
../output/images/pbmc3k_umap.jpg: UMAP visualization with cluster labels.
4. Usage Instructions

Clone the repository and navigate to the directory containing the script.
Modify the data.dir in the Read10X() function to point to your dataset directory.
Run the script in an R environment.
Generated outputs will be saved in the specified ../output/ directory.
5. Visualization Examples

Violin Plot for QC Metrics:
Visualizes RNA features, RNA counts, and mitochondrial gene percentage per cell.
UMAP Visualization:
Displays clusters in two-dimensional space with labeled cell types.
Heatmap of Top Markers:
Highlights expression levels of top markers across clusters.
