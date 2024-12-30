# PBMC Data Analysis Pipeline  

This repository contains an R script for analyzing **Peripheral Blood Mononuclear Cells (PBMC)** data using the Seurat package.  

---

## Prerequisites  

### Required R Packages  
Ensure the following R packages are installed:  
- `dplyr`  
- `Seurat`  
- `patchwork`  
- `ggplot2`  


### Input Data  
- The script expects a 10X Genomics-format dataset located at `filtered_gene_bc_matrices/hg19`.  

---

## Workflow Overview  

1. **Data Loading**  
   - Load the dataset using `Read10X` and initialize a Seurat object.  

2. **Quality Control**  
   - Perform filtering based on mitochondrial content and feature counts.  

3. **Normalization and Feature Selection**  
   - Normalize the data and identify highly variable genes.  

4. **Dimensionality Reduction**  
   - Perform PCA to reduce dimensionality and identify key components.  

5. **Clustering and UMAP**  
   - Cluster the cells and visualize them using UMAP.  

6. **Cluster Annotation and Biomarker Analysis**  
   - Annotate clusters and identify cluster-specific biomarkers.  

7. **Save Outputs**  
   - Save the processed data and visualizations to the output directory.  

---

## Outputs  

- **Seurat Objects:**  
  - `../output/pbmc_tutorial.rds`: Intermediate Seurat object.  
  - `../output/pbmc3k_final.rds`: Final annotated Seurat object.  

- **Plots:**  
  - `../output/images/pbmc3k_umap.jpg`: UMAP plot with labeled clusters.  

---

## Usage  

1. Place the dataset in the specified directory.  
2. Run the script in R or RStudio:  
   ```R  
   source("path_to_script.R")  
   ```  
3. Access outputs in the `../output` directory.  

---

## License  
This script is open-source and distributed under the MIT License.  

--- 
