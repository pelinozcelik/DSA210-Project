# Weather and Retail Sales Patterns-DSA210 Project

## Project Overview
This project aims to investigate the relationship between weather conditions and retail sales for specific product categories. By analyzing historical weather data alongside sales figures, we seek to determine how different weather patterns influence consumer purchasing behavior. The findings could provide valuable insights for businesses in inventory planning, marketing strategies, and operational adjustments based on weather forecasts.

## Project Objectives
1. **Analyze the impact of weather conditions on retail sales**  
   - Investigate how variables such as temperature and precipitation influence consumer purchasing behavior.
2. **Identify seasonal trends in sales performance**  
   - Determine how different weather conditions across seasons affect the demand for specific product categories.
3. **Develop effective data visualizations to communicate findings**  
   - Use graphs, charts, and dashboards to present insights clearly.

## Research Questions & Hypotheses
### Research Questions:
1. How does temperature affect retail sales across different product categories?
2. Are sales of seasonal products (e.g., summer drinks, winter coats) significantly influenced by weather conditions?
3. Do extreme weather conditions (e.g., storms, heatwaves) lead to unusual spikes or drops in sales?

### Hypotheses:  
#### Temperature, Precipitation, and Sales
- **H1:** Higher temperatures lead to increased sales of summer-related products (e.g., cold beverages, ice cream, sunglasses).
- **H2:** Lower temperatures increase sales of winter-related products (e.g., hot beverages, coats, heaters).
- **H3:** Rainy weather increases sales of rain-related products (e.g., umbrellas, raincoats, waterproof shoes).
- **H4:** Sales of outdoor-related products (e.g., camping gear, sports equipment) are lower on rainy or stormy days.

#### Extreme Weather and Consumer Behavior
- **H5:** Severe weather conditions (e.g., storms, hurricanes) cause a temporary surge in the sales of emergency supplies (e.g., bottled water, canned food, batteries).

## Data Sources
### Sales Data
- **Source:** Publicly available retail sales datasets OR manually collected data from a selected retail business.
- **Variables:**
  - Date
  - Product category (e.g., beverages, clothing, outdoor equipment)
  - Daily sales revenue
  - Number of transactions

### Weather Data
- **Source:** Public APIs to obtain historical weather data.
- **Variables:**
  - Temperature (\u00b0C)
  - Precipitation (mm)
  - Weather condition (e.g., sunny, rainy, snowy)

## Data Collection Methodology
1. Gather historical sales data from a publicly available retail dataset or a business willing to share its sales data.
2. Use a weather API to extract historical weather conditions for the same time period as the sales data.
3. Merge the datasets by date, ensuring that each sales record has corresponding weather information.
4. Perform data cleaning, handling missing values and inconsistencies.
5. Conduct exploratory data analysis (EDA) to identify trends and patterns.

## Analysis Plan
- **Descriptive Statistics:** Summarize sales trends across different weather conditions.
- **Correlation Analysis:** Examine the strength of relationships between weather variables and sales.
- **Visualization:** Create charts (line plots, scatter plots, bar charts) to illustrate relationships.
- **Hypothesis Testing:** Conduct statistical tests to validate the proposed hypotheses.

## Data Sources & Links
### Weather Data Sources
- [NOAA Climate Data](https://www.ncdc.noaa.gov/)
- [OpenWeatherMap](https://openweathermap.org/)
- [WeatherStack](https://weatherstack.com/)
- [Meteostat](https://meteostat.net/)
- [Visual Crossing Weather](https://www.visualcrossing.com/)

### Retail Sales Data Sources
- [U.S. Census Bureau - Retail Trade](https://www.census.gov/retail/)
- [Kaggle Retail Datasets](https://www.kaggle.com/)
- [Google Dataset Search](https://datasetsearch.research.google.com/)
- [Data.gov](https://www.data.gov/)
- [Statista - Retail Sales](https://www.statista.com/)
- [European Central Bank Retail Statistics](https://sdw.ecb.europa.eu/)

### Additional Product-Specific Sales Data
- **Beverages (Cold & Hot Drinks):** [Kaggle Beverage Sales](https://www.kaggle.com/)
- **Clothing & Apparel:** [Fashion Sales Data](https://www.kaggle.com/)
- **Outdoor Equipment:** [Outdoor Recreation Economy Data](https://www.bea.gov/)
- **Emergency Supplies:** [FEMA - Emergency Preparedness](https://www.fema.gov/)
- **Seasonal Products:** [U.S. Retail Trade Data - Seasonal Sales](https://www.census.gov/retail/)


