# Single-cell RNA-seq Analysis for Bronchoalveolar Immune Cells in COVID-19 Patients

This repository contains code and data for the analysis of bronchoalveolar immune cells in COVID-19 patients using single-cell RNA-sequencing data. The study aims to understand immune characteristics associated with COVID-19 severity.

## Dataset Description
- **Source**: [GEO Accession GSE145926](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE145926)
- **Title**: Single-cell landscape of bronchoalveolar immune cells in COVID-19 patients
- **Organism**: Homo sapiens
- **Experiment Type**: Expression profiling by high throughput sequencing

## Analysis Pipeline
1. **Data Preprocessing**:
   - .h5 files were preprocessed to extract necessary data slots for machine learning.

2. **Principal Component Analysis (PCA)**:
   - PCA was performed to examine batch effects in the mild group, severe group, control group, and the merged group (mild + severe + control).

3. **Machine Learning (ML)**:
   - The merged group data was used for machine learning tasks.

4. **Machine Learning Algorithms Tested**:
   - Random Forest, K-Nearest Neighbors (KNN), and ExtraTreesClassifier were tested for cell deconvolution to determine the best algorithm.

## Files in Repository
- `ML_Script1_data_preprocessing.ipynb`: Python script for data preprocessing including data extraction from .h5 files.
- `ML_Script2_data_preprocessing.ipynb`: Jupyter notebook containing PCA analysis and train-test split.
- `ML_Script3_model_training.ipynb`: Jupyter notebook containing feature selection and comparing machine learning algorithms.
- `data/`: Folder containing data files used in the ML comparison.
- `data_processing/`: Folder containing the intermediate files during preprocessing
- `data_raw/`: Folder containing raw data download from GEO database

## Usage
1. Clone the repository: `git clone https://github.com/Angel030331/Data_science_ML_project_3`
2. Run the preprocessing script: `ML_Script1_data_preprocessing.ipynb`
3. Explore PCA analysis in the `ML_Script2_data_preprocessing.ipynb` notebook.
4. Compare ML algorithms in the `ML_Script3_model_training.ipynb` notebook.
