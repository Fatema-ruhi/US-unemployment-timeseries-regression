# US-unemployment-timeseries-regression
This project predicts the U.S. unemployment rate using time series regression and investigates the impact of the COVID-19 pandemic on job loss trends.
us-unemployment-timeseries-regression/
│
├── README.md
├── data/
│   └── UNRATE.csv
├── scripts/
│   ├── 01_data_preparation.R
│   ├── 02_modeling.R
│   ├── 03_diagnostics_visuals.R
│   ├── 04_predictions.R
├── visuals/
│   ├── plot_residuals.png
│   ├── plot_studentized.png
│   ├── plot_leverage.png
│   ├── plot_cooks_distance.png
│   └── plot_prediction_intervals.png
├── models/
│   └── mod_1_summary.txt
│   └── mod_2_summary.txt
│   └── mod_3_summary.txt
└── report/
    └── Applied_Regression_Analysis_Graduate_Project_Ruhi.pdf

# US Unemployment Time-Series Regression Analysis

This project predicts the U.S. unemployment rate using time series regression and investigates the impact of the COVID-19 pandemic on job loss trends.

## 📊 Dataset
- Source: [FRED UNRATE](https://fred.stlouisfed.org/series/UNRATE)
- Time Span: Jan 1948 – Oct 2021
- Frequency: Monthly

## 🔍 Objectives
- Fit time-series regression models with 24 lags
- Add dummy variables to represent COVID-19 public health emergency and pandemic
- Compare multiple regression models
- Predict unemployment rates for 3 future months

## 🧪 Models
- **Model 1**: Full regression with 26 predictors
- **Model 2**: Scaled predictors + interaction term
- **Model 3**: Final model with reduced variables and outlier removal

## 📈 Visualizations
- Residuals vs. Fitted
- Studentized Residuals
- Leverage Points
- Cook’s Distance
- Confidence Intervals for Forecasts

## 📦 How to Run
Make sure R is installed. Run the scripts in order:

```bash
Rscript scripts/01_data_preparation.R
Rscript scripts/02_modeling.R
Rscript scripts/03_diagnostics_visuals.R
Rscript scripts/04_predictions.R



---

### ✅ Sample Data Visuals
You'll have 5 visuals from the paper:
1. Residuals vs Fitted Values (`plot_residuals.png`)
2. Standardized Residuals (`plot_studentized.png`)
3. Leverage Plot (`plot_leverage.png`)
4. Cook’s Distance (`plot_cooks_distance.png`)
5. Prediction Intervals (`plot_prediction_intervals.png`)

---

### ✅ Code Scripts
I'll extract and rewrite the R code from your appendix into clean, modular scripts under the `/scripts` folder:
- `01_data_preparation.R`: Reads and lags data, creates dummy variables
- `02_modeling.R`: Builds Model 1, 2, 3 and stores summaries
- `03_diagnostics_visuals.R`: Generates the 5 diagnostic plots
- `04_predictions.R`: Predicts unemployment for the next 3 months

---

### ✅ Next Steps
Would you like me to:
1. Generate all the R code files for this structure?
2. Create a ZIP of the full GitHub-ready folder?
3. Optionally, help you push it directly to your GitHub account?

