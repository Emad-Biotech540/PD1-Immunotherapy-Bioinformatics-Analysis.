# 🧬 RNA-seq Differential Expression Analysis with DESeq2

![R](https://img.shields.io/badge/R-4.6.1-blue)
![Bioconductor](https://img.shields.io/badge/Bioconductor-3.23-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

A comprehensive RNA-seq differential expression analysis pipeline using **DESeq2** in R, featuring quality control, differential expression testing, and publication-ready visualizations.

---

## 📖 Overview

This project demonstrates a **complete RNA-seq differential expression analysis workflow** using simulated data that mimics real biological experiments. It is designed as a learning resource and portfolio project for bioinformatics enthusiasts.

The pipeline includes:

- **Data Simulation**: Generating realistic RNA-seq count data (2000 genes × 12 samples)
- **Quality Control**: Multiple QC plots to assess data quality
- **Differential Expression**: Using DESeq2 to identify significantly changed genes
- **Visualization**: Publication-quality plots for interpretation

---

## ✨ Features

### 📊 Quality Control (QC) Plots
- Boxplot - Distribution of gene expression per sample
- Density Plot - Log2(CPM) distribution across samples
- PCA Plot - Principal Component Analysis for sample clustering
- Sample-to-Sample Distance Heatmap
- MA Plot - Normalization quality assessment

### 🧪 Differential Expression (DE) Plots
- Volcano Plot - Up/down-regulated genes with significance
- Heatmap + Dendrogram - Top 50 DEGs expression patterns
- Bar Plot - Count of up vs down-regulated genes

---

## 🛠 Technologies Used

| Category | Tools |
|----------|-------|
| Language | R 4.6.1 |
| Environment | Google Colab (R runtime) |
| Core Packages | DESeq2, BiocManager |
| Visualization | ggplot2, pheatmap, EnhancedVolcano |
| Enrichment | clusterProfiler, org.Hs.eg.db |

---

## 📁 Project Structure

    PD1-Immunotherapy-Bioinformatics-Analysis/
    │
    ├── RNAseq_Differential_Expression_Analysis.ipynb
    ├── README.md
    ├── data/
    │   ├── counts_matrix.csv
    │   └── sample_info.csv
    └── figures/
        ├── 01_Boxplot_QC.png
        ├── 02_Density_QC.png
        ├── 03_PCA_QC.png
        ├── 04_SampleDistance_QC.png
        ├── 05_MA_Plot.png
        ├── 06_Volcano_DE.png
        ├── 07_Heatmap_DEGs.png
        └── 08_Bar_DE.png

---

## 🚀 How to Run

### Step 1: Open in Google Colab
Click the notebook file and open it in Colab.

### Step 2: Change Runtime to R
- Runtime → Change runtime type → R

### Step 3: Install Packages

    if (!require("BiocManager", quietly = TRUE))
        install.packages("BiocManager")
    
    BiocManager::install(c("DESeq2", "EnhancedVolcano", "clusterProfiler"))
    install.packages(c("ggplot2", "pheatmap", "RColorBrewer"))

### Step 4: Run Analysis
Execute all cells in order.

---

## 📊 Results

### Quality Control

| Plot | Purpose |
|------|---------|
| Boxplot | Check sample distribution |
| Density Plot | Check distribution overlap |
| PCA Plot | Check sample clustering |
| Distance Heatmap | Check sample similarity |
| MA Plot | Check normalization quality |

### Differential Expression

| Plot | Purpose |
|------|---------|
| Volcano Plot | Identify significant genes |
| Heatmap | Visualize expression patterns |
| Bar Plot | Count up vs down genes |

---

## 🧠 Key Concepts

| Term | Meaning | Threshold |
|------|---------|-----------|
| log2FoldChange | Change magnitude (log2 scale) | > 1 or < -1 |
| padj | Adjusted p-value (FDR) | < 0.05 |
| baseMean | Average normalized counts | > 10 |

### The Analysis Pipeline

    Raw Counts → Filtering → Normalization → DESeq2 → DEGs → Visualization

---

## 👤 Author

**Emad Eldin Yousif Omarein Abalker**

- B.Sc. in Biotechnology (Honors) - Omdurman Islamic University, Sudan
- Aspiring Computational Biologist
- Interests: Cancer Immunology, PD-1/PD-L1, Immunotherapy

### Connect with me:
- GitHub: [@Emad-Biotech540](https://github.com/Emad-Biotech540)
- LinkedIn: [Emad Eldin](https://www.linkedin.com/in/emadeldien-omarien-562174316)

---

## 📜 License

This project is licensed under the MIT License.

---

## 📚 References

1. Love MI, Huber W, Anders S. (2014). Moderated estimation of fold change and dispersion for RNA-seq data with DESeq2. *Genome Biology*, 15(12), 550.

2. Blighe K, Rana S, Lewis M. (2018). EnhancedVolcano: Publication-ready volcano plots.

3. Kolde R. (2019). pheatmap: Pretty Heatmaps.

---

<div align="center">

**Made with ❤️ by Emad Eldin Yousif**

*From Construction Sites to Bioinformatics Labs*

</div>