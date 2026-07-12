# Effect of Imports on GNP (Iran) — OLS Regression Analysis

*Coursework project for the Econometrics course at Alzahra University.*

*Note: The source data and full working file are in Persian, as this project uses data from the Central Bank of Iran.*

## Overview

This project studies how imports affect Iran's Gross National Product (GNP), using annual data and EViews. The goal was to build a simple linear regression model, interpret it properly, and test how well it holds up on unseen data — a full walkthrough of the classical OLS workflow from data collection to forecasting.

## Data

Annual GNP and import figures were collected from the Central Bank of Iran, covering the years 1338 to 1393 (SH). Before modeling, the relationship between the two variables was explored visually with a scatter plot and a fitted regression line to check whether a linear model was a reasonable starting point.

## Model

A simple linear regression was estimated using Ordinary Least Squares (OLS):

GNP_t = β₁ + β₂ · Import_t + ε_t

where GNP is the dependent variable and Import is the explanatory variable.

The model was also re-estimated using mean-deviated data (i.e., without an intercept), to see how the coefficients and interpretation change once the constant term is removed.

## Validation

To check how well the model generalizes, the data was split into a training set (70%, 1338–1375) and a test set (the remaining 30%). The model was fit on the training data, then used to generate point forecasts for GNP, which were compared against the actual test-set values. As a further check, the model's behavior was tested under simple transformations — doubling the dependent variable and halving the independent variable — to confirm that the linear structure held up as expected.

## Key Results

- Import coefficient (β₂) = 107.10 — holding other factors constant, a one-unit increase in imports is associated with an average 107-unit increase in GNP.
- The t-statistic and p-value confirm the coefficient is statistically significant at the 5% level.
- R² = 0.662 — imports explain about 66% of the variation in GNP.
- Forecasted values tracked the actual GNP figures reasonably closely across the test period.
- The model's linear structure remained consistent even after scaling the variables, as expected from OLS theory.

## Tools

EViews 13 — used for data entry, visualization, OLS estimation, forecasting, and sensitivity analysis.

## Files

فایل تمرین ایویوز.pdf — the full working file, including all analysis steps and EViews output.
