# 📈 Time Series Forecasting using ARIMA & SARIMA

A comprehensive time series forecasting project developed as part of the **MA641 – Time Series Analysis** course. This repository demonstrates the complete workflow for analyzing, modeling, and forecasting both **non-seasonal** and **seasonal** time series using classical statistical methods in **R**.

The project includes two independent case studies:

- 🥇 **Gold Spot Price Forecasting (XAU/USD)** using **ARIMA**
- 📊 **Consumer Price Index (CPI) Forecasting** using **Seasonal ARIMA (SARIMA)**

---

## Project Objectives

The primary objectives of this project are to:

- Analyze real-world financial and economic time series data.
- Identify trends, seasonality, and stationarity characteristics.
- Apply appropriate transformations to prepare data for modeling.
- Build forecasting models using ARIMA and SARIMA.
- Evaluate model adequacy through statistical diagnostics.
- Generate future forecasts with confidence intervals.

---

## Repository Structure

```
.
├── MA641 Research Project.Rmd              # Gold Price Forecasting (ARIMA)
├── MA641 Research Project(Seasonal).Rmd    # CPI Forecasting (SARIMA)
├── datasets/
│   ├── XAU_USD Historical Data.csv
│   └── CPIAUCSL.csv
├── figures/
│   └── (generated plots)
└── README.md
```

---

# Case Study 1: Gold Spot Price Forecasting

## Problem Statement

Gold prices exhibit significant fluctuations due to macroeconomic conditions, inflation, interest rates, and global market sentiment. This study focuses on forecasting Gold Spot Prices using a non-seasonal ARIMA model.

### Dataset

- Historical Gold Spot Prices (XAU/USD)
- Daily observations

### Workflow

- Data loading and preprocessing
- Exploratory Data Analysis (EDA)
- Summary statistics
- Time series visualization
- Rolling Mean and Rolling Variance
- Stationarity testing using the Augmented Dickey-Fuller (ADF) Test
- Log transformation
- First-order differencing
- ACF and PACF analysis
- ARIMA model selection
- Residual diagnostics
- Future price forecasting

---

# Case Study 2: Consumer Price Index (CPI) Forecasting

## Problem Statement

Consumer Price Index (CPI) is an important indicator of inflation and economic performance. Since CPI exhibits recurring seasonal behavior, Seasonal ARIMA (SARIMA) is employed for accurate forecasting.

### Dataset

- Consumer Price Index (CPI)
- Monthly observations

### Workflow

- Data preprocessing
- Exploratory Data Analysis
- Rolling statistics
- Stationarity analysis
- ADF Test
- KPSS Test
- Log transformation
- First-order differencing
- Seasonal differencing
- Seasonal decomposition
- Seasonal ACF/PACF
- SARIMA model fitting
- Residual diagnostics
- Future CPI forecasting

---

# Methodology

The project follows the standard Box-Jenkins methodology for time series forecasting.

```
Raw Data
    │
    ▼
Data Cleaning
    │
    ▼
Exploratory Data Analysis
    │
    ▼
Stationarity Testing
    │
    ▼
Transformation & Differencing
    │
    ▼
ACF / PACF Analysis
    │
    ▼
Model Selection
(ARIMA / SARIMA)
    │
    ▼
Residual Diagnostics
    │
    ▼
Forecast Generation
```

---

# Statistical Techniques Used

## Exploratory Analysis

- Time series visualization
- Summary statistics
- Rolling Mean
- Rolling Variance

## Stationarity Tests

- Augmented Dickey-Fuller (ADF) Test
- KPSS Test
- Visual inspection

## Data Transformations

- Log Transformation
- First-order Differencing
- Seasonal Differencing

## Model Identification

- Autocorrelation Function (ACF)
- Partial Autocorrelation Function (PACF)

## Forecasting Models

### ARIMA

Used for the Gold Price forecasting dataset.

General notation:

```
ARIMA(p,d,q)
```

where

- p = Autoregressive order
- d = Differencing order
- q = Moving Average order

---

### SARIMA

Used for the CPI forecasting dataset.

General notation:

```
SARIMA(p,d,q)(P,D,Q)m
```

where

- Seasonal autoregressive terms
- Seasonal differencing
- Seasonal moving average terms
- Seasonal period

---

# Model Diagnostics

Each fitted model was evaluated using residual analysis to ensure that assumptions were satisfied.

Diagnostic procedures included:

- Residual plots
- Residual ACF
- Ljung-Box Test
- Normality assessment
- White noise verification

---

# Forecasting

Both projects generate future forecasts with confidence intervals.

Forecast outputs include:

- Point forecasts
- 80% Confidence Interval
- 95% Confidence Interval

These forecasts demonstrate the practical application of ARIMA-based models for economic and financial time series prediction.

---

# Technologies Used

- **R**
- R Markdown
- forecast
- tseries
- ggplot2
- zoo
- stats
- dplyr

---

# Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/time-series-forecasting.git

cd time-series-forecasting
```

Install the required R packages:

```r
install.packages(c(
  "forecast",
  "tseries",
  "ggplot2",
  "zoo",
  "dplyr"
))
```

---

# Running the Project

Open either R Markdown file in RStudio and run:

```r
MA641 Research Project.Rmd
```

or

```r
MA641 Research Project(Seasonal).Rmd
```

The notebooks perform:

- Data preprocessing
- Statistical analysis
- Model fitting
- Forecast generation
- Visualization

---

# Key Learning Outcomes

This project demonstrates practical experience with:

- Time series data preprocessing
- Stationarity analysis
- Statistical hypothesis testing
- ARIMA modeling
- Seasonal ARIMA modeling
- Time series diagnostics
- Forecast evaluation
- Economic and financial forecasting using R

---

# Future Improvements

Potential extensions include:

- Prophet forecasting
- Exponential Smoothing (ETS)
- TBATS models
- Machine Learning approaches (XGBoost)
- Deep Learning models (LSTM, GRU)
- Hybrid forecasting models
- Automated hyperparameter optimization

---

# References

- Box, G. E. P., Jenkins, G. M., Reinsel, G. C., & Ljung, G. M. *Time Series Analysis: Forecasting and Control*.
- Hyndman, R. J., & Athanasopoulos, G. *Forecasting: Principles and Practice*.
- R `forecast` Package Documentation.
- Federal Reserve Economic Data (FRED).
- Historical Gold Spot Price Data (XAU/USD).

---

## Author

**Yash Bhosale**

Master of Science in Data Science  
Stevens Institute of Technology

---

If you found this repository useful, consider giving it a ⭐.
