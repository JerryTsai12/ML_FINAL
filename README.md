# YouBike Demand Forecasting

## Project Overview
This project aims to predict the number of available bikes at various stations in a bicycle sharing system. The prediction is based on historical data including weather conditions, time features, and station characteristics.

## Project Report

The `report.pdf` document contains a comprehensive analysis of our approach to the bicycle sharing prediction problem:

- Detailed explanation of the data preprocessing methods
- Feature engineering techniques used to improve model performance
- Analysis of various models tested (XGBoost, LightGBM, RNN, and LSTM)
- Comparative evaluation of model performance across different stages
- Visualization of prediction results and error analysis

## Competition Results

- **Team Name**: 為什麼會變成這樣呢
- **Kaggle Competitions**:
  - [Stage 1](https://www.kaggle.com/competitions/html2023fall-final/leaderboard)
  - [Stage 2](https://www.kaggle.com/competitions/html2023fall-final-project-stage-2/leaderboard)
  - [Stage 3 (Final Stage)](https://www.kaggle.com/competitions/html2023fall-final-project-stage-3/leaderboard?)

## Data Description

### Station Data
- `data/info/data_stn_tot.json`: Contains the total number of bike slots for each station
- `data/info/data_sno_test_set.txt`: List of station IDs for testing

### Time-based Data
- `data/info/data_dayfeature.csv`: Contains date features including:
  - `weekday`: Day of week (1-7, Monday-Sunday)
  - `workingday`: Whether it's a working day (0 or 1)
  - `holiday`: Whether it's a holiday (0 or 1)
  
- `data/info/data_datelist_train.txt`: Dates for training set
- `data/info/data_datelist_val.txt`: Dates for validation set
- `data/info/data_datelist_test.txt`: Dates for test set
- `data/info/data_datelist_release.txt`: All dates with available public data
- `data/info/data_datelist_del.txt`: Dates to be excluded from analysis

### Weather Data

- `data/info/data_weather.json`: Hourly weather information including:
  - `temp`: Temperature (°C)
  - `rain`: Precipitation (mm)
  - `moist`: Humidity (%)
  - `wind`: Wind speed (m/s)

## Data Format Details

### Station Record Format

The processed station records include the following fields:

- `stnid`: Station ID
- `date`: Date in YYYYMMDD format
- `time`: Time in HH:MM format (hourly intervals)
- `tot`: Total number of bike slots at the station
- `weekday`: Day of week (1-7, Monday to Sunday)
- `working`: Working day indicator (0 or 1)
- `holiday`: Holiday indicator (0 or 1)
- `rain`: Precipitation amount
- `sbi`: System Bike Information - number of available bikes (target variable)

## Data Processing Workflow

### 1. Data Cleaning & Preprocessing (`data/data_cleaning.ipynb`)

- Cleans raw data files
- Handles missing values
- Combines data sources
- Standardizes data formats

### 2. Data Generation (`data/data_gen.ipynb`)

- Creates training, validation and test datasets
- Incorporates features from different sources
- Prepares data for model input

### 3. Data Visualization (`data/data_draw.ipynb`)

- Exploratory data analysis
- Temporal pattern visualization
- Feature correlation analysis
- Station behavior analysis

## Model Implementation

### XGBoost Models (`model/XGBoost.ipynb` & `model/XGBoost_min.ipynb`)

- Gradient boosting implementation
- Feature importance analysis
- Hyperparameter optimization

### LightGBM Models (`model/lightGBM.ipynb`, `model/lightGBM_min.ipynb`, `model/lightGBM_.ipynb`)

- Gradient boosting framework
- Leaf-wise tree growth
- Handling of categorical features

### MLP - Multi-layer Perceptron (`model/MLP.ipynb`)

- Neural network approach
- Deep learning implementation
- Time series prediction