# Breast Cancer Classification

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=for-the-badge)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white&style=for-the-badge)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white&style=for-the-badge)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?logo=matplotlib&logoColor=white&style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-42A5F5?logo=seaborn&logoColor=white&style=for-the-badge)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?logo=scikit-learn&logoColor=white&style=for-the-badge)
![Google Cloud](https://img.shields.io/badge/Google%20Cloud%20Storage-4285F4?logo=googlecloud&logoColor=white&style=for-the-badge)

## About

This project classifies breast cancer tumors as **benign** or **malignant** using real-world diagnostic data. It uses **Logistic Regression** from Scikit-Learn for classification, with preprocessing and visualization done using Pandas, Seaborn, and Matplotlib.

The dataset is publicly hosted in a Google Cloud Storage bucket and is loaded directly via the `google.cloud.storage` library. The model achieves an accuracy of **91.2%** based on a single feature: `radius_mean`.

## Features

- **Public Cloud Dataset**: Loads diagnostic cancer data directly from Google Cloud Storage  
- **Data Preprocessing**: Cleans and encodes the dataset using Pandas and NumPy  
- **Exploratory Analysis**: Visualizes relationships between features and diagnosis labels  
- **Modeling**: Trains a Logistic Regression classifier to predict tumor malignancy  
- **Visualization**: Uses Seaborn to visualize predicted vs actual diagnoses  
- **Accuracy**: Achieves ~91.2% accuracy using a single input feature

## Technology Stack

- **Language**: Python  
- **Libraries**: Pandas, NumPy, Seaborn, Matplotlib  
- **Machine Learning**: Scikit-Learn (Linear Regression, Logistic Regression)  
- **Cloud Storage**: Google Cloud Storage (anonymous access via Python SDK)

## Workflow

1. **Download Dataset**  
   Pulls `cancer.csv` from a public Google Cloud bucket

2. **Data Cleaning**  
   - Maps diagnosis labels: `M` → `1`, `B` → `0`  
   - Selects relevant features for analysis

3. **Modeling**  
   - Linear Regression: baseline with poor performance  
   - Logistic Regression: final model trained on `radius_mean`

4. **Evaluation**  
   - Accuracy Score: 91.2%  
   - Diagnosis-specific predictions visualized with Seaborn
