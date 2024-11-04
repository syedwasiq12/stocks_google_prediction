# stocks_google_prediction
This project aims to predict the daily closing prices of Google Inc. stock using historical data. The model leverages various deep learning architectures, including Temporal Convolutional Networks (TCN), Transformers, and Long Short-Term Memory (LSTM) networks, to achieve accurate and robust predictions. By experimenting with different sequence lengths, dilation rates, and model architectures, the project explores the effectiveness of these models in capturing temporal dependencies in stock price data.

1. Project Objective:
The primary goal is to forecast the daily closing stock prices of Google Inc. by analyzing historical data patterns and improving accuracy for potential investment-related decisions.
2. Data Preprocessing:
Missing values in the dataset are handled using forward-fill and backfill methods.
Holidays are excluded from the data to maintain consistency, focusing solely on relevant trading days.
3. Model Architectures and Experimentation:
Temporal Convolutional Network (TCN):

Utilized multiple configurations with varying dilation rates (1, 2, 4 and 1, 4, 8) and sequence lengths (50, 100, 200).
The best performance for TCN was achieved with a sequence length of 100 and a dilation rate sequence of 1, 2, 4, with results as follows:
Train Score: MSE = 0.00019, RMSE = 0.01
Validation Score: MSE = 0.00188, RMSE = 0.04
Test Score: MSE = 0.00267, RMSE = 0.05
Increasing sequence length to 200 showed diminished returns in performance, particularly on the test set​(stock_predictor).
Transformers:

Evaluated transformer models with different configurations, including 2-block architectures with 2 and 4 attention heads and varying head sizes (64, 128).
The best performance was observed with 2 heads and a sequence length of 200, achieving:
Train Score: MSE = 0.00007, RMSE = 0.01
Validation Score: MSE = 0.00161, RMSE = 0.04
Test Score: MSE = 0.00297, RMSE = 0.05
Performance decreased slightly when the head size was increased to 128​(stock_predictor).
Long Short-Term Memory (LSTM):

LSTM with a sequence length of 200 provided strong predictive performance:
Train Score: MSE = 0.00006, RMSE = 0.01
Validation Score: MSE = 0.00134, RMSE = 0.04
Test Score: MSE = 0.00212, RMSE = 0.05
Reducing the sequence length to 50 resulted in improved training accuracy but did not significantly impact test performance​
