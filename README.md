# Fraud Detection Using Data Analysis and Visualization

## Project Overview

This project focuses on identifying fraudulent financial transactions using Python-based data analysis, visualization, and machine learning techniques. Leveraging a labeled fraud detection dataset, we aim to uncover hidden patterns, detect anomalies, and build interpretable models to support fraud prevention systems.

---

##  Dataset Description

The dataset contains transaction-level data with the following types of information:

- **Transaction Amounts**
- **Transaction Type**
- **Timestamp**
- **Account ID and User Information**
- **Fraud Labels (1 = Fraud, 0 = Legitimate)**

---

##  Data Preprocessing

- Loaded the dataset using `pandas` and conducted an initial inspection.
- Checked for and handled **missing values**, duplicates, and inconsistencies.
- Converted relevant columns to appropriate data types.
- Standardized column names and values (e.g., transaction types).
- Created additional features like:
  - `Hour of Day`
  - `Transaction Frequency`
  - `Daily Average Amount per User`

---

##  Exploratory Data Analysis (EDA)

Performed in-depth EDA using `Seaborn`, `Matplotlib`, and `Pandas` to discover trends and relationships:

- **Heatmaps**: Displayed correlations between numerical variables using `df.select_dtypes(include=[np.number])`.
- **Boxplots & Violin Plots**: Showed distribution differences between fraudulent and legitimate transactions.
- **Histograms**: Analyzed transaction amount distributions.
- **Scatter Plots**: Revealed outliers and suspicious clusters.
- **Time Series Plots**: Visualized fraud spikes over time.

---

##  Feature Engineering

To improve model performance, we generated new informative features:

- **Suspicious Activity Index**: Based on time, frequency, and amount.
- **Anomaly Score**: Created using statistical distance from typical user behavior.
- **Transaction Hour Category**: Categorical binning of transaction time (night, morning, etc.)

---

##  Statistical Analysis

Used inferential statistics and probability distributions to understand the dataset:

- **Normal, Poisson, Bernoulli Distributions** for modeling transaction behavior.
- **Z-Score and P-Value** calculations to test significance.
- **One-Tailed and Two-Tailed Tests** for fraud impact.
- **Type I and Type II Errors** discussed in fraud detection context.
- **Confidence Intervals** for fraud proportions.
- **Z-Test vs. T-Test**: Applied to compare means between fraud and non-fraud.
- **Chi-Square Test**: Examined independence between features.
- **ANOVA**: Tested differences across multiple transaction types.
- All tests and visualizations were performed using `scipy.stats` and `statsmodels`.

---

##  Machine Learning & Model Evaluation

Implemented classification models to detect fraud:

- Used Logistic Regression, Random Forest, and XGBoost.
- Applied **feature scaling** and **train-test split**.
- Evaluated models using:
  - **Accuracy**
  - **Precision & Recall**
  - **F1-Score**
  - **AUC-ROC Curve**
- Performed **K-Fold Cross Validation** to avoid overfitting.
- Conducted **sensitivity analysis** to determine feature impact on predictions.

---

## Visualization Tools

- Used `Seaborn` and `Matplotlib` extensively for:
  - Heatmaps
  - Violin plots
  - Histograms
  - Correlation plots
  - Line charts
- Applied custom color palettes and plot annotations to enhance clarity.

---

##  Key Insights

- Fraudulent transactions often occur outside of business hours and involve unusually high amounts.
- There is a strong correlation between transaction frequency and fraud likelihood.
- Certain transaction types (e.g., `TRANSFER`) show higher fraud rates.
- Time-based features significantly contribute to fraud prediction.

---

##  Development Environment

- **Python 3.11**
- **VS Code** with **Jupyter Notebook** extension
- Libraries used:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`
  - `scipy`
  - `statsmodels`

---

##  References

- McKinney, Wes. “Python for Data Analysis.” O’Reilly Media.
- Boschetti & Massaron. “Python Data Science Essentials.”
- https://www.kaggle.com/datasets for dataset
- Allen Downey. “Think Stats: Probability and Statistics for Programmers”

---

##  Conclusion

This project demonstrates how data science techniques can be effectively used for detecting fraudulent transactions. Through statistical modeling, machine learning, and compelling data visualizations, we provide meaningful insights that can assist financial institutions in building proactive fraud detection systems.

