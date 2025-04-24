**Project Title : House Sale Prices Prediction.**

**Technologies Used:** Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, tensorflow, statsmodels, --- Languages: Python.

**Project Overview:** The main aim of this project is to predict the house sale prices in Washington State, USA, using various machine learning & deep learning models. Additionally, time series analysis is applied to understand market trends and forecast future property prices. The objective is to build a reliable model that can accurately forecast house prices and identify the main elements that affecting high value properties. By analyzing historic data, we can develop a robust prediction model and gain insights into the main factors that contribute to higher house prices.

**Table of contents**
1. Dataset Loading
2. Data Exploration
3. Data Preprocessing
4. Exploratory Data Analysis (EDA)
5. Modelling
6. Time Series Analysis
7. Evaluation Metrics
8. Conclusion

**The project follows a structured pipeline as outlined below:**

  **1. Data Loading:** Load the dataset and inspect its structure.

  **2. Data Exploration:** Understand the dataset by checking distributions, missing values, duplicates, datatypes and key statistics.

Data challenges 

- The data type should be changed to 'Int' for bathrooms & floors variables, and to 'date' for the date variable.

- Duplicate rows in the 'id' column should be removed, keeping the latest 'id' by sorting the date as it contains the updated house price.
   
**3. Data Preprocessing:** - Data types converted, Removed duplicates rows

**4. Exploratory Data Analysis (EDA):** performed univariant and bivariant analysis.

- **Observations in univariant analysis** 

Most houses have 2 to 4 bedrooms, with very few having more than 6. Bathrooms are generally in between 1 & 2, larger numbers are more rare. The majority of houses having 1 or 2 floors, and those with 3 or more floors are less frequent. Regarding waterfront, the distribution shows that most houses do not have a waterfront. Similarly, most houses have no significant view, with higher view indices (1 to 4) being rare. In terms of condition, the houses are generally in good shape, with condition scale ranging between 3 and 5, while very few are in poor condition (indices 1 or 2). Finally, the grade distribution indicates that the majority of houses fall within the middle range (6 to 8), reflecting average to good construction and design quality. Houses with very low (1-3) or very high (10+) grades are uncommon.

- **Observations-The distribution plots**

The distribution of the price variable seems right skewed with most houses having less prices and very few having high-priced houses.The living space area (sqft_living) and above-ground living space (sqft_above) both seems right skewed, with most houses having small areas. Lot size (sqft_lot) is extremely skewed, with a large number of houses having small lots and very few with extremely large lots. The yr_built variable seems multimodal distribution and most houses were built between 1940 and 2010. Latitude (lat) and longitude (long) show clustered distributions, indicating that there are more houses in particular geographic areas.

- **Observations in Bivariant analysis**

Price shows a positive correlation with square footage (both living space and above-ground area), grade, bathrooms, and view, where higher values in these variables correspond to higher prices. Prices for waterfront properties are significantly greater when compared to non-waterfront properties. House condition and the number of floors show only a minor impact on the price, with higher floors or better conditions associated with slight increases. Older houses (based on year built) generally do not show a consistent trend in price, but recently built homes are increasing significantly.

**5. Modeling:** 

**Applied various machine learning models:**
Linear Regression, DecisionTreeRegressor, RandomForestRegressor, XGBRegressor, Support Vector Regression (SVR), K-Nearest Neighbors (KNN) & Neural Networks.

**6. Time Series Analysis**

In addition to predicting house prices using machine learning & deep learning models, time series analysis was applied to forecast future trends. The following steps were followed:

- **Understanding Trends and Seasonality** : Visualized the overall trend and seasonal variations in house prices.
  
  **Observations**:The plot shows the Monthly Average House Prices over a period of time, from July 2014 to May 2015. The trend shows a Downward Trend from July 2014 to March 2015, indicating that house prices were decreasing during this period. After March 2015, the pattern changes to an Upward Trend that shows house prices were increasing.


- **Stationarity Check**
  
Performed the Augmented Dickey-Fuller (ADF) test to check whether the data is stationary or not. Here, data is not stationary. So it is necessary to eliminate trends by using differencing techniques to make the data stationary.

- **Building Time Series Models**
  
ARIMA: Auto-Regressive Integrated Moving Average model.

SARIMA: Seasonal ARIMA model to handle seasonality in the data.

**7. Evaluation**
  
The models were evaluated based on Mean Absolute Error (MAE) and RMSE to determine their forecasting accuracy.

**8. Conclusion:** 

- The Random Forest and XGBoost models provided the most accurate predictions for house prices, with an R² score of 0.88.
- Time series analysis using SARIMA was effective in capturing trends and seasonality, providing reliable forecasts of future house prices.
