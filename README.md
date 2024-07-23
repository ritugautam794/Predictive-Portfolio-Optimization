# Predictive-Portfolio-Optimization

## Introduction

This project focuses on constructing and managing a multi-asset portfolio using advanced machine learning techniques to predict and select top-performing stocks. By leveraging historical financial data and predictive models, the goal is to optimize the equity portion of the portfolio and make data-driven investment decisions.

## Data Collection and Integration

**Streamlining Data Sources to Build One Comprehensive Dataset for ML Model Input**

To build a robust predictive model, we gathered and integrated various financial and market data from reliable sources like Yahoo Finance. The datasets include:

- **Company Financial Ratios**: Provides insights into a company's financial health (e.g., P/E ratio, ROE, D/E ratio).
- **Sector Information**: Helps analyze industry trends and sector-specific dynamics.
- **Market Capitalization Data**: Indicates a company's size and market value.
- **Stock Returns Data**: Essential for analyzing past performance and estimating future movements.

![Data Collection and Integration](https://github.com/user-attachments/assets/33e306d8-3f27-4d9b-814f-970a0b690002)

## Exploratory Data Analysis (EDA)

**Uncovering Patterns and Relationships for Predictive Modeling**

Our exploratory data analysis (EDA) focused on several key areas:

1. **Sector Information**: Analyzed stock distribution across sectors to identify trends and performance variances.
2. **Past 12 Months Returns**: Assessed historical returns to identify strong and weak sectors.
3. **Correlation Analysis**: Identified relationships between financial metrics (e.g., equity_invcap, capital_ratio) to reveal dependencies.
4. **Autocorrelation Analysis**: Examined return persistence to predict future movements.

These insights guide feature selection and model refinement, enhancing prediction accuracy.

![EDA](https://github.com/user-attachments/assets/3b77c078-1c1a-499d-ac35-0b2cf7129cab)
![EDA](https://github.com/user-attachments/assets/77a4439a-9cd3-436a-b2d7-4be18826e68d)

## Data Cleaning and Preprocessing

**Preparing Data for Machine Learning Models**

Key steps in cleaning and preprocessing included:

1. **Removal of Duplicates and Irrelevant Columns**: Ensured data integrity by eliminating redundancy and non-contributory columns.
2. **Feature Engineering**: Created new features like 'Month' and 'Year' from 'Public Date' for enhanced time-series analysis.
3. **Scaling**: Applied Min-Max scaling to normalize features, ensuring balanced model training.
4. **Handling Missing Values**: Used backfilling techniques and data from Yahoo Finance; leveraged XGBoost's handling of missing values.
5. **Managing Outliers**: Addressed extreme values using the Z-score method to maintain robustness.

![Data Cleaning](https://github.com/user-attachments/assets/928ac895-7b44-4022-b832-d4102a3fa71b)
![Data Cleaning](https://github.com/user-attachments/assets/ec381606-c40c-4191-9f99-fdf680fd2e04)

## Model Building Journey

**A Structured Approach to Predictive Modeling**

The model-building process consists of five stages:

1. **Labelling the Target Variable**: Defined thresholds for forward 3-month returns using percentile calculations.
2. **Deciding the Rolling Window**: Tested various lookback windows (3-48 months) to determine the optimal period, with a 6/36-month window achieving the best AUC score of 76.2%.
3. **Moving-Window Feature Analysis**: Evaluated model performance across different 3-year slices to ensure robustness.
4. **Modelling Pipeline**: Applied XGBoost after min-max scaling on monthly and lookback window data.
5. **Observing Best & Worst Performers**: Classified stocks into best (21 tickers) and worst performers (110 tickers) based on a 0.5 classification threshold.

![Model Building](https://github.com/user-attachments/assets/8b876d02-f531-43d0-844f-ef5065c8ff1a)

## Predictive Model Performance and Feature Importance Analysis

**Evaluating Model Accuracy and Key Features**

1. **Model Performance Over Time**:
   - **AUC-ROC Score**: Ranges from 0.405 to 0.703, with the highest score in the most recent period (2018-2021).
   - **F1 Score**: Varies from 0.081 to 0.394, with no consistent correlation to AUC-ROC scores.

2. **Feature Importance Analysis**:
   - **Top Features**: Identified key features such as return, past_return_12m, pb (Price-to-Book ratio), bm (Book-to-Market ratio), and pe (Price-to-Earnings ratio).
   - **Importance Trend**: Notable decrease in feature importance with top features showing higher significance.

3. **Overall Insights**: AUC-ROC scores varied from 0.42 to 0.70, indicating model performance fluctuations influenced by market conditions.

![Model Performance](https://github.com/user-attachments/assets/7d4f7a93-1b41-446f-9b5a-b7b021899c93)

## ML-Driven Portfolio Optimization and Performance Analysis

**Creating and Evaluating a Multi-Asset Portfolio**

1. **Stock Selection**:
   - **Machine Learning Model**: XGBoost Classifier to predict top-performing stocks.
   - **Feature Selection**: Used financial ratios, past returns, and sector information.

2. **Portfolio Construction**:
   - **Equity Portfolio**: Equal-weighted portfolio with 21 top-performing stocks, each allocated 4.8% of the total value as of December 31, 2022.
   - **Metrics Presented**: Market Capitalization, Market Beta, and 12-Month Volatility.

3. **Multi-Asset Allocation**:
   - **Diversification**: Added bond ETFs and commodity ETFs to balance the portfolio.

4. **Optimization**:
   - **Objective**: Minimize volatility and maximize returns.
   - **Constraints**: Stock portion ≥ 50%, Bond ETF portion ≥ 10%.
   - **Portfolio Value**: Assumed starting value of $10 million.


![image](https://github.com/user-attachments/assets/e8cac23c-89d6-4f37-8705-d2e232fc9d76)
![image](https://github.com/user-attachments/assets/da89b773-f9e6-442a-9473-7945a4ec6f44)

![image](https://github.com/user-attachments/assets/12cd4a26-359a-4661-817e-c123593f461a)


![image](https://github.com/user-attachments/assets/be5d6d75-0dba-491c-ba0a-ea8defac3a97)


5. **Performance Analysis**:
   - **Year-End Performance**: Analyzed P/L as of December 31, 2023, compared to S&P 500 and TSX 60.

## Summary

This project integrates machine learning with traditional financial analysis to develop a data-driven investment strategy. It includes:

- **Detailed Portfolio Composition**: Breakdown of selected stocks and metrics.
- **Risk Metrics**: Analysis of volatility and expected returns.
- **Comparative Performance**: Evaluation against major market indices.

The combination of XGBoost for stock selection and careful portfolio construction provides a robust framework for optimized financial performance.










