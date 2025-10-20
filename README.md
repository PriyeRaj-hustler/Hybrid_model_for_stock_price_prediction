# Hybrid Model for Smarter Stock Predictions 📈

---

## Overview

Predicting stock market movements is notoriously challenging due to the multitude of factors influencing prices. This project tackles this challenge by developing a **hybrid prediction model**. Recognizing that stock prices are driven by both historical performance (numerical data) and market sentiment (often reflected in news), this model integrates both types of analysis for a more comprehensive and potentially more accurate forecast.

The model specifically focuses on the **BSE SENSEX**, a major Indian stock market index, using historical price data combined with sentiment extracted from **Times of India** news headlines spanning from 2001 to 2020.

---

## Project Goals

* To design and implement a hybrid predictive model combining time-series analysis of stock prices with sentiment analysis of relevant news data.
* To evaluate the effectiveness of this hybrid approach compared to using numerical data alone (implied).
* To achieve a high degree of accuracy in predicting BSE SENSEX movements, quantified using the R2 score metric.

---

## Methodology

### 1. Numerical Analysis 📊
* Historical daily stock data for the **BSE SENSEX** (Open, High, Low, Close, Volume) from January 2001 to December 2020 was collected (likely using `yfinance` as per the notebook context).
* This time-series data was pre-processed, likely involving normalization and potentially feature engineering (e.g., rolling averages, although not explicitly stated in the summary).
* Appropriate time-series forecasting techniques (like LSTM, as suggested by the notebook context) were applied to model and predict future closing prices based on past price movements.

### 2. Sentiment Analysis 📰
* A large dataset of news headlines from the **Times of India** (2001-2020) was utilized.
* Sentiment scores (compound, positive, negative, neutral) were calculated for the aggregated headlines of each day using a sentiment analysis tool (like VADER, as per the notebook context). This process quantifies the overall mood or sentiment expressed in the news for a given day.

### 3. Hybrid Model Integration 🤝
* The historical stock price data and the calculated daily sentiment scores were combined into a single dataset, aligned by date.
* This combined dataset, containing both numerical price features and sentiment features, was used to train the final predictive model (an LSTM network, based on the notebook context). The model learns patterns from both the price history and the sentiment shifts to make its predictions.

---

## Results & Evaluation

* The performance of the hybrid model was evaluated using the **Coefficient of Determination (R2 score)** on a test dataset.
* The model achieved an **R2 score of 0.98**.
* An R2 score close to 1.0 indicates that the model explains a very high proportion of the variance in the target variable (stock price), suggesting a strong predictive capability and a good fit to the data. This impressive result highlights the potential benefit of incorporating sentiment analysis alongside traditional numerical methods for stock prediction. ✅

---

## Data Sources

* **Stock Prices:** BSE SENSEX data obtained via `yfinance`.
* **News Headlines:** Times of India News Headlines dataset (2001-2020).

---

*(Note: Specific model architecture details like LSTM layers, dropout rates, optimizers, etc., would typically be included here or in the accompanying code/notebook.)*
