# Basic scRNA-seq Preprocessing and Clustering with Scanpy

## Overview
This project performs basic preprocessing and clustering of single-cell RNA-seq data using Scanpy. Data comes from bone marrow mononuclear cells of healthy human donors (NeurIPS 2021 benchmarking dataset).

## Dataset
- **Source:** OpenProblems NeurIPS 2021 benchmarking dataset
- **Samples:** s1d1 (8,785 cells) and s1d3 (8,340 cells)
- **Total:** 17,125 cells × 36,601 genes
- **Technology:** 10X Multiome Gene Expression

## Workflow Steps
1. Data Loading & AnnData creation
2. Quality Control (MT, Ribo, HB genes)
3. Cell & Gene Filtering
4. Doublet Detection (Scrublet)
5. Normalization & Log transformation
6. Feature Selection (2000 HVGs)
7. PCA Dimensionality Reduction
8. Neighborhood Graph & UMAP
9. Leiden Clustering (multiple resolutions)
10. Marker Gene Annotation
11. Differential Expression Analysis

## Key Results
| Metric | Value |
|--------|-------|
| Initial Cells | 17,125 |
| After Filtering | 17,041 cells |
| Genes After Filtering | 23,427 |
| Doublets Detected | 213 |
| Highly Variable Genes | 2,000 |
| Leiden Clusters (res 0.5) | 18 |

## Cell Types Identified
| Cluster | Cell Type |
|---------|-----------|
| 0 | Lymphocytes |
| 1 | Monocytes |
| 2 | Erythroid |
| 3 | B Cells |

## Tools Used
| Tool | Version | Purpose |
|------|---------|---------|
| Scanpy | 1.12.1 | Main analysis |
| AnnData | 0.12.10 | Data structure |
| Leidenalg | 0.11.0 | Clustering |
| Scrublet | - | Doublet detection |

## Repository Structure
├── README.md
├── notebook/
│   └── Basic_scRNAseq_Scanpy_Tutorial.ipynb
└── results/
└── scrnaseq_processed.h5ad

## Reference
- [Scanpy Tutorial](https://scanpy-tutorials.readthedocs.io/en/latest/tutorials/notebooks/basic-scrna-analysis.html)
- Dataset: doi:10.6084/m9.figshare.22716739.v1
