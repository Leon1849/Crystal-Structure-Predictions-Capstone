# Crystal-Structure-Predictions-Capstone
**Collaborators:**  
- Leonid Sarkisyan  
- Alex Hayrapetyan (Supervisor)

## Introduction

This project implements a full pipeline for extracting crystallographic features from CIF files, visualizing data, and training both classical and deep learning models to predict space group symmetry and unit cell volume.

## Pipeline Steps

1. **Data Preprocessing**  
2. **Data Augmentation**  
3. **Data Visualization**  
4. **Initial Modeling**  
5. **DL Model 1**  
6. **DL Model 2**  
7. **DL Model 2 (Volume Regression)**  
8. **DL Model 3**

## Files and Directories

```
data_preprocessing/      → Scripts and notebooks for parsing CIF files and extracting features (unit cell, angles, volume, atomic positions, formula). Output saved as processed_data.csv.
data_augmentation/       → Augmentation notebooks (e.g., lattice distortions, noise injection).
data_visualization/      → Notebooks for histograms, scatter plots, heatmaps, KDEs.
modeling_initial/        → Classical ML pipelines (Decision Tree, Random Forest, SVM) with baseline metrics.
dl_model_1/              → MLP classifier for space group prediction. Weights saved to Models/model_1/.
dl_model_2/              → Composition-based CRYSPNet-style model. Weights saved to Models/model_2/.
dl_model_2_volume/       → Deep Feedforward Volume Regression. Weights saved to Models/model_2_volume/.
dl_model_3/              → TabNet/MLP regressor for volume prediction. Weights saved to Models/model_3/.
Models/                  → Root directory for all saved model weights.
requirements.txt         → Python dependencies list.
README.md                → This overview document.
```

## Features

- End-to-end CIF processing and feature extraction  
- Augmentation routines for robust model training  
- Interactive data visualizations  
- Classical ML and deep learning modeling  
- Automated saving of best model weights

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/crystal-ml-pipeline.git
cd crystal-ml-pipeline
```

Create and activate a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # For Linux/macOS
# OR
venv\Scripts\activate     # For Windows
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Run the Pipeline

1. **Data Preprocessing**
```bash
cd data_preprocessing
jupyter lab preprocessing.ipynb
```

2. **Data Augmentation**
```bash
cd ../data_augmentation
jupyter lab augmentation.ipynb
```

3. **Data Visualization**
```bash
cd ../data_visualization
jupyter lab visualization.ipynb
```

4. **Initial Modeling**
```bash
cd ../modeling_initial
jupyter lab modeling.ipynb
```

5–8. **Deep Learning Models**
```text
dl_model_1 → dl_model_2 → dl_model_2_volume → dl_model_3
```
After each training run, saved weights will appear under the respective `Models/model_*` folder.

## Contributing

Contributions are welcome!  
Feel free to open an issue or submit a pull request for bug fixes, improvements, or feature requests.
