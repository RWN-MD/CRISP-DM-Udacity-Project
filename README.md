# CRISP-DM Udacity Project

## Overview

This project applies the **CRISP-DM** (Cross Industry Standard Process for Data Mining) methodology to analyze and model a dataset from the **Centers for Medicare & Medicaid Services (CMS)**. The dataset contains performance metrics from the **CAHPS** (Consumer Assessment of Healthcare Providers and Systems) for MIPS measures submitted by groups in PY 2022.

The goal is to explore relationships between patient volume and performance rates across various measures and use predictive modeling to identify key insights that can guide healthcare decision-making.

## Motivation

Understanding the relationship between patient volume and performance is critical for optimizing healthcare delivery. This project investigates:

1. **What is the relationship between patient volume and performance rates for different measures?**
   - Explored correlations and scatter plots with trendlines.
2. **Which measures are most influenced by patient volume?**
   - Identified measures with significant correlations (|correlation| > 0.4).
3. **Can patient volume be used to predict performance rates for sensitive measures?**
   - Built and evaluated predictive models for selected measures.
4. **What are the optimal patient volumes for maximizing performance?**
   - Interpreted non-linear trends to identify "sweet spots."
5. **How do performance trends vary across different measures?**
   - Visualized differences in trends for measures like “Getting Timely Care” vs. “Access to Specialists.”

## Files in the Repository

- `notebook.ipynb`: Jupyter Notebook containing the complete analysis, including data processing, exploratory analysis, modeling, and visualization.
- `README.md`: This file, providing an overview of the project, methodology, and results.

## CRISP-DM Framework

### 1. Business Understanding

The primary objective is to analyze the relationship between patient volume and performance rates and predict performance for highly correlated measures. Insights are aimed at aiding healthcare policymakers and administrators.

### 2. Data Understanding

- **Source**: [CMS Dataset](https://data.cms.gov/provider-data/dataset/8c70-d353)
- **Attributes**:
  - `Facility Name`: Name of the healthcare facility.
  - `org_PAC_ID`: Organization identifier.
  - `measure_cd`: Code for the performance measure.
  - `measure_title`: Description of the performance measure.
  - `prf_rate`: Performance rate (target variable).
  - `patient_count`: Number of patients (predictor variable).

### 3. Data Preparation

- Handled missing values using:
  - Mean/median imputation.
  - Row removal for comparison.
- Cleaned categorical data for improved visualization.

### 4. Modeling

Predictive models implemented include:

1. **Linear Regression**
2. **Random Forest**
3. **Support Vector Regressor (SVR)**
4. **Quadratic Fit**

Model evaluation metrics:

- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**

### 5. Evaluation

- Selected the best model for each performance measure based on MAE.
- Highlighted measures most influenced by patient volume using correlation analysis.

### 6. Deployment

Findings will be communicated via a blog post aimed at healthcare stakeholders. Visualizations and narratives will be used to bridge technical insights with practical applications.

## Libraries Used

- **`pandas`**: For data manipulation and cleaning.
- **`numpy`**: For numerical computations, including correlation and polynomial fitting.
- **`matplotlib`**: For basic plotting and visualizations.
- **`seaborn`**: For advanced data visualizations, such as box plots and distribution plots.
- **`sklearn`**: For:
  - Data preprocessing: `StandardScaler`
  - Model evaluation: `train_test_split`, `mean_absolute_error`, `mean_squared_error`
  - Machine learning algorithms: `LinearRegression`, `RandomForestRegressor`, `SVR`
- **`scipy`**: For statistical tests like Kolmogorov-Smirnov (K-S) and Z-score analysis.

## Results Summary

- **Key Insights**:
  - Strong correlations identified between patient volume and specific performance measures.
  - Predictive modeling revealed the best approaches for estimating performance rates.
- **Visualizations**:
  - Scatter plots, box plots, and actual vs. predicted charts effectively communicate insights.

## Acknowledgments

- Dataset provided by the Centers for Medicare & Medicaid Services (CMS).
- Guidance from Udacity's Data Science Nanodegree program.

---

For more details, view the Jupyter Notebook or reach out through the GitHub repository.
