# Plasmonic Nanocube Spectral Analysis  

This repository contains code and workflows for analyzing the plasmonic properties of silver nanocubes using machine learning methods. The work focuses on predicting **material classification, thickness, and dielectric values** from UV-Vis spectral data.  

## Overview  

- **Dataset**: ~600+ spectral profiles in the range of 300–1000 nm for silver nanocubes with varying dielectric environments.  
- **Objective**: Develop predictive models to classify material type and estimate nanocube thickness and dielectric properties from spectral data.  

Two stages of development are included:  

1. **Initial Exploration (`Plasmonic_Initial(Classification and Clustering).ipynb`)**  
   - Applied preprocessing (Savitzky–Golay smoothing, Euclidean distance filtering).  
   - Tested clustering and classification models.  
   - Linear Discriminant Analysis (LDA) initially performed best but failed to generalize on unseen spectra.  

2. **Final Approach (`Plasmonic_BaggingModels.ipynb`)**  
   - Introduced a cascaded **bagging model** strategy:  
     1. **Step 1**: Classify material type.  
     2. **Step 2**: Use predicted material type as an additional feature to regress **thickness** and **dielectric value**.  
   - Improved robustness on unseen spectral data.  

## Repository Structure  

- `Plasmonic_Initial(Classification and Clustering).ipynb` – Early clustering & classification trials (LDA, etc.)  
- `Plasmonic_BaggingModels.ipynb` – Final cascaded bagging model solution  
- `data/` – Spectral dataset (not included here for size/privacy)  
- `README.md` – Project description and usage  

## Installation  

This project was developed using **Python 3.11.5**.  

### Dependencies  

- numpy  
- pandas  
- scikit-learn  
- matplotlib  
- scipy
- plotly  
- jupyter  

Install all dependencies with:  

```bash
pip install numpy pandas scikit-learn matplotlib scipy jupyter
````

## Usage  

1. **Clone the repository**  
   ```bash
   git clone <repo-link>
   cd plasmonic-nanocubes
   ````
2. Execute on Jupyter notebook
