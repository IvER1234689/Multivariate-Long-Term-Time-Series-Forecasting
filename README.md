# Multivariate-Long-Term-Time-Series-Forecasting

In this GitHub repository, we provide eight widely-used and publicly available datasets for research in multivariate long-term time series forecasting. These datasets span diverse real-world domains, including weather prediction, traffic flow monitoring, energy consumption, and financial exchange rate analysis. Each dataset is formatted consistently: for a time series signal with `T` timestamps and `n` sensors at each timestamp, the data file contains `T` lines, with each line comprising `n` real numbers separated by commas. We also include data preprocessing scripts to ensure compatibility with our proposed model, EAPformer, and other time series forecasting frameworks.

## Paper
**EAPformer: Entropy-Aware Patch Transformer for Multivariate Long-Term Time Series Forecasting**

## Datasets

### 1. Electricity Consumption
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/ElectricityLoadDiagrams20112014)
- **Description**: This dataset records electricity consumption (in kWh) every 15 minutes from 2011 to 2014 for 321 clients. Due to zero-valued dimensions in 2011, we excluded those records and used data from 2012 to 2014. The data has been preprocessed to reflect hourly consumption for consistency.
- **Temporal Resolution**: Hourly
- **Dimensionality**: 321 sensors (clients)
- **Usage**: Suitable for modeling energy consumption patterns over time.

### 2. Traffic Usage
- **Source**: [PeMS - California Department of Transportation](http://pems.dot.ca.gov)
- **Description**: This dataset contains 48 months (2015–2016) of hourly road occupancy rates (ranging from 0 to 1) measured by sensors on San Francisco Bay Area freeways. It captures traffic flow dynamics across multiple locations.
- **Temporal Resolution**: Hourly
- **Dimensionality**: Varies (sensor-dependent)
- **Usage**: Ideal for studying traffic flow patterns and congestion forecasting.

### 3. Weather
- **Source**: Referenced in [Autoformer](https://arxiv.org/abs/2106.13008) [Wu et al., 2021]
- **Description**: This dataset includes multivariate time series data for weather-related variables, such as temperature, humidity, and pressure, collected at high temporal resolution. It is designed to test forecasting models on periodic and seasonal patterns.
- **Temporal Resolution**: Varies (e.g., 15-minute intervals)
- **Dimensionality**: Multiple weather variables
- **Usage**: Suitable for evaluating models on weather forecasting tasks.

### 4. Exchange
- **Source**: Referenced in [Autoformer](https://arxiv.org/abs/2106.13008) [Wu et al., 2021]
- **Description**: This dataset captures daily exchange rates for multiple currencies. It reflects financial time series with non-stationary and fluctuating dynamics.
- **Temporal Resolution**: Daily
- **Dimensionality**: Multiple currency pairs
- **Usage**: Useful for financial time series forecasting and trend analysis.

### 5. ETT Datasets (ETTm1, ETTm2, ETTh1, ETTh2)
- **Source**: Referenced in [Informer](https://arxiv.org/abs/2012.07436) [Zhou et al., 2021]
- **Description**: The Electricity Transformer Temperature (ETT) datasets consist of four variants: ETTm1, ETTm2 (minute-level), and ETTh1, ETTh2 (hourly). These datasets record transformer load and temperature metrics, capturing both periodic and non-stationary dynamics. They vary in temporal granularity and sequence length, making them suitable for testing long-term forecasting robustness.
- **Temporal Resolution**: 
  - ETTm1, ETTm2: 15-minute intervals
  - ETTh1, ETTh2: Hourly
- **Dimensionality**: Varies (multiple transformer metrics)
- **Usage**: Ideal for evaluating models on both high- and low-resolution time series with complex temporal dependencies.