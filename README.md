# cs247

---

## &#127806; [Final Project Report] Agricultural Crop Price Prediction

<p style='text-align: right;'> CS 247 Machine Learning </p>
<p style='text-align: right;'> December 18, 2022 | Angelica Kim </p>

---

### 1. Project Goal

In this project, I employ machine learning models, specifically neural-network-based models, to forecast the daily average price of crops across all agricultural wholesale markets in Korea. While the agricultural produce exhibit high price volatility, readily impacted by macroeconomic conditions and policits, I hypothesize that their prices would show some patterns due to their life cycle related to growth and harvest. Accurate crop price forecasting would be extremely valuable in trading because it helps identify arbitrage opportunities that directly translate to profits.

### 2. Data Description

In this project, I analyze aggregate time series data that combines daily transaction information from wholesale and retail markets, daily weather in the primary growing areas, and monthly trades data for 37 crops from 2013 to 2016. The data was provided by an online artificial intelligence (AI) competition platform hosted by Korea Agro-Fisheries & Food Trade Corporation ([Link to data source](https://aifactory.space/competition/data/2091)). Note that I translated the variable names into English since the original data was from a source based in Korea.

#### Data Dictionary:

> 1.  `date`: Date
> 2.  `crop`: Type of crops encoded in numbers (0-36)  
>     <strong>Price information (All price units are in Korean Won):</strong>
> 3.  `daily_avg_price`: Daily average price of each crop across 32 wholesale markets in Korea
> 4.  `daily_total_volume`: Total volume of each crop traded in 32 wholesale markets each day
> 5.  `avg_price_low`: Daily average of prices that fall below the value of `daily_avg_price` on that day
> 6.  `avg_price_high`: Daily average of prices that are higher than the value of `daily_avg_price` on that day  
>     7.`low_price_volume`: Total volume of each crop whose price is lower than the `daily_avg_price` for that crop traded on that day
> 7.  `high_price_volume`: Total volume of each crop whose price is higher than the `daily_avg_price` for that crop traded on that day  
>     <strong>Wholesale and retail transaction-related variables: </strong>
> 8.  `daily_max_wholesale_price`: Daily maximum price of each crop traded in 12 wholesale markets
> 9.  `daily_avg_wholesale_price`: Daily average price of each crop traded in 12 wholesale markets
> 10. `daily_min_wholesale_price`: Daily minimum price of each crop traded in 12 wholesale markets
> 11. `daily_max_retail_price`: Daily maximum price of each crop traded in 45 retail markets
> 12. `daily_avg_retail_price`: Daily average price of each crop traded in 45 retail markets
> 13. `daily_min_retail_price"`: Daily minimum price of each crop traded in 45 retail markets  
>     <strong>Trade-related variables:</strong>
> 14. `export_weight`: Weight of the crop exported, by month (in kilograms)
> 15. `export_amount_usd`: Value of export, by month (in US Dollars)
> 16. `import_weight`: Weight of the crop imported, by month (in kilograms)
> 17. `import_amount_usd`: Value of import, by month (in US Dollars)
> 18. `trade_balance_usd`: The balance of trade, which is the difference between the value of exports and imports (in US Dollars)  
>     <strong>Meteorological variables:</strong>
> 19. `area0_base_temp`: The base temperature of each crop at the first primary growing area, below which the crop no longer develops (in Celsius degrees)
> 20. `area0_max_temp`: Daily maximum temperature at the first primary growing area of each crop (in Celsius degrees)
> 21. `area0_min_temp`: Daily minimum temperature at the first primary growing area of each crop (in Celsius degrees)
> 22. `area0_avg_temp`: Daily average temperature at the first primary growing area of each crop (in Celsius degrees)
> 23. `area0_precip`: Daily precipitation amount at the first primary growing area of each crop (in milliliters)  
>     <em>There are two more sets of the same variables for two other primary growing areas.</em>

### 3. Related Work

There is an overflow of literature that performs stock price prediction using machine learning models. Taking into account the fact that the historical information has served as the basis of investment decisions in the finance industry, Wei employs Long Short-Term Memory (LSTM) neural network to perform stock price prediction (Wei, 2019). The model has proven effective for analyzing the time series since it uses the selective memory to keep track of the historical information. Since the data I'm using is also a time series that describes the daily average price of agricultural crops, I use LSTM models for crop price prediction.

<strong> Citations: </strong>

<li> Wei, Dou. “Prediction of Stock Price Based on LSTM Neural Network.” 2019 International Conference on Artificial Intelligence and Advanced Manufacturing (AIAM), 2019, https://doi.org/10.1109/aiam48774.2019.00113. </li>
<li> <em>FORECASTING: PRINCIPLES AND PRACTICE</em>, by Rob J Hyndman and George Athanasopoulos </li>
<li> <em> Machine Learning with PyTorch and Scikit-Learn</em>, by Sebastian Raschka, Yuxi (Hayden) Liu, and Vahid Mirjalili, Packt Publishing, 2022. </li>

---
