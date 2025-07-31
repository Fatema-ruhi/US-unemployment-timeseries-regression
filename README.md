# **A Statistical Analysis of Unemployment Rate in the United States of America Using The Time-Series Method**
### **Objective**
To build a time-series regression model that accurately predicts U.S. unemployment rates while evaluating the **impact of COVID-19** using historical monthly data from **January 1948 to October 2021**.

### **Dataset**

* **Source**: [FRED: UNRATE](https://fred.stlouisfed.org/series/UNRATE)
* **Observations**: 862
* **Variables**:

  * `y_t`: Unemployment rate
  * `x1–x24`: Lagged unemployment rates (lag-1 to lag-24)
  * `x25`: COVID-19 Public Health Emergency (binary)
  * `x26`: COVID-19 Pandemic Declaration (binary)
  
### **Methodology**

1. **Model 1**:

   * Full model using 24 lagged predictors + 2 COVID dummies
   * Found high multicollinearity among lag predictors (VIF > 10)
   * Adjusted R² = **93.85%**

2. **Model 2**:

   * Standardized lag variables
   * Added interaction between lag-1 and COVID (x1\_1 × x25)
   * All variables statistically significant
   * Adjusted R² = **94.91%**
   * Reduced multicollinearity

3. **Model 3** (Final Model):

   * Removed influential outliers (33 points)
   * Focused on 4 key predictors: `lag_1`, `lag_2`, `covid`, `interaction`
   * Adjusted R² = **98.63%**
   * Residual standard error: **0.1929**
   * Final equation:

     $$
     \text{Unemployment} = \beta_0 + \beta_1 \text{lag}_1 + \beta_2 \text{lag}_2 + \beta_3 \text{covid} + \beta_4 (\text{lag}_1 \times \text{covid})
     $$

### **Predictions**

Using the final model, predicted unemployment for the **next 3 months**:

| Month | Predicted Rate | 95% Confidence Interval |
| ----- | -------------- | ----------------------- |
| 1     | 4.79%          | \[4.39%, 5.19%]         |
| 2     | 4.92%          | \[4.52%, 5.32%]         |
| 3     | 5.25%          | \[4.85%, 5.64%]         |

## Visualizations
- Residuals vs. Fitted

![pic 1](https://github.com/Fatema-ruhi/US-unemployment-timeseries-regression/blob/f29cf7e6b9f35fe48fb839e0a88a9659ea795169/Residuals%20vs%20Fitted%20Values.PNG)

- Studentized Residuals
- Leverage Points
- Cook’s Distance

### **Key Takeaways**

* Lagged unemployment rates are **strong predictors** of future values.
* The **COVID-19 health emergency significantly impacted unemployment**, as captured by interaction terms.
* **Model 3** is the best model in terms of adjusted R², residual error, and statistical significance.
* Standardization and outlier removal **enhanced prediction accuracy** and reduced multicollinearity.

### **Tools Used**

* **R** programming language
* Regression diagnostics: residuals, leverage, Cook’s distance
* VIF for multicollinearity
* Prediction intervals
