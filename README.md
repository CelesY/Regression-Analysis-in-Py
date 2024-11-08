# Financial Data Analysis with Python
This repository contains projects focused on financial data analysis using Python, covering various machine learning techniques.

## Projects
### Credit Card Fraud Detection
This project focuses on identifying fraudulent credit card transactions through the following steps:

Exploratory Data Analysis (EDA): Initial data exploration and basic statistical analysis.

Feature Engineering with PCA: Use of Principal Component Analysis (PCA) to clean the data and extract essential features.

Model Training with KNN-SMOTE: To address class imbalance, KNN-SMOTE is applied for synthetic sample generation. The results are compared to a standalone KNN model for classification performance.

Prediction with LSTM: LSTM is implemented for prediction, with evaluation using a confusion matrix.

### EMD-LSTM for Volatility Prediction in Stock Market
This project leverages the EMD-LSTM model for stock market volatility prediction:

EMD for Wavelet Decomposition: Empirical Mode Decomposition (EMD) is used to decompose the time series data into intrinsic mode functions, enhancing the LSTM model's ability to predict volatility. By capturing the underlying dynamics of market data, EMD aids in improving predictive accuracy.

Risk Assessment with VaR: Value at Risk (VaR) is used to evaluate model performance, providing a quantitative measure of potential financial risk.

Backtesting with Kupiec Method: The Kupiec method is applied to backtest the consistency of the VaR estimates, ensuring the reliability of the predictions.
