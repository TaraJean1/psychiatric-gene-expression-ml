# Psychiatric Gene Expression ML

Machine-learning classification of schizophrenia, bipolar disorder and healthy controls using brain gene-expression data.

## Project Overview

This project investigates the following research question:

**Can machine-learning models distinguish schizophrenia, bipolar disorder and healthy controls using brain gene-expression profiles?**

The project uses gene-expression data from the Gene Expression Omnibus (GEO) dataset **GSE62191**, focusing on samples from the frontal cortex. The task is a three-class classification problem, with disease state as the target variable and gene-expression measurements as input features.

## Dataset

- **Source:** NCBI Gene Expression Omnibus (GEO)
- **Accession:** GSE62191
- **Dataset page:** https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE62191
- **Data type:** Brain gene-expression measurements
- **Target classes:** Bipolar disorder, schizophrenia and healthy control
- **Input features:** Gene-expression measurements

The original dataset contains 88 samples. One sample was excluded during data preparation.

See `data/README.md` for instructions on obtaining and preparing the data.

## Repository Structure

```text
psychiatric-gene-expression-ml/
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_preprocessing_and_baseline.ipynb
│   ├── 03_model_training_and_evaluation.ipynb
│   ├── 04_pca_experiments.ipynb
│   └── 05_elastic_net.ipynb
├── data/
│   ├── README.md
│   ├── geo/
│   └── processed/
├── README.md
└── requirements.txt
```

## Methods

The project includes data exploration, missing-value handling, feature scaling, baseline classification and comparisons between machine-learning models.

Models investigated so far include:

- DummyClassifier baseline
- Logistic regression
- K-nearest neighbours (KNN)
- Random forest
- Logistic regression with principal component analysis (PCA)
- Elastic Net logistic regression

Evaluation uses accuracy, macro-F1, precision, recall and confusion matrices. Preprocessing should be fitted using training data only, within the model pipeline, to avoid data leakage.

## Setup and Installation

**Requirements:** Python and the packages listed in `requirements.txt`.

## Running the Project

1. Clone or download this repository.
2. Follow `data/README.md` to obtain and prepare the dataset.
3. Open JupyterLab from the project environment.
4. Run the notebooks in numerical order, following their headings and instructions.
5. Check that the notebooks complete successfully and reproduce their displayed results.

## Limitations and Responsible Use

The dataset is small relative to the number of gene-expression features. This creates a risk of overfitting and limits how reliably model performance can be estimated. Results may also depend on the selected samples, preprocessing choices and evaluation split.
