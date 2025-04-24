## Project title : Time Series Analysis of Daily Female Births in California, 1959

Technologies Used: Libraries: Pandas, Matplotlib, Seaborn, sklearn, statsmodels, --- Languages: Python.

**Project Overview:** The aim of this project is to analyze the daily female birth data from California in 1959, identifying trends, seasonal patterns, and any significant fluctuations over the time. The analysis will explore how birth rates vary throughout the year, highlight any unusual patterns, and provide a visual representation of the data to better understand the demographic trends of the time. The insights derived from this analysis can contribute to a deeper understanding of birth patterns and potentially build a forecasting model.

**Table of contents**

Data Loading,
Data Exploration,
Data Preprocessing,
Exploratory Data Analysis (EDA),
Modelling,
Evaluation Metrics.

The project follows a structured pipeline as outlined below:

1. Data Loading: Load the dataset and inspect its structure.

2. Data Exploration: Understand the dataset by checking distributions, missing values, duplicates, datatypes, Stationary Check and key statistics.

- Data challenges : The data type should be changed to 'date' for the date variable.

3. Data Preprocessing: - converting 'date' variable data type from object into date

4. Exploratory Data Analysis (EDA):

- Daily births over time observations : The data fluctuates over time, showing significant variations in the number of daily female births. Some months have higher peaks, indicating possible seasonality.

- Boxplot to check seasonal patterns (by month) observations: Highest births in September, with more outliers and variability. May and June show slightly lower births than other months. Consistent spread across months, but seasonal effects are visible.

- Time Series Decomposition observations: 
    - Trend : A slow upward trend is noticeable that means Births increase until Sept-Oct 1959, then decline slightly.
    - Seasonality: Clear repeating patterns indicate a strong seasonal cycle.
    - Residuals: Randomly distributed, with some spikes but no major patterns.

5. Modeling:

ARIMA: Auto-Regressive Integrated Moving Average model.

SARIMA: Seasonal ARIMA model to handle seasonality in the data.

6. Evaluation

The models were evaluated based on Mean Absolute Error (MAE) and RMSE to determine their forecasting accuracy.
