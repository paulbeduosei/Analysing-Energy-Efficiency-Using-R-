# Energy Efficiency Analysis

**Authors:** Paul Bedu-Osei, Carlos Batista-Diaz, Kwabena Antwi Anyemedu  
**Course:** SCM 651 — Business Analytics  
**Date:** November 2026

## Overview

This project uses multiple linear regression in R to analyze the UCI Energy 
Efficiency dataset. The goal is to identify which building characteristics 
have the strongest influence on heating and cooling energy loads.

## Dataset

- **Source:** UCI Machine Learning Repository — Energy Efficiency Dataset
- **Observations:** 768 buildings
- **Response Variables:**
  - Y1 — Cooling Load
  - Y2 — Heating Load
- **Predictor Variables:**
  - X1 — Relative Compactness
  - X2 — Surface Area
  - X3 — Wall Area
  - X4 — Roof Area *(excluded due to multicollinearity)*
  - X5 — Overall Height
  - X6 — Orientation
  - X7 — Glazing Area
  - X8 — Glazing Area Distribution

## Analysis Steps

1. Exploratory data analysis — scatterplot matrices and histograms
2. Correlation matrix to identify relationships between variables
3. Multiple linear regression models for Y1 (cooling) and Y2 (heating)
4. Identification of significant predictors
5. Interpretation of coefficients and lessons learned

## Key Findings

- **Overall Height (X5)** and **Glazing Area (X7)** are the strongest 
  predictors of both heating and cooling load
- **Roof Area (X4)** was dropped from both models due to multicollinearity 
  with other structural variables
- **Orientation (X6)** was not a significant predictor for either load
- Both models achieved an adjusted R-squared above 0.88, indicating a 
  strong model fit

## Tools Used

- R
- RCommander (Rcmdr)
- readXL, abind, e1071 packages
