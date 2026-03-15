# Singapore HDB Resale Price Analysis and Prediction (2017–2025)

This project analyzes **Singapore HDB resale transaction data from 2017 to 2025** and builds predictive models to estimate resale prices using both statistical and machine learning approaches.

## Project objective

The goals of this project are to:

- explore HDB resale price trends over time
- identify factors associated with higher resale prices
- test whether mature estates have significantly different resale prices from non-mature estates
- compare baseline linear regression with richer feature-based regression and Random Forest

## Dataset

The dataset contains HDB resale transaction records from **2017 to 2025**.

Example fields used in the analysis include:

- `month`
- `town`
- `flat_type`
- `storey_range`
- `floor_area_sqm`
- `lease_commence_date`
- `resale_price`

## Project workflow

1. Data loading and cleaning
2. Feature engineering
3. Exploratory data analysis
4. Hypothesis testing
5. Baseline OLS regression
6. Expanded OLS regression with encoded categorical features
7. Random Forest regression
8. Model comparison and feature importance review

## Key engineered features

- **year**: extracted from transaction month
- **remaining_years**: estimated lease remaining using transaction year
- **is_mature**: binary flag for whether the town is a mature estate

## Main insights

- HDB resale prices generally increased over the period studied
- Mature estates showed higher average resale prices than non-mature estates
- A feature-rich regression model performed better than a simple baseline OLS model
- Random Forest delivered the best predictive performance among the tested models

## Models used

### 1. Baseline OLS Regression
Uses a small set of interpretable predictors:
- remaining years
- floor area
- mature estate flag

### 2. Expanded OLS Regression
Adds one-hot encoded categorical predictors such as:
- flat type
- flat model
- storey range
- town

### 3. Random Forest Regressor
Captures nonlinear effects and feature interactions, improving predictive accuracy.
