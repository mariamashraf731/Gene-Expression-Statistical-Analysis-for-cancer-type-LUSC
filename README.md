# 🧬 LUSC Gene Expression Statistical Analysis

![Language](https://img.shields.io/badge/Python-3.8%2B-blue)
![Domain](https://img.shields.io/badge/Domain-Bioinformatics-green)
![Data](https://img.shields.io/badge/Dataset-TCGA--LUSC-orange)
![Method](https://img.shields.io/badge/Method-Hypothesis%20Testing%20%26%20Correlation-red)

## 📌 Project Overview
This project performs a comprehensive **Statistical Analysis** on Gene Expression data for **Lung Squamous Cell Carcinoma (LUSC)**. The goal is to identify biomarkers and understand the genetic differences between cancerous and healthy tissues using data from **TCGA (The Cancer Genome Atlas)**.

The study employs statistical methods to find **Differentially Expressed Genes (DEGs)** and analyzes gene-gene correlations to uncover potential co-expression networks.

## ⚙️ Methodology

### 1. Hypothesis Testing (Differential Expression)
* **Objective:** Identify genes that show statistically significant differences in expression levels between Tumor and Normal samples.
* **Methods:**
    * **Null Hypothesis ($H_0$):** There is no difference in gene expression means between the two groups.
    * **Test Used:** Two-sample t-test (or Wilcoxon rank-sum test for non-parametric).
    * **Correction:** False Discovery Rate (FDR) correction (e.g., Benjamini-Hochberg) to handle multiple testing.
* **Outcome:** A list of significant genes categorized by up-regulation and down-regulation.

### 2. Correlation Analysis (Co-expression)
* **Objective:** Explore the relationship between different genes in healthy vs. cancerous tissues.
* **Methods:**
    * **Pearson/Spearman Correlation Coefficients.**
    * Identifying highly correlated gene pairs (Co-expression networks).
* **Outcome:** Ranked lists of correlated genes helping to identify pathways disrupted by cancer.

## 📂 Dataset
The data is sourced from **TCGA-LUSC** dataset (Lung Squamous Cell Carcinoma), containing RSEM normalized gene expression values (FPKM).
* **Samples:** Paired Tumor and Normal tissue samples.
* **Files:** `lusc-rsem-fpkm-tcga-t_paired.txt` (Tumor), `lusc-rsem-fpkm-tcga_paired.txt` (Normal).

## 📊 Key Results
* **Gene Signatures:** Extracted specific genes that can serve as potential diagnostic biomarkers.
* **Report:** Full statistical derivation and biological interpretation can be found in the [Final Report](docs/Biostatistics_Report.pdf).

## 🚀 How to Run
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/mariamashraf731/LUSC-Gene-Expression-Analysis.git](https://github.com/mariamashraf731/LUSC-Gene-Expression-Analysis.git)
    ```
2.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Run Analysis:**
    * For Hypothesis Testing: `jupyter notebook notebooks/2_Hypothesis_Testing.ipynb`
    * For Correlation: `jupyter notebook notebooks/1_Correlation_Analysis.ipynb`

## 👨‍💻 Technologies Used
* **Python**: Data manipulation and analysis.
* **Pandas & NumPy**: Handling large genomic datasets.
* **SciPy.stats**: Statistical tests (T-test, Pearson r, etc.).
* **Matplotlib/Seaborn**: Visualization of distributions and heatmaps.