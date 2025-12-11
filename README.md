# Time Series Analysis of the Blitz Rating on Lichess for ArturoArias

**By:** Arturo Alfredo Arias Aguilar

**Course:** Time Series

**Program:** Data Science Specialization

**Institution:** Data Science Research Peru

**Date:** June 2025

## Overview

This repository contains a complete time series analysis of my Blitz rating history on Lichess. The project applies classical statistical techniques to explore, model, and forecast the behavior of competitive chess rating data. The analysis includes decomposition, stationarity testing, smoothing methods, and ARIMA modeling to assess both short-term dynamics and long-term trends.

The notebook serves as an academic and practical demonstration of time series modeling within the context of real-world user-generated data.

## Objectives

- Extract Blitz rating history from the Lichess API.
- Explore the series through visualization and descriptive statistics.
- Decompose the time series into trend, seasonality, and residual components.
- Assess stationarity using ACF, PACF, variogram, and Dickey–Fuller tests.
- Apply smoothing techniques (moving average, SES, Holt).
- Fit and compare ARIMA models (manual selection and `auto_arima`).
- Evaluate model performance and discuss forecasting implications.

## Methods and Techniques

The project implements the following methods:

### 1. Data Extraction
- Rating history retrieved directly from the Lichess API.
- Filtering and preparation of Blitz mode data.

### 2. Exploratory Analysis
- Time series visualization
- Trend and volatility inspection
- Summary statistics

### 3. Classical Decomposition
- Additive decomposition with a 30-day period
- Identification of long-term trend and seasonal patterns

### 4. Stationarity Diagnostics
- ACF and PACF analysis
- Variogram assessment
- Augmented Dickey–Fuller test
- First-order differencing

### 5. Smoothing Models
- Centered Moving Average (MA)
- Simple Exponential Smoothing (SES)
- Holt’s method (additive trend)

### 6. ARIMA Modeling
- Manual grid search with walk-forward validation
- Automated model selection using `auto_arima`
- Forecast comparison and interpretation

## Tools and Libraries

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Statsmodels  
- pmdarima  
- scikit-learn  

## Key Findings (Summary)

- The Blitz rating series exhibits a combination of trend, weak seasonality, and noise.
- Stationarity tests confirm that the original series is non-stationary, requiring first-order differencing.
- Smoothing methods capture different aspects of the series, with SES and Holt adapting well to level changes.
- Manual ARIMA selection favored AR(2), while `auto_arima` selected ARIMA(1,0,0) based on AIC.
- Forecasting performance depends on volatility patterns and chosen methodology.
