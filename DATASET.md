# Bitcoin Historical Dataset Documentation

**Project:** Bitcoin Price Forecasting & Data Analysis  
**Author:** Muhammad Adjie Daud

## 1. Dataset Overview

This document describes the historical Bitcoin (BTC) price data intended for analysis and time-series forecasting.

The dataset documentation will cover its source, structure, observation period, data quality, and preprocessing procedures.

## 2. Data Source

- **Asset:** Bitcoin (BTC)
- **Trading pair:** BTC-USD
- **Source:** Yahoo Finance historical market data
- **Data frequency:** Daily
- **Start date:** January 1, 2020
- **End date:** May 10, 2026
- **Number of observations:** 2,322 daily records
- **Number of columns:** 7

Source: https://finance.yahoo.com/quote/BTC-USD/history/

## 3. Dataset Structure

The original dataset may contain the following columns:

| Column | Description |
|---|---|
| Date | Observation date |
| Open | Opening price in USD |
| High | Highest price in USD |
| Low | Lowest price in USD |
| Close | Closing price in USD |
| Adj Close | Adjusted closing price, if available |
| Volume | Trading volume |

The actual columns will be confirmed by inspecting the original data file.

## 4. Data Quality Checks

The following checks are planned:

- Check for missing values.
- Identify duplicate records.
- Verify date formats and chronological order.
- Inspect invalid or inconsistent numerical values.
- Confirm the dataset's observation period.
- Verify the price variable used in the analysis.

## 5. Data Preprocessing

Any data cleaning, filtering, transformation, or normalization will be documented after reviewing the original dataset.

Only procedures actually performed will be reported.

## 6. Limitations

Historical market data describes past observations and does not guarantee future Bitcoin price movements. Data sources, missing observations, and preprocessing choices may affect the analysis.

## 7. Project Status

**Status:** Dataset selected; data analysis and research documentation in progress.

The selected dataset contains 2,322 daily Bitcoin price observations covering January 1, 2020, through May 10, 2026.

Data quality findings, preprocessing procedures, descriptive statistics, visualizations, and forecasting results will be documented based on the inspected dataset and verified analytical results.
