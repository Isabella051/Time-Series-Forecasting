# Time Series Forecasting
## 1. Kobe Bryant Shot Analysis & Auckland Temperature Study
[Kobe Bryant Shot Analysis & Auckland Temperature Study.html](https://isabella051.github.io/Time-Series-Forecasting/A1.html)

- Filtered and cleaned Kobe Bryant’s game records (**dplyr**)
- Converted dates and re-centered shot coordinates (**lubridate**)
- Created scatter plots and 2D density plots (**ggplot2**, **geom_density_2d**)
- Calculated shot distance and compared results by game type (**geom_histogram**)
- Analyzed free-throw performance and game frequency by weekday
- Converted monthly average temperature data to a tsibble object with proper date format (**read_csv**)
- Produced time plots, seasonal plots, and subseries plots (**gg_season**, **gg_subseries**)
- Analyzed trends and seasonality (hottest and coldest months)
- Created lag plots to study autocorrelation patterns (**gg_lag**)

## 2. Auckland Temperatures & NVIDIA Closing Stock Prices & Trading-Day Adjustments
[Auckland Temperatures & NVIDIA Closing Stock Prices & Trading-Day Adjustments.html](https://isabella051.github.io/Time-Series-Forecasting/A2.html)

- Decompose the series into trend, seasonal, and remainder components
- Visualize each component and analyze series features
- Apply a manual **Box-Cox** transformation with λ=0.5
- Plot the transformed time series and **correlogram**
- Analyze autocorrelation patterns and seasonal cycles
- Seasonally adjust the Box-Cox transformed series using **STL**
- Plot the seasonally adjusted series and subseries plot
- Plot the correlogram of the remainder component (ACF)
- Verify with a **Ljung-Box test** (Box.test)
- Convert the closing price series to a tsibble and create a weekday variable
- Use **boxplots** to show the distribution of closing prices for each weekday (geom_boxplot)
- Fit three **benchmark forecasting models**: Average, Naive, and Random-Walk with Drift
- Visualize the actual closing prices along with forecasted points
- Evaluate which model performs best and worst

## 3. Time Series Decomposition and Forecasting & Time Series Regression & Manual Cross-Validation Calculation
[Time Series Decomposition and Forecasting & Time Series Regression & Manual Cross-Validation Calculation.html](https://isabella051.github.io/Time-Series-Forecasting/A3.html)

- Fit **STL decomposition**
- Forecast the seasonal component using SNAIVE
- Forecast the seasonally-adjusted series using **benchmark models**: NAIVE, MEAN, and Random Walk with Drift
- Forecast 2 years ahead and plot point forecasts with original data
- Compute forecast accuracy measures and discuss which forecast method performs best for monthly average temperatures
- Identify three quarters with outliers; create a single **dummy variable** for them
- Identify the quarter with a level shift; create a **dummy variable** starting from that quarter
- Fit Regression Models:
  Model 1: Linear trend + level shift + seasonal factors;
  Model 2: Linear trend + level shift + seasonal factors + outliers;
  Model 3: Linear trend + level shift + Fourier terms (K=1) + outliers;
- Plot original series with fitted values from all three models
- Compare models using **AICc** and **CV**
- Select the best predictive model and report its estimates
- Check assumptions: linearity, independence, normality, zero mean, equal variance (gg_tsresiduals)
- Use observed vs fitted plots and **Ljung-Box test** for residual analysis
- Forecast 4 years ahead using the selected model and plot forecasts with 90% and 99% **prediction intervals**
- Manually compute the cross-validation for the selected regression model using the hat matrix method
- Construct the design matrix X with trend, seasonal, and dummy variables

## 4. Retail Trade
[Retail Trade.html](https://isabella051.github.io/Time-Series-Forecasting/RetailTrade.html)

- Create time plot, subseries plot, decomposition plot and discuss the features (autoplot, gg_subseries, STL)
- Fit different **ETS** models (ETS)
- Select the model with the lowest AIC value
- Fit different **ARIMA** models (gg_tsdisplay)
- Produce **residual diagnostic** plots for the ETS model
- Test the independence of your residuals using the **surrogate_test**
- Produce point forecasts and prediction intervals (accuracy, forecast)

