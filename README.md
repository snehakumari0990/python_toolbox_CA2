# python_toolbox_CA2
A Python-based data analysis project on the Indian Climate Dataset (2024–2025). The project involves data preprocessing, exploratory data analysis (EDA), and visualization to uncover trends in temperature, rainfall, and climate patterns using libraries like Pandas, NumPy, Matplotlib, and Seaborn.
# 🌦️ Indian Climate Data Analysis (2024–2025)

Exploratory Data Analysis and Predictive Modeling on daily climate records from 10 major Indian cities over 2 years.

---

## 📌 Project Overview

This project analyzes how climate variables like temperature, rainfall, humidity, and air quality vary across Indian cities. The goal is to uncover seasonal patterns, test statistical hypotheses, and build a regression model to predict temperature.

Key areas explored:
- Seasonal temperature trends across cities
- Relationship between rainfall and humidity
- Air quality (AQI) distribution and pollution hotspots
- Statistical impact of rainfall on temperature
- Predicting temperature using climate features

---

## 📂 Dataset

**File:** `Indian_Climate_Dataset_2024_2025.csv`

| Column | Description |
|--------|-------------|
| Date | Date of recording |
| City | One of 10 Indian cities |
| State | Corresponding state |
| Temperature_Max / Min / Avg (°C) | Daily temperature readings |
| Humidity (%) | Moisture level in air |
| Rainfall (mm) | Daily rainfall amount |
| Wind_Speed (km/h) | Wind speed |
| AQI | Air Quality Index value |
| AQI_Category | Good / Satisfactory / Moderate / Poor / Very Poor |
| Pressure (hPa) | Atmospheric pressure |
| Cloud_Cover (%) | Sky cloudiness percentage |

- **7,310 records** · **13 columns** · **No missing values**
- Cities: Mumbai, Delhi, Bengaluru, Chennai, Kolkata, Hyderabad, Ahmedabad, Jaipur, Lucknow, Bhopal

---

## 🧹 Data Cleaning & Preprocessing

- Converted `Date` column to datetime format
- Verified and confirmed zero missing values
- Created new features: `Month`, `Year`, `Season`, `Month_Name`, `Day_of_Week`
- Defined seasons: Winter (Dec–Feb), Summer (Mar–May), Monsoon (Jun–Sep), Autumn (Oct–Nov)
- Separated rainy vs dry days for hypothesis testing

---

## 📊 Exploratory Data Analysis

- Distribution histograms for Temperature, Humidity, and AQI
- Statistical summary of all numeric columns
- Records per city verification

---

## ❓ Key Questions & Insights

### 1️⃣ How does temperature vary across cities and seasons?
- Line chart of monthly average temperature for 5 major cities
- Seasonal boxplot comparing Winter, Summer, Monsoon, Autumn
- **Insight:** Delhi shows the widest temperature range; Bengaluru remains the most stable year-round

### 2️⃣ Is there a relationship between rainfall and humidity?
- Scatter plot of Rainfall vs Humidity
- Full correlation heatmap across all climate variables
- **Insight:** Moderate positive correlation between rainfall and humidity

### 3️⃣ Which cities have the worst air quality?
- Bar chart of average AQI per city
- Count plot of AQI categories across all records
- **Insight:** Over 47% of recorded days fall under Poor or Very Poor AQI — only 251 out of 7,310 days recorded "Good" air quality

### 4️⃣ Does rainfall significantly affect temperature? (Hypothesis Testing)
- Split data into rainy days (Rainfall > 0) and dry days
- Two-sample independent t-test
- **H₀:** No difference in temperature between rainy and dry days
- **H₁:** Rainfall significantly affects temperature
- **Insight:** p-value < 0.05 → Reject H₀; rainfall does have a statistically significant cooling effect

### 5️⃣ Can we predict average temperature from climate features? (Linear Regression)
- Features: Humidity, Wind Speed, Rainfall, Pressure
- Target: Temperature_Avg
- Metrics: R² Score, Mean Absolute Error (MAE)
- **Insight:** Pressure and Humidity are the strongest predictors of temperature

### 6️⃣ Which climate variables are most correlated with each other?
- Full correlation matrix heatmap
- Feature importance bar chart from regression coefficients
- Outlier detection boxplots for all key variables
- **Insight:** Temperature_Max and Temperature_Min are highly collinear; Pressure shows a negative relationship with temperature

---

## 🛠️ Technologies Used

- Python · Pandas · NumPy · Matplotlib · Seaborn · Scikit-learn · SciPy

---

## 📂 File Structure

```
├── Indian_Climate_Dataset_2024_2025.csv
├── preprocessing_eda.py
├── objective1_temperature.py
├── objective2_rainfall_humidity.py
├── objective3_aqi.py
├── objective4_hypothesis.py
├── objective5_regression.py
├── objective6_correlation_importance.py
└── plots/
    ├── plot0_distributions.png
    ├── plot1_temperature_trend.png
    ├── plot2_seasonal_boxplot.png
    ├── plot3_rainfall_vs_humidity_scatter.png
    ├── plot4_correlation_heatmap.png
    ├── plot5_avg_aqi_per_city.png
    ├── plot6_aqi_category_distribution.png
    ├── plot7_hypothesis_test.png
    ├── plot8_actual_vs_predicted.png
    ├── plot9_coefficients.png
    ├── plot10_full_correlation.png
    ├── plot11_feature_importance.png
    └── plot12_outliers_boxplot.png
```

---

## ▶️ How to Run

```bash
pip install pandas matplotlib seaborn scikit-learn scipy
python preprocessing_eda.py
python objective1_temperature.py
python objective2_rainfall_humidity.py
python objective3_aqi.py
python objective4_hypothesis.py
python objective5_regression.py
python objective6_correlation_importance.py
```

---

## 📈 Key Learnings

- Air quality across India is poor — "Good" AQI days are rare
- Rainfall has a statistically significant cooling effect on temperature
- Pressure is the strongest single predictor of daily average temperature
- Bengaluru is the most climatically stable city; Delhi shows the most seasonal extremes
- Older, established cities don't always have better air quality

---

## 👤 Author

Sneha kumari
Python Toolbox Project · 2025
