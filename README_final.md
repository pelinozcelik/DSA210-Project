
# Weather and Retail Sales Patterns

## 📌 Project Overview

This project explores the relationship between weather conditions and retail sales. We analyzed historical weather data alongside transactional retail sales records to identify how weather variables influence purchasing behavior. The findings aim to help businesses optimize inventory, promotional campaigns, and staffing based on seasonal and daily weather conditions.

## 🎯 Project Objectives

- Quantify how weather conditions influence daily retail sales  
- Identify seasonal sales patterns based on temperature and precipitation  
- Predict high sales days using machine learning models  
- Present findings using visualizations and statistical evidence  

## 📚 Research Questions & Hypotheses

**Questions Explored:**
1. Does temperature significantly affect daily retail sales?
2. Are there noticeable patterns in sales across different seasons?
3. Can weather features predict whether a day will result in high or low sales?

**Hypotheses Tested:**
- H1: Higher temperatures are associated with increased sales.
- H2: Winter months (low temperatures) correlate with lower overall sales.
- H3: Sales patterns differ significantly across seasons (ANOVA).

## 📊 Data Sources

**1. Retail Sales Data**  
- Source: Public retail dataset (`retail_sales_dataset.csv`)  
- Time Period: January 1–March 31, 2023  
- Variables: Date, Product Category, Total Amount, Transaction ID  

**2. Weather Data**  
- Source: Meteostat API  
- Location: New York City  
- Variables Used: Temperature (tavg), Precipitation (prcp)  

## 🧪 Data Collection & Preprocessing

- Loaded retail data into a Pandas DataFrame  
- Retrieved daily weather data from Meteostat API  
- Merged datasets on `Date`  
- Cleaned and transformed the combined data  
- Aggregated retail sales to daily totals  

## 🔧 Feature Engineering

- `season`: Mapped from month  
- `is_extreme_temp`: Flag for temps < 0°C or > 30°C  
- `high_sales`: Binary label for sales above the median  

## 📊 Visualizations & Interpretations

**1. Daily Sales Over Time**  
![Line plot](plots/daily_sales.png)  
📌 *Interpretation*: Highlights fluctuations in daily sales — useful for spotting trends and outliers.

**2. Total Sales by Season**  
![Boxplot](plots/sales_by_season.png)  
📌 *Interpretation*: Spring showed higher median sales, but differences were not statistically significant (p > 0.05).

**3. Temperature vs Total Sales**  
![Scatter plot](plots/temperature_vs_sales.png)  
📌 *Interpretation*: Positive trend — higher temperatures tend to correlate with increased sales.

**4. Correlation Matrix**  
![Heatmap](plots/correlation_matrix.png)  
📌 *Interpretation*: `tavg` shows a positive correlation with `total_sales`; precipitation shows a slight negative effect.

## ✅ Hypothesis Testing

**T-Test: High vs Low Temp Days**  
- T-statistic: 4.99  
- P-value: < 0.001  
📌 *Interpretation*: Statistically significant — high temp days tend to have higher sales.

**ANOVA: Seasonal Sales Differences**  
- F-statistic: 2.57  
- P-value: 0.112  
📌 *Interpretation*: No statistically significant difference between winter and spring sales.

## 🤖 Machine Learning Task

**Goal**: Predict whether a day will have high sales based on weather data.

**Features Used**:
- tavg
- prcp
- season (encoded)
- is_extreme_temp

**Target**:
- high_sales (boolean)

**Model**: Logistic Regression  

### 🔍 Model Evaluation:
- **Accuracy**: 0.72  
- **F1-score (High Sales)**: 0.76  
- **Confusion Matrix**:  
```
[[5 3]
 [2 8]]
```
📌 **Interpretation**: The model performs reasonably well, especially for predicting high sales days.

---

## 📎 Conclusion

This project demonstrates how retail sales can be influenced by weather patterns. Temperature showed a statistically significant impact on sales, while seasonal differences were not as impactful in our sample. A logistic regression model trained on weather features achieved 72% accuracy in predicting high sales days.

📌 **Key Takeaways**:
- Warmer days are generally associated with higher retail sales  
- Precipitation may slightly reduce consumer activity  
- Temperature can be a valuable feature for retail forecasting  

### Future Improvements:
- Use a full-year dataset for more robust seasonality patterns  
- Include more granular product categories  
- Try advanced ML models (e.g., Random Forest, XGBoost) for better performance  

---

## 🧪 How to Run

1. Clone the repo:
```bash
git clone https://github.com/pelinozcelik/DSA210-Project.git
```

2. Open `final_report.ipynb` in Jupyter or Google Colab  
3. Run all cells to reproduce the full workflow  

---

## 📎 Disclosure

- Weather data collected using the `meteostat` Python package  
- Retail data is synthetic/public for educational use  
- Model results may vary based on randomness in train/test split

---

## 📦 Dependencies

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `meteostat`
