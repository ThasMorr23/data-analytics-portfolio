# Customer Tenure Analysis (Linear Regression)

## Overview
This project uses linear regression to analyze factors influencing customer tenure in a telecommunications dataset. The goal was to determine whether selected customer and geographic variables could explain how long customers remain with a service.

---

## Objective
- Identify variables associated with customer tenure  
- Build and evaluate a linear regression model  
- Assess the model’s ability to explain variation in tenure  

---

## Tools & Technologies
- Python  
- Pandas, NumPy  
- scikit-learn, statsmodels  
- Matplotlib, Seaborn  

---

## Data Preparation

- Selected relevant features including monthly charges, income, and geographic variables  
- Checked for missing and duplicate values  
- Evaluated outliers using Z-score standardization (retained valid extreme values)  
- Prepared dataset for regression modeling  

---

## Methodology

### Linear Regression Model

A multiple linear regression model was used to examine the relationship between customer tenure (dependent variable) and several independent variables.

Feature selection was performed using **Recursive Feature Elimination (RFE)** to identify the most relevant predictors.

---

### Model Comparison

Two models were evaluated:

- Initial model (full feature set)  
- Reduced model (selected features via RFE)  

Model performance was assessed using:
- R² (coefficient of determination)  
- F-statistic  
- p-values  
- Residual analysis  

---

## Results

### Regression Equation (Reduced Model)

Tenure = 38.4249  
− 0.0021 × MonthlyCharge  
+ 2.025e−06 × Income  
− 0.0836 × Latitude  
− 0.0028 × Longitude  
− 1.333e−05 × Population :contentReference[oaicite:0]{index=0}  

---

### Model Performance

- R² ≈ 0.001  
- Reduced model R² ≈ 0.000  
- High p-values across predictors  

These results indicate that the model explains **almost none of the variance** in customer tenure. :contentReference[oaicite:1]{index=1}  

---

### Residual Analysis

Residual plots revealed **heteroscedasticity**, indicating non-constant variance in errors and reduced model reliability. :contentReference[oaicite:2]{index=2}  

---

## Key Insights

- The selected variables do not strongly explain customer tenure  
- Very low R² values indicate minimal predictive power  
- High p-values suggest relationships may be due to chance  
- Geographic and financial variables have only negligible effects  

---

## Interpretation

The analysis suggests that customer tenure is likely influenced by factors not included in the dataset.  

This indicates:
- Customer retention may depend on behavioral or service-related factors  
- The current feature set is insufficient for predictive modeling  
- More complex or non-linear relationships may exist  

---

## Business Relevance

Although the model did not produce strong predictive results, the findings are still valuable:

- Prevents reliance on ineffective predictors  
- Highlights gaps in available data  
- Guides future data collection efforts  
- Encourages exploration of more meaningful variables (e.g., customer behavior, service interactions)  

---

## Limitations

- Linear regression assumes a linear relationship between variables  
- Presence of heteroscedasticity violates model assumptions  
- Important predictive features may be missing from the dataset  
- Model does not capture complex or non-linear relationships :contentReference[oaicite:3]{index=3}  

---

## Future Improvements

- Explore alternative target variables (e.g., churn instead of tenure)  
- Incorporate behavioral and engagement-based features  
- Apply non-linear models or machine learning approaches  
- Reduce feature set to improve interpretability and performance  
- Address heteroscedasticity through transformation or model selection  

---

## Project Files

- `project-summary.docx` → Full written analysis  
- `images/` → Regression output and residual plots  

---

## Key Takeaway

This project demonstrates that not all models produce strong predictive results—and that evaluating model performance critically is just as important as building the model itself. Identifying when a model does **not** work provides valuable insight that informs better future analysis.
