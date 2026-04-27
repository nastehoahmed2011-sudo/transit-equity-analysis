# 📍 Accessing Mobility: Transit Access and Demographic Inequality

## Overview

This project examines how socioeconomic status, race, age, and urban infrastructure shape access to walkable and bikeable environments across U.S. metropolitan areas. Using cleaned survey data (CleanData derived from the American Housing Survey), the analysis applies logistic regression, interaction models, and disproportionality indices to evaluate equity in mobility access.

The central focus is whether access to transit-friendly environments is distributed equitably across demographic groups or structured by systemic inequality.

---

## Research Question

To what extent do demographic and structural factors (income, race, age, metropolitan region, and infrastructure availability) influence the likelihood of living in a transit-friendly environment?

---

## Data

The dataset (`finalcleanwalk`) is a cleaned version of survey-based transportation and demographic data.

### Key Variables

- AGE: Respondent age  
- ZINC2: Household income  
- RACE: Race/ethnicity category  
- METRO3: Metropolitan classification  
- WBBIKELANE: Presence of bike infrastructure  
- WBBIKEWALK: Reported walking/biking behavior  
- walkbikedummy: Binary outcome (1 = walks/bikes, 0 = does not)

---

## Methods

### 1. Data Cleaning & Feature Engineering
- Standardized variable names  
- Converted categorical and numeric variables  
- Created binary outcome variable (walkbikedummy)  
- Constructed age group categories  

---

### 2. Descriptive Analysis
- Distribution of walking/biking behavior by race  
- Age distribution of mobility behavior  
- Visualization of demographic composition  

---

### 3. Equity Measurement

A Disproportionality Index was used to assess whether racial groups are over- or under-represented among individuals who walk or bike:

Index = Observed proportion / Expected proportion

- Values > 1 = overrepresentation  
- Values < 1 = underrepresentation  

---

### 4. Statistical Models

#### Logistic Regression (Baseline Model)
Predicts probability of walking/biking using:
- AGE  
- ZINC2 (household income)  
- RACE  
- METRO3  

---

#### Interaction Models
To test structural inequality effects:
- Race × Income  
- Metro × Income  
- Bike infrastructure × Income  

These models examine whether the effect of income varies across demographic and geographic contexts.

---

### 5. Predictive Modeling
- Individual-level probability estimates for walking/biking  
- Classification of mobility likelihood  
- Visualization of predicted probabilities  

---

### 6. Model Evaluation
- Akaike Information Criterion (AIC) used for model comparison  
- Logistic regression summary statistics used for inference  

---

## Key Findings (Summary)

- Income (ZINC2) is one of the strongest predictors of transit access  
- Metropolitan region is a significant structural factor shaping mobility  
- Race alone is less predictive once income and metro are included  
- Infrastructure (bike lanes) interacts with income, suggesting uneven distribution of built environment benefits  
- Overall, mobility access is shaped more by structural inequality than individual demographic characteristics alone  

---

## Visualizations

The analysis includes:
- Race distribution of mobility behavior  
- Age distribution of walkers/bikers  
- Disproportionality index plots  
- Predicted probability plots  

---

## Technologies Used

- R  
- tidyverse (dplyr, ggplot2, tidyr)  
- caret  
- MASS  
- stats (glm, lm)

---

## Project Structure

mobility-project/
│
├── analysis.R
├── finalcleanwalk.csv
├── README.md

---

## Limitations

- Survey-based self-reported data may include bias  
- Missing structural variables (e.g., safety, transit frequency)  
- Cross-sectional data limits causal interpretation  

---

## Author

Nasteho Ahmed  
Quantitative Policy & Data Analysis
