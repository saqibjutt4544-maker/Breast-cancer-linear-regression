# Breast Cancer Linear Regression

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

A simple linear regression model that predicts tumor **area** (`area_mean`) from tumor **radius** (`radius_mean`) using the Breast Cancer Wisconsin (Diagnostic) dataset. Built with `scikit-learn` and includes model evaluation, residual analysis, and a comparison of alternative features.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Requirements](#requirements)
- [Model](#model)
- [Results](#results)
- [Future Improvements](#future-improvements)
- [License](#license)

## Overview
This project demonstrates the fundamentals of simple linear regression:
- Fitting a single-feature linear model with `scikit-learn`
- Evaluating performance using MSE and R²
- Visualizing the regression line on training and test data
- Comparing multiple candidate features for predictive strength
- Performing residual analysis to check model assumptions (homoscedasticity, normality)
- Making predictions on new/example input values

## Dataset
The project uses the **Breast Cancer Wisconsin (Diagnostic) dataset**, which contains measurements computed from digitized images of breast mass fine needle aspirates (FNA). Each row represents one tumor sample, with features describing characteristics of the cell nuclei (radius, texture, perimeter, area, smoothness, etc.).

- **Feature (X):** `radius_mean`
- **Target (y):** `area_mean`

> Note: The dataset file (`Breast_cancer_dataset.csv`) is not included in this repository. You can find the original dataset on [Kaggle](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data) or the UCI Machine Learning Repository.

## Project Structure

Breast-cancer-linear-regression/
│
├── simple_linear_regression.py # Main script: training, evaluation, visualization
├── Breast_cancer_dataset.csv # Dataset (not included — add your own copy)
├── README.md # Project documentation
└── requirements.txt # Python dependencies


## Installation
1. Clone the repository:
```bash
   git clone https://github.com/saqibjutt4544-maker/Breast-cancer-linear-regression.git
   cd Breast-cancer-linear-regression
```
2. Install dependencies:
```bash
   pip install -r requirements.txt
```
3. Add the dataset file (`Breast_cancer_dataset.csv`) to the project root.

## Usage
Run the script directly:
```bash
python simple_linear_regression.py
```
The script will:
1. Load and inspect the dataset
2. Train a linear regression model (`radius_mean` → `area_mean`)
3. Print evaluation metrics (MSE, R², coefficient, intercept)
4. Display training/test scatter plots with the fitted regression line
5. Compare R² scores across multiple candidate features
6. Show residual diagnostic plots (residuals vs. predicted, histogram, Q-Q plot)
7. Print example predictions for sample radius values

## Requirements

pandas
numpy
matplotlib
scikit-learn
scipy


## Model
The relationship is modeled as:

area_mean = intercept + coefficient × radius_mean

The model is trained on an 80/20 train-test split (`random_state=42`) for reproducibility.

## Results
Exact metrics (MSE, R², coefficient, intercept) depend on the dataset used and are printed when the script runs. Given that tumor area scales with the square of radius, this simple linear model serves as a good introductory baseline — a polynomial or log-transformed feature may capture the relationship even more accurately.

## Future Improvements
- Explore polynomial regression, since area theoretically scales with radius²
- Extend to multiple linear regression using additional features
- Add cross-validation for more robust performance estimates
- Package as a reusable module/notebook comparison

## License
This project is open source and available under the [MIT License](LICENSE).