# Analyzing Healthcare Performance Metrics: A CRISP-DM Approach

## Overview
This project applies the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** methodology to analyze and model performance metrics from the **Centers for Medicare & Medicaid Services (CMS)** dataset. Specifically, the dataset includes measures from the **CAHPS (Consumer Assessment of Healthcare Providers and Systems)** for MIPS (Merit-based Incentive Payment System) submitted by groups in PY 2022.

The objective of this project is to explore the relationship between **patient volume** and **performance rates**, identify trends, and use predictive modeling to provide actionable insights for healthcare policymakers and administrators.

---

## Motivation
Understanding how patient volume affects healthcare performance is crucial for optimizing delivery and patient satisfaction. This project addresses key questions, including:

- **How does patient volume impact performance rates across measures?**
  - Explored correlations and scatter plots with trendlines.
- **Which measures are most sensitive to patient volume?**
  - Identified measures with significant correlations (|correlation| > 0.4).
- **Can patient volume predict performance for specific measures?**
  - Built predictive models to evaluate the relationship.
- **What are the optimal patient volumes for maximizing performance?**
  - Identified "sweet spots" using non-linear trend analysis.
- **How do performance trends vary across different measures?**
  - Investigated variability and systemic barriers affecting specific measures.

---

## Files in the Repository
### Analysis and Code
- **`CRISP_DM_Udacity_Project_Notebook.ipynb`**: Jupyter Notebook containing the complete analysis, including data preprocessing, exploratory analysis, modeling, and visualization.
- **`CRISP_DM_Udacity_Project.py`**: Python script version of the notebook for streamlined execution.

### Blog Post
- **`Balancing Patient Volume and Performance in Healthcare: A Data-Driven Perspective.md`**: Blog post summarizing the findings, featuring key visualizations and insights for healthcare stakeholders.

### Figures
All figures used in the analysis and blog are stored in the `BlogFigures` directory:
- **`BlogFigures/BlogFigure1.png`**: Performance trends across measures by patient volume.
- **`BlogFigures/BlogFigure2.png`**: Measures most impacted by patient volume.
- **`BlogFigures/BlogFigure3.png`**: Actual vs. predicted performance rates for key measures.
- **`BlogFigures/BlogFigure4.png`**: Optimal patient volumes for maximizing performance.
- **`BlogFigures/BlogFigure5.png`**: Distribution of performance rates across measures.

### Repository Metadata
- **`README.md`**: This file, providing an overview of the project, methodology, and results.

---

## CRISP-DM Framework
### 1. Business Understanding
The objective is to understand how patient volume affects performance rates and use predictive modeling to assist healthcare decision-making. Key stakeholders include healthcare policymakers and administrators.

### 2. Data Understanding
**Dataset Source**: CMS  
**Attributes**:
- `Facility Name`: Name of the healthcare facility.
- `org_PAC_ID`: Organization identifier.
- `measure_cd`: Code for the performance measure.
- `measure_title`: Description of the performance measure.
- `prf_rate`: Performance rate (target variable).
- `patient_count`: Number of patients (predictor variable).

### 3. Data Preparation
- **Handling Missing Values**:
  - Used mean/median imputation or row removal.
- **Data Cleaning**:
  - Processed categorical variables for improved visualization and analysis.

### 4. Modeling
**Models Implemented**:
- Linear Regression
- Random Forest
- Support Vector Regressor (SVR)
- Quadratic Fit

**Evaluation Metrics**:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

### 5. Evaluation
- Highlighted measures most influenced by patient volume using correlation analysis.
- Selected the best predictive models for each performance measure.
- Investigated variability trends using visualizations.

### 6. Deployment
- Findings were communicated via a blog post featuring visualizations and narratives aimed at healthcare stakeholders.

---

## Libraries Used
- **`pandas`**: Data manipulation and cleaning.
- **`numpy`**: Numerical computations, including correlation and polynomial fitting.
- **`matplotlib`**: Basic plotting and visualizations.
- **`seaborn`**: Advanced visualizations (e.g., box plots, violin plots).
- **`sklearn`**:
  - Data preprocessing: `StandardScaler`
  - Model evaluation: `train_test_split`, `mean_absolute_error`, `mean_squared_error`
  - Machine learning algorithms: `LinearRegression`, `RandomForestRegressor`, `SVR`
- **`scipy`**: Statistical tests (e.g., Kolmogorov-Smirnov, Z-score).

---

## Results Summary
### Key Insights
1. **Strong correlations** identified between patient volume and performance for specific measures.
2. **Predictive modeling** highlighted effective approaches for estimating performance rates.
3. **Visualizations** revealed trends and variability across measures, aiding targeted interventions.

### Visualizations
- **Scatter Plots**: Highlighted trends in patient volume vs. performance.
- **Bar Charts**: Identified measures most impacted by patient volume.
- **Violin Plots**: Illustrated variability in performance trends.
- **Prediction Plots**: Compared actual vs. predicted performance rates.

---

## Blog and Future Directions
The blog post, **“Balancing Patient Volume and Performance in Healthcare: A Data-Driven Perspective,”** highlights the project's findings with actionable insights for healthcare stakeholders. Future steps include:

1. **Expanding the dataset** to include regional trends, socioeconomic data, and staffing ratios.
2. **Incorporating qualitative insights** for a more nuanced understanding of performance metrics.
3. **Engaging policymakers and researchers** to foster interdisciplinary collaboration.

---

## Acknowledgments
- **Centers for Medicare & Medicaid Services (CMS)** for providing the dataset.
- **Udacity Data Science Nanodegree program** for guidance and support.

For more details, explore the Jupyter Notebook or reach out via the repository.  
