# Stock-Price-Prediction

## Project Overview

This project explores various machine learning models and their applications in predicting stock prices, specifically focusing on Apple Inc. (AAPL) stock data from 2015 to 2019. The models implemented include traditional time series models like ARIMA, advanced deep learning models like Long Short-Term Memory (LSTM) networks (with and without sentiment analysis), and Transformer architectures. Additionally, GPT-3 is employed to assess its viability in predicting stock prices using historical financial data.

## Features

- ARIMA Model: Applied to predict stock prices based solely on historical data.
- LSTM Model: Long Short-Term Memory networks used to capture time dependencies.
- LSTM + Sentiment: Incorporation of sentiment analysis from Twitter (now X) as an additional feature in the LSTM model.
- Transformer Model: Utilized both with single (Adjusted Close) and multi-feature inputs (including technical indicators like MA5, MA30, RSI).
- GPT-3 Model: Evaluates the predictive power of GPT-3 using only historical financial data.

```bash
/project-directory
│
├── /notebooks/               # Jupyter notebooks for model training, sentiment analysis, and comparison
│   ├── AAPL Sentiment Analysis.ipynb         # Sentiment analysis on Apple-related tweets.
│   ├── ARIMA.ipynb                          # ARIMA model for stock price prediction.
│   ├── Comparative Analysis.ipynb           # Comparison of model performances using various metrics.
│   ├── LSTM.ipynb                           # LSTM-based stock prediction model.
│   ├── LSTM + Sentiment.ipynb               # LSTM with sentiment analysis for stock prediction.
│   ├── Final Transformers (Adj Close).ipynb # Final Transformer model using only Adjusted Close Price for prediction.
│   ├── Final Transformers F7.ipynb          # Final Transformer model using 7 features for prediction.
│   ├── GPT-3 Stock Prediction (Adj Close).ipynb  # GPT-3 model using only Adjusted Close Price for prediction.
│   ├── GPT-3 Stock Prediction F4.ipynb      # GPT-3 model using Adjusted Close Price, MA(5), MA(30), and RSI for prediction.
│   └── GPT-3 Stock Prediction-2024.ipynb    # GPT-3 model for Adjusted Close Price prediction on 2024 test data.
│
├── /datasets/               # Datasets used in the project
│   ├── AAPL_Tweets_with_Sentiment.csv       # Apple tweets with sentiment scores.
│   ├── AAPL_Tweets.csv                      # Raw Apple-related tweets data.
│   └── Tweet.csv                            # General Twitter dataset related to financial tweets.
│
├── /model_weights/           # Model weights and trained model files
│   ├── Final Transformer Model - 7 features  # Transformer model weights and architecture for further analysis using 7 features.
│   └── Transformer Model - 1 feature         # Transformer model trained using only Adjusted Close Price (1 feature).
│
├── /gpt_predictions/         # GPT-3 predictions and results
│   └── predictions.csv                        # Actual and predicted scores using the GPT-3 model.
│
├── README.md                 # This file.

```


## Results

In summary:

Transformer models (particularly with multi-feature inputs) demonstrated the best overall performance, significantly outperforming ARIMA and LSTM models. 
Incorporating sentiment analysis in the LSTM model did not result in significant performance improvements, potentially due to the use of older data.
The GPT-3 model showed promising predictive capabilities, maintaining high performance even when tested on recent stock data.
