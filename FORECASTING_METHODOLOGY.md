# LSTM Forecasting Methodology for Bitcoin Prices

**Author:** Muhammad Adjie Daud  
**Program:** Information Systems, Universitas Nusa Putra  
**Project:** Bitcoin Price Forecasting & Data Analysis

## 1. Objective

This document describes the Long Short-Term Memory (LSTM) approach used in the Bitcoin price forecasting research. The goal is to document the modeling workflow, forecast setup, evaluation metrics, and reported comparison results in a reproducible and transparent way.

## 2. Data Used

The source dataset is the selected daily BTC-USD historical price file covering **January 1, 2020, through May 10, 2026**. It contains **2,322 daily observations** and seven columns: `Date`, `Adj Close`, `Close`, `High`, `Low`, `Open`, and `Volume`.

Related documentation:

- [Dataset Documentation](DATASET.md)
- [Data Quality Assessment Report](DATA_QUALITY_REPORT.md)
- [Exploratory Data Analysis Report](EDA_REPORT.md)
- [Historical Closing Price Chart](bitcoin_historical_closing_price.png)

## 3. Why LSTM?

LSTM is a recurrent neural network architecture designed to learn patterns across ordered sequences. Its memory state and gating mechanisms help the model represent temporal dependencies in sequential data. This makes LSTM a candidate method for modeling patterns in historical time-series data such as Bitcoin prices.

Model performance must be assessed against held-out observations and suitable error metrics; the model's use does not guarantee accurate future prices.

## 4. Forecasting Setup

The research materials available for this project specify the following setup:

| Setting | Value |
|---|---|
| Main model | LSTM |
| Look-back window | 3 months |
| Forecast horizon | 24 monthly forecast values |
| Forecast period | 2027–2028 |
| Target | Bitcoin price / closing-price series |

The source file contains daily observations, while the reported forecasting setup uses a monthly look-back and 24-month horizon. The daily-to-monthly aggregation rule should match the procedure used in the original experiment; it is not inferred in this document.

## 5. Modeling Workflow

### 5.1 Data Preparation

1. Use the selected BTC-USD historical dataset and retain the documented observation period.
2. Sort observations chronologically from oldest to newest before sequence modeling.
3. Select the closing-price series as the forecasting target, consistent with the research objective.
4. Prepare the monthly series and the three-month look-back sequences according to the original experiment's preprocessing procedure.
5. Apply the normalization procedure used in the research workflow and retain the parameters needed to transform forecasts back to the price scale.

### 5.2 Sequence Construction

A three-month look-back means that the model uses the preceding three monthly observations as input context. This sequence is used to learn temporal patterns for the forecasting task. The forecasting horizon specified in the research is 24 monthly values for 2027–2028.

### 5.3 LSTM Model

The LSTM model learns relationships within the prepared sequences by updating its internal memory and gate states. The specific layer count, number of units, activation functions, optimizer, loss function, epoch count, batch size, and train-validation-test partition are not stated here because their exact values have not been verified from the original model configuration. These implementation details should be copied from the final experiment record rather than assumed.

### 5.4 Forecast Output

The intended output is a sequence of 24 monthly Bitcoin price estimates for 2027–2028. Forecast values should be reported with their corresponding month labels and the same price unit used by the source series. Forecasts are estimates, not guarantees of future market behavior.

## 6. Evaluation Metrics

The research comparison used the following error metrics:

- **Mean Absolute Error (MAE):** the average absolute difference between actual and predicted values.
- **Root Mean Squared Error (RMSE):** the square root of the average squared prediction error; larger errors receive greater weight.
- **Mean Absolute Percentage Error (MAPE):** the average absolute percentage error, expressed as a percentage.

Lower values indicate smaller errors for the evaluated data and setup. Comparisons are meaningful only when models are evaluated on comparable observations and under a consistent evaluation procedure.

## 7. Reported Model Comparison

The following values are the model-performance results previously supplied for this research project.

| Model | MAE (USD) | RMSE (USD) | MAPE |
|---|---:|---:|---:|
| ARIMA(2,1,2) baseline | 3,847 | 4,821 | 4.23% |
| LSTM selected model | 1,692 | 2,134 | 1.89% |

For these reported results, the LSTM model has lower MAE, RMSE, and MAPE than the ARIMA(2,1,2) baseline. The table records the reported comparison; it does not independently reproduce the training run.

## 8. Interpretation and Limitations

The reported comparison favors LSTM on the three listed error metrics. However, cryptocurrency prices are volatile, and historical forecasting performance does not guarantee future accuracy. The evaluation period, preprocessing procedure, and modeling configuration affect the interpretation of model errors.

This repository documents an academic research project and is not financial or investment advice.

## 9. Reproducibility Details

For full reproducibility, the final research materials should specify the exact monthly aggregation rule, normalization method, data split dates or ratios, LSTM architecture, training parameters, and the observations used to calculate MAE, RMSE, and MAPE. Those details should be added from the original, verified experiment settings rather than inferred.

## 10. Project Status

**Status:** Methodology documentation in progress; the reported model-comparison metrics are documented from the research materials previously supplied.

The repository will be updated with final configuration details and forecast-result artifacts when they are matched to the final experiment record.
