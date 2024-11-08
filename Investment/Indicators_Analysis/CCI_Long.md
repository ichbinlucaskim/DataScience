# Commodity Channel Index

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1ThSTSB6WSD41NYitN-wsJLQOLgaaSDpT/view?usp=sharing)


## Introduction

- Abstract:

Analysis of the Intersection Points of Supply and Demand for Listed Stocks in the Korean Stock Market

- Background: 

Stock prices do not have a direct 1:1 correlation with corporate profits; ultimately, they follow the principles of supply and demand. This project started from the idea that if we can identify the peaks of demand (overbought) and the troughs of supply (oversold), we might be able to reduce investment risks.

- Objective: 

To verify how effectively the Commodity Channel Index (CCI), known as an overbought and oversold indicator, represents overbought and oversold conditions through backtesting with historical data.

## Methodology

- Tools and Technologies:
```
Python, Pandas, NumPy, Matplotlib
```

- Algorithms and Models:

```
Developed custom backtesting algorithm, CCI
```

Commodity Channel Index (CCI): Implemented the CCI to identify overbought and oversold conditions:


$$CCI = \frac{( \text{Typical Price} - \text{SMA} )}{0.015 \times \text{Mean Deviation}}$$

$\[
\text{Typical Price} = \frac{\text{High} + \text{Low} + \text{Close}}{3}
\]$

$\[
\text{Mean Deviation} = \frac{1}{N} \sum_{i=1}^{N} | \text{Typical Price}_i - \text{SMA} |
\]$



## Data Description

- Data Sources:

Collected 10 years of data from the Korean stock markets (KOSPI, KOSDAQ) via FnGuide and converted it into H5 files.

- Data Characteristics:

All stocks are composed of daily data, with the closing price of each day set as the price. The dataset consists only of stocks and ETFs listed on the market; futures and options are not included.

- Data Preprocessing:

In the Korean market, there is a daily limit of 30% on price increases and decreases. Therefore, outliers exceeding this limit were removed before analysis.

## Workflow

```
	1.	Import and Verify Data: Loaded the dataset and performed initial data validation.
	2.	Implement CCI: Calculated the CCI using the formula provided.
	3.	Set Trading Conditions: Established trading rules based on CCI thresholds.
	4.	Perform Backtesting: Executed backtesting over the historical data.
	5.	Review Results: Analyzed the performance metrics and outcomes.
```

## Results


