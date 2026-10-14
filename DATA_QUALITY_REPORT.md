# Bitcoin Dataset Quality Assessment Report

**Project:** Bitcoin Price Forecasting and Data Analysis  
**Author:** Muhammad Adjie Daud  
**Data Source:** Yahoo Finance BTC-USD historical data

## 1. Assessment Overview

This report documents the initial quality assessment of the historical Bitcoin price dataset selected for this project.

The assessment focuses on dataset structure, observation period, missing values, duplicate records, chronological ordering, and basic numerical consistency.

## 2. Dataset Summary

| Attribute | Result |
|---|---|
| Asset | Bitcoin (BTC) |
| Trading Pair | BTC-USD |
| Observation Period | January 1, 2020 – May 10, 2026 |
| Data Frequency | Daily |
| Number of Observations | 2,322 |
| Number of Columns | 7 |
| Data Format | Excel |
| Source Reference | https://finance.yahoo.com/quote/BTC-USD/history/ |

## 3. Dataset Structure

The dataset contains the following columns:

| Column | Description |
|---|---|
| Date | Date of the observation |
| Adj Close | Adjusted closing price |
| Close | Closing price |
| High | Highest recorded price |
| Low | Lowest recorded price |
| Open | Opening price |
| Volume | Recorded trading volume |

## 4. Data Quality Findings

The initial assessment identified the following results:

| Quality Check | Result |
|---|---|
| Missing values | None detected |
| Duplicate dates | None detected |
| Missing calendar dates | None detected within the stated observation period |
| Negative numeric values | None detected |
| OHLC consistency | All records passed basic price consistency checks |
| Adj Close and Close | Equal across all observations |
| Date ordering | Descending; chronological sorting is required before time-series analysis |

These findings describe the initial checks performed on the selected file. They do not independently establish the accuracy of every market price against the external source.

## 5. Descriptive Statistics

The following preliminary statistics were obtained from the dataset's Close column:

| Statistic | Value |
|---|---:|
| Minimum closing price | USD 4,970.79 |
| Maximum closing price | USD 124,752.53 |
| Mean closing price | USD 48,814.77 |
| Median closing price | USD 42,237.92 |

The minimum closing price occurred on March 12, 2020, while the maximum occurred on October 6, 2025.

These statistics describe historical observations and do not represent future price estimates.

## 6. Data Preparation Recommendations

Before conducting forecasting analysis, the following procedures should be applied and documented:

1. Sort records chronologically from oldest to newest.
2. Confirm that the date column is recognized as a date field.
3. Verify numerical data types and price units.
4. Select the target variable according to the research methodology.
5. Preserve the original dataset and document any transformations.
6. Validate the data again after preprocessing.

No imputation should be reported as necessary unless subsequent checks identify missing values.

## 7. Limitations

This assessment covers basic data quality checks. Further validation may be required to assess extreme market movements, source accuracy, data provenance, and suitability for a specific forecasting model.

The observation period ends on May 10, 2026. No later dates are included in this selected dataset.

## 8. Project Status

**Status:** Initial dataset quality assessment documented.

The dataset is ready for further exploratory data analysis, subject to chronological sorting and verification of the final research preprocessing procedure.

## 9. Conclusion

The selected dataset contains 2,322 daily observations and seven columns. The initial checks detected no missing values, duplicate dates, missing calendar dates, or negative numeric values.

These results provide a foundation for exploratory data analysis and subsequent time-series forecasting work. All later transformations and model results should be documented using verified outputs.
