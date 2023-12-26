# Exploratory Data Analysis and Predictive Modeling

## Time Series Assignment

**Submitted By:**  
**Mohamed Fares Mekaoussi**  
**Email:** mohamed-fares.mekaoussi@etu.u-paris.fr  

---

## Bike Sharing Dataset Analysis

This project aims to explore and model the bike sharing dataset from UCI Machine Learning Repository. The dataset contains the hourly and daily count of rental bikes between years 2011 and 2012 in Capital bikeshare system in Washington, DC with the corresponding weather and seasonal information.

---

## Objectives

The main objectives of this project are:

1. Perform exploratory data analysis on the bike sharing dataset.
2. Smooth the time series of the daily count of bike rentals and compare it with the original time series.
3. Choose a suitable smoothing method and frequency for the time series.
4. Test the stationarity and seasonality of the time series and decompose it into trend, seasonal and irregular components.
5. Fit an ARIMA model on the de-seasonalized time series and select the best model based on the AIC criterion and the residual analysis.
6. Forecast the next 25 observations using the chosen ARIMA model and compare it with the actual data.

---

## Data

The data can be downloaded from here. It consists of two files: `hour.csv` and `day.csv`. Both files have the following fields, except `hr` which is not available in `day.csv`:

- `instant`: Record index
- `dteday`: Date
- `season`: Season (1:springer, 2:summer, 3:fall, 4:winter)
- `yr`: Year (0: 2011, 1:2012)
- `mnth`: Month (1 to 12)
- `hr`: Hour (0 to 23)
- `holiday`: weather day is holiday or not (extracted from Holiday Schedule)
- `weekday`: Day of the week
- `workingday`: If day is neither weekend nor holiday is 1, otherwise is 0.
- `weathersit`: (extracted from Freemeteo)
    - 1: Clear, Few clouds, Partly cloudy, Partly cloudy
    - 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
    - 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
    - 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
- `temp`: Normalized temperature in Celsius. The values are derived via (t-t_min)/(t_max-t_min), t_min=-8, t_max=+39 (only in hourly scale)
- `atemp`: Normalized feeling temperature in Celsius. The values are derived via (t-t_min)/(t_max-t_min), t_min=-16, t_max=+50 (only in hourly scale)
- `hum`: Normalized humidity. The values are divided to 100 (max)
- `windspeed`: Normalized wind speed. The values are divided to 67 (max)
- `casual`: count of casual users
- `registered`: count of registered users
- `cnt`: count of total rental bikes including both casual and registered

---

## Code

The code for this project is written in R and can be found in the file `bike_sharing_Mekaoussi.ipynb`. The code is organized into four parts:

1. Part 1: Data examination
2. Part 2: Time series smoothing and frequency selection
3. Part 3: ARIMA model fitting and selection
4. Part 4: Forecasting with ARIMA models

The code is well-commented and follows the objectives of the project.

---

## Conclusion

This project has demonstrated how to perform exploratory data analysis and predictive modeling on the bike sharing dataset using R. The main findings are that the bike rental demand is influenced by the weather and seasonal factors, such as temperature, humidity and windspeed. The time series of the daily count of bike rentals can be smoothed and modeled by an ARIMA model, which can provide reasonable forecasts for the future. However, the model may not be suitable for decision-making purposes, as it does not take into account other potentially influential factors, such as holidays, events, promotions, etc.
