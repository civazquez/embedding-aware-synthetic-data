# Embedding-Aware Synthetic Data Generation

Code and notebooks supporting the dissertation:

**A Unified Framework for Embedding-Based Synthetic Data Generation with High-Cardinality Categorical Features**

## What this project does
This work studies how categorical representations affect both:
1) **Predictive utility on real data**, and  
2) **Synthetic data fidelity** (whether synthetic data can stand in for real data).

We evaluate representations through:
- **Intrinsic structure** (embedding geometry diagnostics such as NN-overlap and IDP/IDPE when a reference structure exists)
- **Extrinsic performance** (downstream prediction on real data)
- **Synthetic fidelity** (TSTR/TRTS using CTGAN, TVAE, and an LLM-based generator)

## Datasets and tasks
- **Adult** (classification): income prediction using numeric features + categorical variables  
- **PetFinder** (classification): adoption outcome using numeric features + categorical variables  
- **Breast Cancer** (classification): 5-year survival using numeric features + TNM codes + hospital ID  
- **IPEDS / CIP** (regression): predicting completion counts (i.e., number of awards/completions reported for a program/institution)

> Note: Datasets are not included in this repository.

## Repository structure
- `notebooks/` — notebooks (01–05F) for preprocessing, encoding/embedding, evaluation, and aggregation
- `config/` — `config.json` with dataset paths, targets, and split settings
- `data/` — placeholder (expected location for cleaned CSVs)
- `outputs/` — placeholder (large outputs not tracked)

## How to run (high level)
1. Place cleaned CSVs under `data/` using the filenames referenced in `config/config.json`.
2. Open notebooks in `notebooks/` and run in order (01 → 05F).
3. Generated results will be written to `outputs/` (not tracked in git).

## Reproducibility notes
Experiments were developed in a Google Drive environment (Colab-style paths in some notebooks).
You may need to adjust file paths depending on your setup.

## Contact
Cesar Vazquez
