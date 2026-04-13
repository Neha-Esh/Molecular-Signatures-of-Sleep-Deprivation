# Molecular Signatures of Sleep Deprivation

## Project Overview

This repository contains a computational analysis pipeline for studying gene expression changes associated with sleep deprivation using publicly available GEO microarray data.

The workflow emphasizes **phase-aware transcriptomic analysis**, focusing on how gene expression changes during sleep deprivation and whether expression returns toward baseline during recovery.

Key components of the analysis include:

- Data preprocessing and normalization (microarray-based)
- Phase-aware analysis (baseline, experimental, recovery)
- Differential expression analysis
- Statistical filtering with FDR correction
- Effect size–based gene ranking
- Experimental vs recovery comparison
- Recovery vs persistent gene classification
- Pathway enrichment analysis
- Protein interaction exploration (PPI)

All analyses are implemented in Python using Jupyter Notebooks.

---

## Repository Structure

```text
.
├── Final_project.ipynb
├── Phase_Aware_Gene_Expression_Analysis.ipynb
├── Phase_Based_Reanalysis.ipynb
├── Advanced_Integrated_Analysis_v2.ipynb
├── Enrichment analysis.ipynb
├── protein interaction analysis.ipynb
├── ML model.ipynb
├── labels.ipynb
├── analysis.ipynb
├── results/
│   ├── normalized_expression.csv
│   ├── sample_metadata.csv
│   ├── dge_results.csv
│   ├── degs_all.csv
│   ├── degs_up.csv
│   ├── degs_enhanced_table.csv
│   ├── mapped_all_gene_symbols.csv
│   ├── mapped_up_gene_symbols.csv
│   ├── mapped_down_gene_symbols.csv
│   ├── enrich_all_symbols.csv
│   ├── enrich_up_symbols.csv
│   ├── enrich_down_symbols.csv
│   ├── rec_enrichment_results.csv
│   ├── exp_enrichment_results.csv
│   ├── ml_logistic_top_genes.csv
│   ├── ml_random_forest_top_genes.csv
│   ├── model_metrics_leakfree_cv.csv
│   ├── permutation_test_aucs.csv
│   ├── stability_selection_all.csv
│   ├── stable_signature.csv
│   ├── top_exp_genes_symbols.csv
│   ├── top_rec_genes_symbols.csv
│   ├── protein_interaction_network_edges.csv
│   ├── protein_interaction_network_hubs.csv
│   └── (other intermediate outputs)
├── figures/
│   ├── volcano_plot.png
│   ├── ma_plot.png
│   ├── heatmap_top_degs.png
│   ├── top_degs_expression.png
│   ├── feature_importance_rf.png
│   ├── cm_leakfree_top50_logreg.png
│   └── expected_pathways.png
└── README.md
```

---

## Notebook Descriptions

### Phase_Aware_Gene_Expression_Analysis.ipynb

- Defines baseline, experimental, and recovery phases
- Performs subject-level normalization
- Explores gene expression trends across timepoints

---

### Phase_Based_Reanalysis.ipynb

- Core analysis notebook
- Computes differential expression without averaging
- Applies FDR correction
- Ranks genes by effect size
- Compares experimental vs recovery phases
- Classifies genes as recovered or persistent

---

### Enrichment analysis.ipynb

- Performs pathway enrichment
- Focuses on recovered and persistent genes
- Identifies ribosomal and translational pathway signals

---

### protein interaction analysis.ipynb

- Builds protein–protein interaction networks
- Identifies hubs and connectivity patterns

---

### Advanced_Integrated_Analysis_v2.ipynb

- Integrates results from all steps
- Generates summary visualizations
- Supports final interpretation

---

### Final_project.ipynb

- Initial pipeline before refinement
- Includes preprocessing, normalization, and early DE analysis

---

### ML model.ipynb

- Exploratory machine learning models
- Logistic regression and random forest
- Feature importance and evaluation

**Note:** ML is optional and not the main focus.

---

### labels.ipynb

- Processes metadata
- Extracts subject IDs, conditions, and timepoints

---

### analysis.ipynb

- Exploratory notebook
- Used for testing and intermediate steps

---

## Results Folder

The `results/` folder contains:

- Differential expression outputs
- Gene mapping files
- Enrichment results
- Machine learning outputs
- Stability selection outputs
- Protein interaction data

---

## Figures Folder

The `figures/` folder contains:

- Volcano and MA plots
- Heatmaps of top genes
- Expression visualizations
- ML evaluation plots
- Enrichment-related figures

---

## How to Run

```bash
git clone <your-repo-link>
cd <repo-name>
pip install -r requirements.txt
jupyter notebook
```

Recommended order:

1. Phase_Aware_Gene_Expression_Analysis.ipynb  
2. Phase_Based_Reanalysis.ipynb  
3. Enrichment analysis.ipynb  
4. Advanced_Integrated_Analysis_v2.ipynb  

---

## Requirements

- pandas  
- numpy  
- scipy  
- statsmodels  
- scikit-learn  
- matplotlib  
- seaborn  

---

## Key Findings

- No genes passed strict FDR < 0.05
- Phase-aware analysis revealed meaningful patterns
- Experimental phase showed stronger disruption
- Many genes partially recovered
- Ribosomal and translational pathways were enriched
- Pathway-level analysis was more informative than gene-level

---

## Notes

- Based on Affymetrix microarray data  
- Data already normalized (RMA)  
- No RNA-seq normalization needed  
- Results are exploratory due to weak statistical signal  

---

## Context

This project was developed as part of an academic bioinformatics study on transcriptomic responses to sleep deprivation.
