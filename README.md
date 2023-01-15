# &#127806; [Final Project Report] Agricultural Crop Price Prediction

<p align="right"> CS 247 Machine Learning </p>
<p align="right">December 18, 2022 | Angelica Kim </p>

### 1. Project Goal

This project employs neural-network-based models--Long Short-term Memory (LSTM)--to forecast the daily average price of crops across all agricultural wholesale markets in Korea. While the agricultural produce exhibit high price volatility, readily impacted by macroeconomic conditions and policits, there are seasonality and periodicity in crop prices due to life cycles of crops related to growth and harvest. Accurate crop price prediction would be extremely valuable in trading agricultural futures because it helps identify arbitrage opportunities.

### 2. Data Description

In this project, I analyze aggregate time series data that combines daily transaction information from wholesale and retail markets, daily weather in the primary growing areas, and monthly trades data for 37 crops from 2013 to 2016. The data was provided by an online artificial intelligence (AI) competition platform hosted by Korea Agro-Fisheries & Food Trade Corporation ([Link to data source](https://aifactory.space/competition/data/2091)). Note that I translated the variable names into English since the original data was from a source based in Korea.

### 3. Related Work

There is an overflow of literature that performs stock price prediction using machine learning models. Taking into account the fact that the historical information has served as the basis of investment decisions in the finance industry, Wei employs LSTM models to perform stock price prediction (Wei, 2019). The model has proven effective for analyzing the time series since it uses the selective memory to keep track of the historical information.

<strong> Citations: </strong>

<li> Wei, Dou. “Prediction of Stock Price Based on LSTM Neural Network.” 2019 International Conference on Artificial Intelligence and Advanced Manufacturing (AIAM), 2019, https://doi.org/10.1109/aiam48774.2019.00113. </li>
<li> <em>FORECASTING: PRINCIPLES AND PRACTICE</em>, by Rob J Hyndman and George Athanasopoulos </li>
<li> <em> Machine Learning with PyTorch and Scikit-Learn</em>, by Sebastian Raschka, Yuxi (Hayden) Liu, and Vahid Mirjalili, Packt Publishing, 2022. </li>
