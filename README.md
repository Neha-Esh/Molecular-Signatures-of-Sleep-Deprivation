# Sleep Deprivation Transcriptomic Analysis

## Project Overview

This repository contains a computational analysis pipeline for studying gene expression changes associated with sleep deprivation using publicly available GEO microarray data.

The workflow includes:

- Data preprocessing and quality control
- Normalization and transformation
- Differential gene expression analysis
- Statistical filtering with FDR correction
- Machine learning classification
- Integrated downstream biological analysis
- Functional enrichment exploration

All analyses are implemented in Python using Jupyter Notebooks.

---

##  Repository Structure
<pre>
```text
.
├── Final_project.ipynb
├── Advanced_Integrated_Analysis_v2.ipynb
├── Enrichment analysis.ipynb
├── Untitled.ipynb
└── README.md
```
</pre>
---

## File Descriptions

### 1. `Final_project.ipynb`

This is the primary analysis notebook and contains:

- GEO data parsing
- Quality control filtering
    - Missing value removal
    - Median imputation
    - Variance filtering
- Quantile normalization
- Log2 transformation
- Differential expression testing (Welch’s t-test)
- Benjamini–Hochberg FDR correction
- Log2 fold change calculation
- DEG identification
- Visualization:
    - Volcano plot
    - MA plot
    - Heatmap (hierarchical clustering)
- Machine learning models:
    - Logistic Regression (baseline)
    - Random Forest classifier
    - Model evaluation (accuracy, precision, recall, F1)

This notebook establishes the core transcriptomic signature.

---

### 2. `Advanced_Integrated_Analysis_v2.ipynb`

This notebook extends the primary analysis and includes:

- Deeper statistical exploration
- Additional visualization layers
- Feature importance analysis
- Comparative model evaluation
- Enhanced interpretability workflows

It builds on the results generated in `Final_project.ipynb`.

---

### 3. `Enrichment analysis.ipynb`

This notebook performs downstream biological interpretation:

- Mapping differentially expressed probes
- Functional annotation
- Pathway enrichment exploration
- Biological theme identification

This stage connects statistical results to biological meaning.

---

### 4. ` analysis.ipynb`

This notebook contains experimental or auxiliary analysis steps, including:

- Testing alternative preprocessing strategies
- Model comparisons
- Parameter tuning experiments
- Additional exploratory plots

It serves as a sandbox for iterative development.

---

## How to Navigate This Repository

1. Start with `Final_project.ipynb` to understand the complete analysis pipeline.
2. Move to `Advanced_Integrated_Analysis_v2.ipynb` for extended modeling and interpretation.
3. Open `Enrichment analysis.ipynb` to explore biological pathway insights.
4. Review `Untitled.ipynb` for additional exploratory or experimental work.

The notebooks are designed to be read sequentially for full reproducibility.

---

##  Requirements

Python 3.x with the following libraries:

- pandas
- numpy
- scipy
- statsmodels
- scikit-learn
- matplotlib
- seaborn

---

## Notes

- All analyses are reproducible within Jupyter Notebook.
- Large datasets are not included in the repository.
- Figures are generated directly within the notebooks.

---

## 🎓 Context

This project was developed as part of an academic bioinformatics analysis exploring molecular signatures of sleep deprivation using transcriptomic data.
