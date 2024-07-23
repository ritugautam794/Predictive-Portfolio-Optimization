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




![image](https://github.com/user-attachments/assets/470f4e52-e6a8-4f71-a3d2-d8c0cda25aa2)

![image](https://github.com/user-attachments/assets/7fad94e1-c62c-4455-9760-173a3b25e230)

## Exploratory Data Analysis (EDA)

With the comprehensive dataset in hand, we conducted an exploratory data analysis to uncover meaningful patterns and relationships that can guide our predictive modeling efforts. The EDA focused on several key areas:

1. Sector Information: We began by analyzing the distribution of stocks across different sectors. This provided insights into sector-specific trends and variances. For instance, we identified which sectors showed higher volatility or consistent performance over time. Understanding these patterns is crucial for sector-specific stock selection and risk management.

2. Past 12 Months Returns: We calculated and analyzed the past 12 months' returns for stocks within each sector to assess their performance trends. This analysis helped us identify sectors with strong momentum and those facing challenges. By comparing historical returns, we can pinpoint sectors that have historically outperformed or underperformed the market, which can inform future investment strategies.

3. Correlation Analysis: We performed a correlation analysis to identify relationships between different financial metrics, such as equity_invcap and capital_ratio . This analysis highlighted potential dependencies and interactions between variables, revealing insights into which factors are most closely linked with stock returns. Understanding these correlations allows us to better model the factors driving stock performance.

Autocorrelation Analysis: Finally, we conducted an autocorrelation analysis to examine the persistence of stock returns over time. This analysis helped us identify patterns and predictability in the time series data of stock returns. Recognizing autocorrelations is essential for developing time series models that can better forecast future stock movements.

The insights gained from EDA provide a deeper understanding of the data landscape, highlighting important variables and trends that inform our modeling approach. This analysis lays the groundwork for selecting relevant features and refining our machine learning models, ultimately enhancing our ability to predict future stock performance.



![image](https://github.com/user-attachments/assets/f4688d1a-021b-4eaf-b2a6-d4da9bae40b1)

![image](https://github.com/user-attachments/assets/3575aa32-a09e-4dbd-b8bc-83128a478980)

![image](https://github.com/user-attachments/assets/0c8d50af-5ebf-4199-b162-adca5273745f)

![image](https://github.com/user-attachments/assets/953057ef-eb92-4791-9d53-d9acf1bd9da1)

![image](https://github.com/user-attachments/assets/61ac1fda-dbd7-4ea7-988a-b35eebd3f3db)

![image](https://github.com/user-attachments/assets/a0ee58bf-d03a-4bb5-a945-3fe801e967cf)

![image](https://github.com/user-attachments/assets/be5d6d75-0dba-491c-ba0a-ea8defac3a97)

![image](https://github.com/user-attachments/assets/69bcd5fa-cc09-4600-b6ee-9123591f4efb)














