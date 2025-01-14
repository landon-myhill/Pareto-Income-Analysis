# Pareto Distribution Analysis with World Top Incomes Data

This project analyzes income data from the **World Top Incomes Database** to estimate the Pareto distribution's exponent, a parameter that characterizes the income distribution's upper tail. The analysis involves data preparation, function development, and visualization to explore the relationships in the dataset.

---

## Purpose of the Code

The Pareto distribution is often used to model the distribution of wealth or income, particularly for high earners. The exponent `a` in the Pareto distribution determines the distribution's "tail heaviness." By estimating `a`, we can gain insights into income inequality and how wealth is concentrated at the top of the income distribution.

This code:
- Prepares and cleans the dataset for analysis.
- Implements mathematical functions to estimate the Pareto exponent using observed income thresholds.
- Visualizes the trends and relationships in the income data over time.
- Fits regression models to analyze trends in the Pareto exponent across years.

---

## Key Steps in the Code

### 1. **Data Preparation**
- The dataset is loaded and relevant columns are selected for analysis.
- The new dataset contains:
  - `Year`: The year of observation.
  - `P99`, `P99.5`, `P99.9`: Income thresholds at the 99th, 99.5th, and 99.9th percentiles.

### 2. **Discrepancy Function**
The code defines a function `percentile_ratio_discrepancies` that calculates the discrepancies between observed income ratios and expected values under the Pareto model. It minimizes these discrepancies to estimate the exponent `a`.

### 3. **Optimization**
Using numerical optimization (`nlm`), the code solves for the Pareto exponent `a` that minimizes discrepancies between observed and expected income thresholds.

### 4. **Estimation Across Years**
The function is applied to each row of the dataset to calculate an annual estimate of `a`. These estimates show how income inequality has changed over time.

### 5. **Visualization**
Scatterplots and regression models are created to visualize the trends in the Pareto exponent (`a`) across years.
