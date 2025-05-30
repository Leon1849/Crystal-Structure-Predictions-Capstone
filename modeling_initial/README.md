# Crystal Structure Prediction and Volume Regression Project
## Colobarators
- Leonid Sarkisyan
- Alex Hayrapetyan(Supervisor)

## Introduction
This project implements a full pipeline for extracting crystallographic features from CIF files, visualizing data, and training both classical and deep learning models to predict space group symmetry and unit cell volume.

## Pipeline Steps
1) **Data Preprocessing**
2) **Data Augmentation**
3) **Data Visualization**
4) **Initial Modeling**
5) **DL Model 1**
6) **DL Model 2**
7) **DL Model 2 (Volume Regression)**
8) **DL Model 3**

## Files and Directories
- **data_preprocessing/**: Scripts/notebooks to parse CIF links and extract features (unit cell parameters, angles, volume, atomic positions, formula).
- **data_augmentation/**: Notebooks for augmenting structural feature sets (lattice distortions, noise injection).
- **data_visualization/**: Notebooks for plotting histograms, scatter plots, heatmaps, and KDEs.
- **modeling_initial/**: Classical ML pipelines (Decision Trees, Random Forests, SVM) with baseline metrics.
- **dl_model_1/**: MLP classifier for space group prediction; saves weights under `Models/model_1/`.
- **dl_model_2/**: Composition-based symmetry network (CRYSPNet-style); saves weights under`Models/model_2/`.
- **dl_model_2_volume/**: Deep Feedforward Volume Regression; saves weights under `Models/model_2_volume/`.
- **dl_model_3/**:  TabNet/MLP regressor for volume prediction; saves weights under `Models/model_3/`.
- **Models/**: Root folder for all saved model weights, organized by model subfolder.
- **requirements.txt**: Python dependency list.
- **README.md**: This overview document.

## Features
- End-to-end CIF processing and feature extraction.
- Augmentation routines for robust model training.
- Interactive visualizations for exploratory data analysis.
- Baseline and advanced modeling: classical ML and deep learning.
- Automated saving of best model weights after training.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/crystal-ml-pipeline.git
   cd crystal-ml-pipeline

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate
   
3. Install dependencies:
  ```bash
  pip install -r requirements.txt
  ```

### Follow pipeline order:

### 1) Data preprocessing
cd data_preprocessing && jupyter lab preprocessing.ipynb

### 2) Data augmentation
cd ../data_augmentation && jupyter lab augmentation.ipynb

### 3) Data visualization
cd ../data_visualization && jupyter lab visualization.ipynb

### 4) Initial modeling
cd ../modeling_initial && jupyter lab modeling.ipynb

### 5–8) Deep learning models
#### dl_model_1 → dl_model_2 → dl_model_2_volume → dl_model_3

After each training run, check the corresponding Models/model_* folder for saved weights.


Contributing

Contributions are welcome! Please open an issue or submit a pull request for bug fixes or feature requests.

