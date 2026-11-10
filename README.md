# Pandas Time Series Analysis: US Light Vehicle Sales
Roadmap Project: https://roadmap.sh/projects/pandas-time-series

## About this project
A time series analysis of monthly US light vehicle sales data (FRED series
LTOTALNSA), covering January 1976 to September 2026 — 609 months of data.

## What the notebook does
- Loads the CSV into a Pandas DataFrame with pd.read_csv()
- Parses the date column with pd.to_datetime() and sets it as a DatetimeIndex
- Checks the data for missing months and confirms the dates are in order
- Creates date ranges with pd.date_range() and frequency strings (D, W, ME, MS, QE)
- Uses .resample() to build monthly, quarterly, and yearly totals
- Uses .shift() and .diff() to compare each month with the month before it
- Uses .rolling() to calculate a 12-month rolling mean
- Plots the original monthly series and the rolling mean on the same chart

## What I learned
How DatetimeIndex works, and how to use .resample(), .shift(), .rolling(),
and .diff(). Differencing is useful with sales and financial data because it
removes the long-term trend and shows only the period-to-period changes, so
unusual months stand out and the changes are easier to analyze and forecast.

## Files
- time_series.ipynb — the analysis notebook
- LTOTALNSA.csv — the dataset

## Data source
FRED (Federal Reserve Bank of St. Louis), series LTOTALNSA:
Total Light Vehicle Sales, thousands of units, monthly.

## Tools
Python, Pandas, NumPy, Matplotlib, Jupyter Notebook
