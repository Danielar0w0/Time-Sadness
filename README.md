# Time Series Analysis of Programming Technology Trends

A time series analysis project examining Python programming language adoption patterns using Stack Overflow question frequency data. This project applies classical statistical methods including SARIMA, ETS, and GARCH models to forecast technology trends and assess prediction uncertainty.

## Project Overview

This study analyzes temporal dynamics of technology usage patterns through rigorous time series analysis, focusing on Python programming language trends from 2009 onwards.

### Key Objectives
- **Trend Analysis**: Quantify long-term growth patterns in Python usage
- **Seasonality Detection**: Identify recurring patterns reflecting academic and industry cycles  
- **Forecasting**: Develop reliable predictive models for future Python usage trends
- **Model Comparison**: Evaluate SARIMA, ETS, and GARCH modeling approaches
- **Uncertainty Quantification**: Provide confidence intervals and bootstrap validation

## Repository Structure

```
Time-Sadness/
├── Time_Series.Rmd          # Main analysis R Markdown file
├── data.csv                 # Stack Overflow question count dataset
└── README.md                # This file
```

## Dataset

**Source**: [Kaggle - StackIndex Dataset](https://www.kaggle.com/datasets/aishu200023/stackindex)

**Description**: Monthly Stack Overflow question counts for various programming technologies and libraries from January 2009 onwards.

**Key Features**:
- **Temporal Coverage**: Monthly observations from 2009-present
- **Technology Scope**: Python, R, TensorFlow, scikit-learn, pandas, NumPy, and 70+ other technologies
- **Data Quality**: Aggregated monthly counts providing robust trend indicators
- **Global Representation**: Stack Overflow's international user base

## Methodology

### 1. Exploratory Data Analysis
- Time series visualization and decomposition
- Stationarity testing (ADF, KPSS, Phillips-Perron tests)
- Seasonal pattern identification
- Box-Cox transformation assessment

### 2. Model Development (Box & Jenkins Methodology)
- **SARIMA Models**: Systematic identification using ACF/PACF analysis
- **ETS Models**: Exponential smoothing with various error/trend/seasonal components
- **GARCH Models**: Volatility modeling for uncertainty quantification

### 3. Forecast Generation & Validation
- Train/test split (80%/20%) for out-of-sample validation
- Multiple accuracy metrics (RMSE, MAE, MAPE, MASE)
- Confidence interval analysis and coverage assessment
- Bootstrap methodology for non-parametric uncertainty quantification

### 4. Model Comparison & Selection
- Information criteria comparison (AIC, BIC)
- Forecast accuracy assessment
- Residual analysis and diagnostic evaluation
- Parameter significance testing

## Technical Requirements

### R Dependencies
```r
library(tidyverse)     # Data manipulation and visualization
library(forecast)      # Time series forecasting
library(tseries)       # Time series analysis and tests
library(ggplot2)       # Advanced plotting
library(lubridate)     # Date handling
library(gridExtra)     # Multiple plot arrangements
library(reshape2)      # Data reshaping
library(rugarch)       # GARCH modeling (optional)
```

### Installation
```r
# Install required packages
install.packages(c("tidyverse", "forecast", "tseries", "ggplot2", 
                   "lubridate", "gridExtra", "reshape2", "rugarch"))
```

## [Report](https://typst.app/project/rQmZ2s28TiOO4mIYLY98z9)