# trayectories_1

# Time Series Analysis and Prediction Script

This repository contains an R script for time series analysis and prediction. The script is structured as follows:

## Data Loading and Preprocessing
The script begins by:
- Reading a data file and transposing it.
- Initializing variables for analysis:
  - `d`: Dimension of the data.
  - `n`: Number of data points.
  - `y`: Matrix to hold the data.
  - `t`: Time points.
  - `k`: Product of `d` and `n`.
  - `h`: Interval between time points.

## Defining Functions for Parameter Estimation
Several functions are defined (`A1` to `A32`, `fa`, `fs`, `fc`, `fb`). These functions are tailored to the statistical model used and are intended to calculate various parameters and statistics based on the input data.

## Plotting and Finding Roots
- The function `fb` is plotted over a specified interval.
- The `uniroot.all` function from the `rootSolve` package is used to find the roots of `fb` within a given range.

## Parameter Estimation
- Parameters (`auxA`, `auxC`, `auxS2`, `auxM`, `auxBeta`) are calculated using the roots found in the previous step and the earlier defined functions. These parameters are central to the model's predictions.

## Prediction Calculations
- Functions for making predictions (`mediapred`, `modapred`, `medianapred`, `cuantil5pred`, `cuantil95pred`, and their conditional versions) are defined. These functions predict future values in the time series under various statistical assumptions (mean, mode, median, and specific quantiles).

## Writing Predictions to Files
- The script computes predicted values for all time points and writes these predictions to separate text files for each type of prediction.

## Predictions for a New Time Point
- Includes functions to predict values at a new time point not included in the original data, both unconditionally and conditionally, based on the last observed value.

