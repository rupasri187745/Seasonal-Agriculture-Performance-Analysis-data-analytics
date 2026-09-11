# Seasonal Agriculture Performance Analysis

## 📌 Project Overview
This project performs an end-to-end data analytics study on agricultural performance across different farming seasons—**Kharif**, **Rabi**, and **Zaid**. Agricultural outcomes vary significantly depending on seasonal variations in rainfall, temperature, soil conditions, resource usage, and market pricing. 

The primary goal of this project is to investigate seasonal differences, discover patterns in resource efficiency and crop yield, and provide evidence-based recommendations to optimize seasonal agricultural planning.

---

## 📁 Dataset Description
The dataset contains **4,000 records** and **28 attributes** representing agricultural activities, environmental parameters, resource metrics, and economic performance.

### Key Columns:
* **Categorical / Identification:** `Farm_ID`, `State`, `District`, `Crop`, `Season`, `Irrigation_Method`.
* **Environmental Factors:** `Rainfall_mm`, `Avg_Temperature_C`, `Humidity_pct`, `Sunlight_Hours_Day`, `Soil_pH`, `Soil_Moisture_pct`.
* **Resource Usage:** `Nitrogen_kg_ha`, `Phosphorus_kg_ha`, `Potassium_kg_ha`, `Fertilizer_kg_ha`, `Pesticide_Litre_ha`, `Water_Used_m3`, `Seed_Quality_Score`.
* **Performance & Economic Outcomes:** `Farm_Area_Hectares`, `Yield_Tonnes_Ha`, `Production_Tonnes`, `Market_Price_INR_Tonne`, `Total_Cost_INR`, `Revenue_INR`, `Profit_INR`, `Water_Efficiency_t_per_1000m3`, `Disease_Pest_Risk_pct`.

---

## 🛠️ Tech Stack & Dependencies
* **Programming Language:** Python 3.x
* **Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`
* **Environment:** Jupyter Notebook (`.ipynb`)

---

## 🔬 Project Workflow & Checklist Implementation

This project fulfills all 18 standard project criteria:

### 1. Dataset Loading & Inspection
* Loaded `seasonal_agriculture_performance_dataset.csv` into a Pandas DataFrame.
* Verified structural dimensions: **4,000 rows** and **28 columns**.
* Inspected initial rows (`df.head()`) and confirmed data types across integer, float, and object columns.

### 2. Data Cleaning & Preprocessing
* **Missing Value Imputation:** Identified missing entries in `Rainfall_mm` (48), `Soil_Moisture_pct` (40), and `Yield_Tonnes_Ha` (32). Imputed missing values using feature medians to maintain robustness against skewed distributions.
* **Duplicate Check:** Verified 0 duplicate records across the dataset.

### 3. Exploratory Data Analysis (EDA)
* **Descriptive Statistics:** Computed central tendencies, standard deviations, and range distributions for numeric and categorical attributes.
* **Outlier Analysis:** Created boxplots for `Yield_Tonnes_Ha`, `Profit_INR`, and `Rainfall_mm` to evaluate distribution spreads and extreme values.
* **Univariate Analysis:** Visualized the frequency distribution of records across seasons and crop types.
* **Bivariate Analysis:** Evaluated average `Revenue_INR` and `Profit_INR` across the three farming seasons.
* **Multivariate Analysis:** Analyzed interaction patterns of average crop yield (`Yield_Tonnes_Ha`) grouped simultaneously by `Crop` and `Season`.
* **Correlation Analysis:** Generated a correlation heatmap linking weather factors, resource inputs, yield, and financial parameters.

### 4. Custom Student-Designed Analyses
1. **Water Efficiency by Irrigation & Season:** Evaluated `Water_Efficiency_t_per_1000m3` distributions across different irrigation techniques (`Drip`, `Flood`, `Rainfed`) per season.
2. **Pest/Disease Risk vs. Profitability:** Analyzed scatter relationship between `Disease_Pest_Risk_pct` and `Profit_INR` across seasons.
3. **Profit Density per Hectare:** Created violin plots showing profit distribution scaled per hectare (`Profit_INR / Farm_Area_Hectares`) by season.

---

## 📊 Key Findings & Insights

1. **Seasonal Revenue & Profit Disparity:** Kharif and Rabi seasons generate significantly higher average revenue and profit compared to the off-peak Zaid season.
2. **Missing Value Structure:** Missing values were localized to environmental and output fields (`Rainfall_mm`, `Soil_Moisture_pct`, `Yield_Tonnes_Ha`) and handled via median replacement.
3. **Yield Anomalies:** Highly skewed yield peaks (reaching up to 101.44 Tonnes/Ha) indicate localized high-density farming or extreme yield variance.
4. **Irrigation Efficiency:** Modern drip irrigation delivers consistently higher water efficiency ($t / 1000m^3$) than traditional flood irrigation across all seasons.
5. **Rainfall Impact:** Total rainfall during Kharif cycles shows strong positive alignment with soil moisture retention.
6. **Input Efficiency Thresholds:** High fertilizer application rates ($kg/ha$) show diminishing marginal returns beyond specific threshold limits.
7. **Pest Risk Vulnerability:** Warm, high-humidity seasonal periods show heightened `Disease_Pest_Risk_pct` levels.
8. **Negative Margin Risk:** Off-peak seasonal farming exhibits higher frequencies of negative profit margins driven by elevated water usage costs.

---

## 💡 Practical Recommendations

* **Transition Irrigation Infrastructure:** Promote drip irrigation deployment over flood irrigation, particularly in dry season cultivation.
* **Optimal Fertilizer Application:** Provide soil-testing guidelines to prevent cost inflation caused by over-fertilization.
* **Seasonal Crop Selection:** Encourage low-water-requirement crops (like pulses) during the Zaid season rather than water-intensive crops.

---

## ⚠️ Limitations

* **Time-Series Scope:** Dataset represents fixed observation periods without multi-year longitudinal tracking.
* **Price Volatility:** Market pricing remains static per record without real-time intra-season price fluctuation data.

---

## 🏁 Conclusion

Seasonal variations exert a major influence on crop yield, input efficiency, and financial return. Using data-driven seasonal insights allows agricultural stakeholders to optimize resource management, mitigate pest risks, and stabilize farm profitability.


##### GITHUB LINK :
https://github.com/rupasri187745/Seasonal-Agriculture-Performance-Analysis-data-analytics
