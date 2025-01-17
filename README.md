# Predicting-Stock-Movements-Using-Sentiment-Analysis-and-Machine-Learning

## Overview
This project explores the relationship between sentiment in news headlines and stock price movements. Using a combination of historical stock data, sentiment analysis, and machine learning, it predicts whether the stock price will increase on the following day.

### Stocks Analyzed:
- **ONCO**
- **CNEY**
- **TNXP**
- **APLD**
- **KTTA**

### Project Duration:
Data spans from early 2021 to October 2024.

---

## Features

### 1. Data Extraction
- **Libraries Used:**
  - `yfinance`: Historical stock data.
  - `BeautifulSoup`: Web scraping for news headlines.
  - `pandas`: Data manipulation.
- **Outputs:**
  - Historical stock data for price trends.
  - News headlines related to each stock.

### 2. Sentiment Analysis
- **Libraries Used:** TextBlob and VADER.
- **Objective:** Classify news articles as Positive, Neutral, or Negative.
- **Results:**
  - Example sentiment scores:
    - **CNEY:** 0.34 (highest)
    - **TNXP:** 0.0011 (lowest)

### 3. Time Series Analysis
- Decomposed stock price time series into trend, seasonality, and residuals.
- Stationarity checked using the Augmented Dickey-Fuller (ADF) test.
- Autocorrelation plots used for ARIMA modeling insights.

### 4. Machine Learning Predictions
- **Model Used:** Random Forest Classifier.
- **Features:**
  - Moving averages (10-day and 20-day).
  - Sentiment scores.
  - Previous closing prices.
- **Results:**
  - RMSE values highlight prediction accuracy (e.g., ONCO: 17.44, APLD: 0.36).

### 5. Visualizations
- Sentiment distributions (bar charts).
- Time series plots for stock prices.
- Scatter plots comparing actual vs. predicted prices.

---

## Files
- **`Stock_Analysis_1.ipynb`**: Contains code for data extraction, sentiment analysis, and preprocessing.
- **`Stock_Analysis_2.ipynb`**: Includes time series analysis, machine learning, and visualization code.
- **`Predicting Stock Movements Using Sentiment Analysis and Machine Learning.pdf`**: Detailed project report.

---

## Conclusion
This project demonstrates the impact of sentiment analysis on stock price predictions. It highlights challenges such as stock volatility and suggests future work using advanced models like LSTM and granular sentiment data.
