# eBay Analysis
---
# Purpose
The purpose of this analysis is to gather and analyze eBay sales data to find trends and predict future trends of prices and demand of products. The data being analyzed is collected from eBay of sales from different categories spanning back to Aug of 2019. 

---

# Trends

Each Analysis file for each product includes their data along with charts and histogram which indicates their sales over the given period of time. However for sake of time, only one product will be analyzed. 
For this analysis the sales of necklaes will be looked at. Before analyzing the data any sales that are considered outliers will be eliminated. 
![image](https://github.com/evanbruno617/eBay_Analysis/blob/main/Images/Screenshot%202024-10-15%20at%209.08.23%E2%80%AFPM.png)
As Seen in the image above there are outliers in certain months and therefore they need to be removed from the data in order to not interfere with the model's estimation. 

---
# Cleaning

In order for the time series analysis to be ran both the independent and dependent variables must be stationary. The economic factors being used for the time series analysis are stationary with I(1) and total sales and average price of necklaces are stationary with (1)

---

# Change in Total Sold

The change in total sold is the dependent variable in the time series model and is estimated using the following model with lags up to 4. 
![image](https://github.com/evanbruno617/eBay_Analysis/blob/main/Images/Screenshot%202024-10-15%20at%209.11.25%E2%80%AFPM.png)

The model has a NRMSE of 0.2 which means that it is a good model to estimate the change in total sold. 

However When testing for autocorrelations it was found that there was correlation at lag 2
![image](https://github.com/evanbruno617/eBay_Analysis/blob/main/Images/Screenshot%202024-10-15%20at%209.17.09%E2%80%AFPM.png)

In order to fix this issue up to 2 lags of the dependent variable was added to the mnodel. 

Afterwards when testing for heteroscedasticity it passed the test.

# Change in Average Sold price

The change in average sold price is the dependent variable in the time series model and estimated using the following model with lags up to 4. 
![image](https://github.com/evanbruno617/eBay_Analysis/blob/main/Images/Screenshot%202024-10-15%20at%209.19.17%E2%80%AFPM.png)

When testing for both autocorrelation and heteroscedasticity it passed both of these tests. Then the models NRMSE was calculated below. 
![image](https://github.com/evanbruno617/eBay_Analysis/blob/main/Images/Screenshot%202024-10-15%20at%209.19.52%E2%80%AFPM.png)

The NRMSE being 0.08 indicates that this model is excellent at predicting the change in average sold price of necklaces. 

---

# Conlsuion

Even though only one of the products used time series analysis to predict changes in total sold and average price sold this same model and concepts can be used in other products as well. 
Being able to predict the change in average price sold is useful for sellers to know when to sell their products and the best price to sell it at. Being able to apply this same model and concept to other products
this can be highly beneficial in scaling and managing different products in different categories on eBay. 

