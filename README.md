# Predictive Modeling of Aqueous Solubility (ESOL) Using Automated Machine Learning Frameworks

## Author
**Pritom Kundu** *B. Pharm Honors* *University of Rajshahi*

---

## Overview
This repository contains a comprehensive computational pipeline for predicting the aqueous solubility of small molecules—a critical parameter in the pharmacokinetic profiling and lead optimization phases of drug discovery. Utilizing the **Delaney (ESOL) dataset**, this project implements an automated machine learning (AutoML) workflow to transition from raw molecular structures to high-accuracy predictive models.

Aqueous solubility determines the bioavailability and efficacy of therapeutic compounds. This implementation leverages the **PyCaret** library and **RDKit** to provide a robust, scalable solution for cheminformatics research.

## Key Features
* **Molecular Descriptor Engineering**: Automated calculation of key physicochemical properties, including LogP, Molecular Weight (MW), Number of Rotatable Bonds (NRB), and Aromatic Proportion (AP).
* **AutoML Integration**: Systematic model comparison across various regression architectures (e.g., LightGBM, Gradient Boosting, Random Forest, and Extra Trees).
* **Predictive Analytics**: High-performance modeling targeting $R^2$ optimization for log solubility (logS) prediction.
* **Interpretability & Validation**: Comprehensive evaluation through residuals analysis, prediction error plots, and feature importance mapping.

## System Architecture & Workflow

### 1. Data Acquisition and Preprocessing
The pipeline utilizes the standard ESOL dataset containing SMILES (Simplified Molecular Input Line Entry System) strings. The preprocessing stage involves:
* Standardization of molecular structures using RDKit.
* Feature engineering to derive molecular descriptors.
* Data partitioning for unbiased model validation and testing.

### 2. Model Development (PyCaret Implementation)
The core of the predictive engine is built on the `pycaret.regression` module, which streamlines academic workflows:
* **Setup**: Automated feature scaling, normalization, and handling of multicollinearity.
* **Model Comparison**: Parallel evaluation of multiple regressors based on MAE, MSE, RMSE, and $R^2$ metrics.
* **Hyperparameter Optimization**: Systematic tuning to enhance generalization and mitigate over-fitting.

### 3. Visualization and Diagnostics
To ensure scientific rigor, the repository includes built-in diagnostic plots:
* **Residuals Plot**: Assessing error distribution and homoscedasticity.
* **Feature Importance**: Identifying the molecular descriptors most influential to solubility.
* **Prediction Error**: Visualizing the correlation between experimental and predicted values.

## 🛠️ Technical Requirements
The project is optimized for execution within **Google Colab** and requires the following dependencies:

* 🐍 **Python 3.x**
* 🧪 **RDKit** (Cheminformatics toolkit)
* 🤖 **PyCaret >= 3.0.0** (Low-code ML library)
* 📊 **Pandas & Numpy** (Data manipulation)
* 📈 **Matplotlib & Seaborn** (Data visualization)

## Usage
To replicate the study or deploy the model for new chemical entities:
1. Clone the repository.
2. Install dependencies via the initialization cells provided in the `.ipynb` notebook.
3. Execute the pipeline to perform automated model selection and solubility prediction.

## Results Summary
The automated selector typically identifies ensemble-based methods (such as **LightGBM** or **Extra Trees Regressor**) as the most effective architectures for this chemical space, consistently achieving high $R^2$ values on test hold-out data.

---
*This work is intended for researchers in Computer-Aided Drug Design (CADD), Cheminformatics, and Computational Pharmaceutical Sciences.*
