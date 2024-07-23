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

![Portfolio Optimization](https://github.com/user-attachments/assets/e8cac23c-89d6-4f37-8705-d2e232fc9d76)
![Portfolio Optimization](https://github.com/user-attachments/assets/da89b773-f9e6-442a-9473-7945a4ec6f44)

5. **Performance Analysis**:
   - **Year-End Performance**: Analyzed P/L as of December 31, 2023, compared to S&P 500 and TSX 60.

## Summary

This project integrates machine learning with traditional financial analysis to develop a data-driven investment strategy. It includes:

- **Detailed Portfolio Composition**: Breakdown of selected stocks and metrics.
- **Risk Metrics**: Analysis of volatility and expected returns.
- **Comparative Performance**: Evaluation against major market indices.

The combination of XGBoost for stock selection and careful portfolio construction provides a robust framework for optimized financial performance.



# Predictive-Portfolio-Optimization

## Introduction
This project aims to construct and manage a multi-asset portfolio using advanced machine-learning techniques to predict and select top-performing stocks. The focus is on optimizing the equity portion of the portfolio by leveraging historical financial data and predictive models to identify potential future winners in the stock market.

## Data Collection and Integration

Streamlining Data Sources to Build One Comprehensive Dataset for ML Model Input

Exploring Data Sources:
In the quest to construct a robust predictive model, a critical first step is to gather and integrate diverse datasets that can offer insights into stock performance. Our approach involves collecting a variety of financial and market data from reliable sources such as Yahoo Finance. The key data files include:

1. Company Financial Ratios: These ratios, such as price-to-earnings (P/E), return on equity (ROE), and debt-to-equity (D/E), provide insight into a company's financial health and operational efficiency.

2. Sector Information: Understanding the sector classification of each stock allows us to analyze industry trends and sector-specific dynamics, which can influence stock performance.

3. Market Capitalization Data: Market cap is a key indicator of a company's size and market value, affecting investment strategies and risk assessment.

4. Stock Returns Data: Historical stock returns are crucial for analyzing past performance and estimating future price movements.



![image](https://github.com/user-attachments/assets/33e306d8-3f27-4d9b-814f-970a0b690002)


## Exploratory Data Analysis (EDA)

With the comprehensive dataset in hand, we conducted an exploratory data analysis to uncover meaningful patterns and relationships that can guide our predictive modeling efforts. The EDA focused on several key areas:

1. Sector Information: We began by analyzing the distribution of stocks across different sectors. This provided insights into sector-specific trends and variances. For instance, we identified which sectors showed higher volatility or consistent performance over time. Understanding these patterns is crucial for sector-specific stock selection and risk management.

2. Past 12 Months Returns: We calculated and analyzed the past 12 months' returns for stocks within each sector to assess their performance trends. This analysis helped us identify sectors with strong momentum and those facing challenges. By comparing historical returns, we can pinpoint sectors that have historically outperformed or underperformed the market, which can inform future investment strategies.

3. Correlation Analysis: We performed a correlation analysis to identify relationships between different financial metrics, such as equity_invcap and capital_ratio . This analysis highlighted potential dependencies and interactions between variables, revealing insights into which factors are most closely linked with stock returns. Understanding these correlations allows us to better model the factors driving stock performance.

4. Autocorrelation Analysis: Finally, we conducted an autocorrelation analysis to examine the persistence of stock returns over time. This analysis helped us identify patterns and predictability in the time series data of stock returns. Recognizing autocorrelations is essential for developing time series models that can better forecast future stock movements.

The insights gained from EDA provide a deeper understanding of the data landscape, highlighting important variables and trends that inform our modeling approach. This analysis lays the groundwork for selecting relevant features and refining our machine learning models, ultimately enhancing our ability to predict future stock performance.

![image](https://github.com/user-attachments/assets/3b77c078-1c1a-499d-ac35-0b2cf7129cab)
![image](https://github.com/user-attachments/assets/77a4439a-9cd3-436a-b2d7-4be18826e68d)



## Data Cleaning and Preprocessing
To ensure the accuracy and effectiveness of our machine learning model, we meticulously cleaned and preprocessed the dataset. This process involved several key steps:

1. Removal of Duplicates and Irrelevant Columns: We started by identifying and removing duplicate records to prevent redundancy and ensure data integrity. Irrelevant columns that did not contribute to our analysis were also eliminated to streamline the dataset and focus on pertinent variables.

2. Feature Engineering: We enhanced the dataset by creating new features that add value to our analysis. For example, we extracted 'Month' and 'Year' features from the 'Public Date' to facilitate time-series analysis and improve model performance by capturing temporal trends.

3. Scaling: We applied Min-Max scaling to the monthly return data to normalize the range of the features and ensure that they contribute equally to the model training process. This scaling is crucial for models sensitive to the magnitude of input features.

4. Handling Missing Values: Missing values were addressed using several strategies to maintain data quality. We employed custom backfilling techniques. Additionally, where feasible, we filled missing values using data sourced from Yahoo Finance to enrich the dataset. In cases where missing values were unavoidable, we opted to leverage XGBoost's inherent ability to handle missing data, allowing the model to manage these gaps during the training phase.

5. Managing Outliers: Outliers were handled separately using the Z-score method, which involves calculating the standard score for each data point and identifying those that fall outside a specified threshold. These extreme values were addressed to prevent skewed analyses and maintain dataset robustness.

Through these data cleaning and preprocessing steps, we transformed our raw data into a well-structured and refined dataset, ready for input into our machine learning models. 




![image](https://github.com/user-attachments/assets/928ac895-7b44-4022-b832-d4102a3fa71b)
![image](https://github.com/user-attachments/assets/ec381606-c40c-4191-9f99-fdf680fd2e04)



## Model Building Journey
The diagram below outlines the structured approach undertaken to develop a predictive model for financial performance, specifically for stock selection. The process is divided into five key stages:

1. Labelling the Target Variable: The journey begins by defining the target variable, which is based on forward 3-month returns. Percentile thresholds are established, with the upper (70th percentile) and lower (30th percentile) thresholds calculated for each month’s returns. These thresholds are crucial for categorizing stocks into performance brackets.

2. Deciding the Rolling Window: A series of rolling windows with various lookback periods (3, 6, 12, 18, 24, 36, and 48 months) were tested to determine the optimal time frame for model performance. The current best-performing window is a combination of 6-month and 36-month lookbacks, achieving a cross-validated AUC score of 76.2%. This stage is critical for identifying the most effective historical data range for accurate predictions.

3. Moving-Window Feature Analysis: Using the final model from the previous step, we perform a moving-window analysis by dividing the dataset into equal 3-year slices. This analysis helps evaluate the model’s performance across different time periods and ensures that the model remains robust and relevant over time.

4. Modelling Pipeline: Each 3-year slice is subjected to min-max scaling based on monthly and lookback window data to normalize the features. The XGBoost algorithm is then applied to predict forward 3-month returns. Enhanced performance metrics were observed when the model was scaled on the lookback window, demonstrating the importance of proper feature scaling.

5. Observing Best & Worst Performers: Two distinct models are created to classify stocks into best and worst performers. With a classification threshold of 0.5, the models identified 21 tickers as best performers and 110 tickers as worst performers. This classification allows for targeted investment strategies and portfolio optimization.

This systematic approach ensures a thorough and effective development of a predictive model for financial performance, providing valuable insights for stock or investment selection purposes.

![image](https://github.com/user-attachments/assets/8b876d02-f531-43d0-844f-ef5065c8ff1a)

## Predictive Model Performance and Feature Importance Analysis
This analysis provides a comprehensive overview of the predictive model's performance and key feature importance across various time periods. Below is a detailed breakdown:

1. Model Performance Over Time: 
The analysis examines the model’s performance across six 3-year periods from 2003 to 2021. Two key performance metrics are evaluated for each period:

a. AUC-ROC Score: This metric ranges from 0.405 to 0.703, with the highest score recorded in the most recent period (2018-2021). The AUC-ROC score measures the model’s ability to distinguish between positive and negative classes, with higher scores indicating better performance.

b. F1 Score: This score ranges from 0.081 to 0.394. The F1 Score is a measure of the model’s accuracy in classifying the positive class, considering both precision and recall. There is no consistent correlation between the AUC-ROC score and the F1 Score, indicating variations in the model’s performance across different metrics.

Overall, the model's performance shows significant fluctuations over time, with the best AUC-ROC score achieved in the most recent period and the worst during 2012-2015.

2. Feature Importance Analysis
A bar chart displays the top 30 features ranked by their aggregate importance across all six time segments. Key findings include:
Top Features: The most influential features identified are: return,past_return_12m, pb (Price-to-Book ratio),bm (Book-to-Market ratio), pe (Price-to-Earnings ratio)
Feature Importance Trend: The chart illustrates a decreasing trend in feature importance, with the top features showing significantly higher importance compared to those lower in the ranking.

3. Overall Insights
The analysis reveals that AUC-ROC scores vary between 0.42 and 0.70 across the six time segments, indicating considerable variability in the model’s predictive accuracy over time. This fluctuation suggests that the model’s effectiveness in predicting "forward 3-month returns" may be influenced by changing market conditions or other temporal factors.

![image](https://github.com/user-attachments/assets/7d4f7a93-1b41-446f-9b5a-b7b021899c93)





## ML-Driven Portfolio Optimization and Performance Analysis

#### Stock Selection
Machine Learning Model: Employed an XGBoost Classifier to predict top-performing stocks. The model was trained using historical data spanning from 2003 to 2022.
Feature Selection: The model utilized features such as financial ratios, past returns, and sector information to classify stocks into potential high performers.
#### Portfolio Construction
Equity Portfolio: Constructed an equal-weighted portfolio comprising 21 top-performing stocks, with each stock allocated 4.8% of the total portfolio value as of December 31, 2022.
Metrics Presented: For each stock, the following information was detailed: 
Market Capitalization (Market-Cap),
Market Beta,
12-Month Volatility,

#### Multi-Asset Allocation
Diversification: Expanded the portfolio to include not only stocks but also a selection of bond ETFs and commodity ETFs, achieving a balanced multi-asset portfolio.
#### Optimization
Objective: The primary goal was to minimize expected volatility while maximizing expected returns.
Constraints: 1. The stock portion of the portfolio was maintained at a minimum of 50%.
             2. The bond ETF portion was kept at a minimum of 10%.
Portfolio Value: Assumed a starting portfolio value of $10 million.

![image](https://github.com/user-attachments/assets/e8cac23c-89d6-4f37-8705-d2e232fc9d76)
![image](https://github.com/user-attachments/assets/da89b773-f9e6-442a-9473-7945a4ec6f44)

![image](https://github.com/user-attachments/assets/12cd4a26-359a-4661-817e-c123593f461a)


![image](https://github.com/user-attachments/assets/be5d6d75-0dba-491c-ba0a-ea8defac3a97)


#### Performance Analysis
1. Year-End Performance: Analyzed the portfolio's performance as of December 31, 2023, including a comparison with major indices such as the S&P 500 and TSX 60.
2. Return on Investment: Evaluated the year-end profit and loss (P/L) to assess the portfolio’s effectiveness relative to benchmarks.

## Summary
This project demonstrates how machine learning can be effectively integrated with traditional financial analysis to create a data-driven investment strategy. It includes:

1. Detailed Portfolio Composition: Breakdown of the selected stocks and their respective metrics.
2. Risk Metrics: Analysis of portfolio volatility and expected returns.
3. Comparative Performance: Evaluation of portfolio performance against leading market indices.

The combination of XGBoost for stock selection and careful portfolio construction provides a robust framework for achieving optimized financial performance.












