# Weather and Retail Sales Patterns

## 📌 Project Overview

This project explores the relationship between weather conditions and retail sales. We analyzed historical weather data alongside transactional retail sales records to identify how weather variables influence purchasing behavior. The findings aim to help businesses optimize inventory, promotional campaigns, and staffing based on seasonal and daily weather conditions.

---

## 🎯 Project Objectives

1. Quantify how weather conditions influence daily retail sales  
2. Identify seasonal sales patterns based on temperature and precipitation  
3. Predict high sales days using machine learning models  
4. Present findings using visualizations and statistical evidence  

---

## 📚 Research Questions & Hypotheses

### Questions Explored:
1. Does temperature significantly affect daily retail sales?
2. Are there noticeable patterns in sales across different seasons?
3. Can weather features predict whether a day will result in high or low sales?

### Hypotheses Tested:
- **H1**: Higher temperatures are associated with increased sales.
- **H2**: Winter months (low temperatures) correlate with lower overall sales.
- **H3**: Sales patterns differ significantly across seasons (ANOVA).

---

## 📊 Data Sources

### 1. Retail Sales Data  
- **Source**: Public retail dataset (retail_sales_dataset.csv)  
- **Time Period**: January 1–March 31, 2023  
- **Variables**: Date, Product Category, Total Amount, Transaction ID

### 2. Weather Data  
- **Source**: [Meteostat API](https://meteostat.net)  
- **Location**: New York City  
- **Variables Used**: Temperature (tavg), Precipitation (prcp)

---

## 🧪 Data Collection & Preprocessing

1. Loaded retail data into a Pandas DataFrame  
2. Retrieved daily weather data from Meteostat API  
3. Merged datasets on `Date`  
4. Cleaned and transformed data  
5. Aggregated retail sales to daily totals  

---

## 🔧 Feature Engineering

- `season`: Mapped from month  
- `is_extreme_temp`: Flag for temps < 0°C or > 30°C  
- `high_sales`: Binary label for sales above daily median  

---

## 📊 Visualizations & Interpretations

### 1. Daily Sales Over Time  
![Daily Sales Over Time](plots/daily_sales.png)  
This line plot shows daily total sales from Jan to March 2023.  
📌 **Significance**: Highlights fluctuations, with visible sales dips and peaks — possible links to weather.

---

### 2. Total Sales by Season  
![Sales by Season](plots/season_boxplot.png)  
Boxplot comparing total sales across winter and spring.  
📌 **Significance**: Spring shows higher median sales. ANOVA revealed no statistically significant difference.

---

### 3. Temperature vs Total Sales  
![Temp vs Sales](plots/temp_vs_sales.png)  
Scatter plot of average temperature vs sales.  
📌 **Significance**: Shows a positive relationship — warmer days correlate with higher sales.

---

### 4. Correlation Matrix  
![Correlation Matrix](plots/correlation_heatmap.png)  
Heatmap showing feature correlations.  
📌 **Significance**: Temperature correlates positively with sales; precipitation correlates negatively.

---

## ✅ Hypothesis Testing

### T-Test: High vs Low Temp Days
- **T-statistic**: 4.99  
- **P-value**: < 0.001 → Significant difference

### ANOVA: Seasonal Sales Differences
- **F-statistic**: 2.57  
- **P-value**: 0.112 → Not statistically significant

---

## 🤖 Machine Learning Task

**Goal**: Predict whether a day will have high sales based on weather data.

### Features:
- `tavg`, `prcp`, `season`, `is_extreme_temp`

### Target:
- `high_sales` (boolean)

### Model: Logistic Regression
- **Accuracy**: 72%  
- **F1-score (High Sales)**: 0.76  
- **Confusion Matrix**:

