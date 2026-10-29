# Dataset Information

## Dataset

**GSE62191 — Gene-expression profiles from frontal-cortex samples**

## Source

NCBI Gene Expression Omnibus (GEO)

Dataset page: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE62191

## Description

The dataset contains brain gene-expression profiles from frontal-cortex samples associated with three groups: healthy controls, individuals with bipolar disorder, and individuals with schizophrenia.

The original GEO study contains 88 samples. One sample is excluded during preprocessing.

## Data Access

The GEO family file is downloaded from NCBI and saved as:

`data/geo/GSE62191_family.soft.gz`

The data-exploration notebook loads this file using GEOparse and constructs the expression matrix and sample metadata.

## Processed Data

Processed files are saved under `data/processed/`, including:

- `expression_matrix.csv` — gene-expression features used for modelling.
- `sample_metadata.csv` — sample identifiers and associated metadata.

Additional CSV files record the results of Elastic Net cross-validation and class-weight experiments.

## Reproducibility and Data Handling

Run the notebooks in the documented order to reproduce data loading, exploration, preprocessing and modelling. Confirm that required packages are installed using the instructions in the main project README.

The original dataset is not stored in this repository.