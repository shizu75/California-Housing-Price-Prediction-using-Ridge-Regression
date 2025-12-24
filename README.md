# California Housing Price Prediction using Ridge Regression

## Overview
This repository presents a structured regression analysis pipeline applied to the California Housing dataset. The project focuses on feature selection, exploratory data analysis, statistical correlation assessment, and regularized linear regression. It is written and documented in a research-oriented manner, suitable for inclusion in a PhD or academic portfolio, emphasizing methodological clarity and reproducibility.

## Dataset
The dataset used is **California Housing Training Data**, loaded from:
`/content/sample_data/california_housing_train.csv`

The target variable is **median_house_value**, representing the median house price for a given geographic block group. All other variables are treated as predictive features.

## Data Cleaning and Feature Selection
Initial preprocessing involves removing redundant or highly correlated features to reduce multicollinearity and improve model stability. The following steps are applied:
- Removal of `total_rooms` due to redundancy with other housing attributes
- Removal of `population` after correlation analysis
- Removal of `latitude` to reduce spatial bias during baseline modeling
- Validation of missing values (none detected)

Descriptive statistics are computed to understand feature distributions before modeling.

## Exploratory Data Analysis
Correlation analysis is performed using Pearson correlation coefficients and visualized with a heatmap to identify relationships between features. Additional exploratory visualizations include:
- Scatter plots to examine relationships between households and total bedrooms
- Histograms to inspect the distribution of median income

These steps guide informed feature selection prior to regression modeling.

## Data Preparation
The dataset is split into features (X) and target (Y). Feature scaling is performed using **StandardScaler** to normalize feature magnitudes, which is critical for regularized regression methods. The data is then split into training (70%) and testing (30%) subsets with randomized shuffling to ensure generalization.

## Model Architecture
A **Ridge Regression** model is employed to address potential multicollinearity and overfitting by introducing L2 regularization. The regularization parameter is set to:
- Alpha = 0.5

This choice balances bias and variance while maintaining interpretability.

## Model Evaluation
Model performance is evaluated on the test set using regression-appropriate metrics:
- Mean Squared Error (MSE) to quantify prediction error
- R-squared (R²) to measure variance explained by the model

These metrics provide a clear assessment of predictive performance and model fit.

## Tools and Technologies
Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, and regularized linear regression techniques are used throughout this project.

## Research Significance
This project demonstrates a statistically grounded regression workflow suitable for baseline modeling in socioeconomic and geospatial prediction tasks. It highlights principled feature selection, regularization, and transparent evaluation, making it appropriate for academic research, benchmarking, and PhD portfolio inclusion. The methodology can be extended to advanced models such as Elastic Net, Gradient Boosting, or deep learning architectures.

## Disclaimer
This work is intended for academic and research purposes only. The predictions are not meant for real-world housing valuation or financial decision-making.

## Author
This repository represents an academically structured machine learning regression study developed for research and PhD portfolio presentation.
