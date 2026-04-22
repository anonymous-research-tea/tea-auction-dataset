# 📊 Dataset Metadata and Description

## Dataset Name
**Sri Lankan Tea Auction Dataset**

## Description
This dataset is a cleaned and integrated representation of Sri Lankan tea auction data, designed for reproducible forecasting and econometric analysis. It combines sale-level information, price observations across tea categories, and aligned weather features with temporal lags.

---

## 📁 Structure

- **Total Records:** 12,233  
- **Total Sales:** 105  
- **Features:** 26 columns  

---

## 🔑 Key Fields

- **sale_id**: Unique identifier for each auction sale (primary key)  
- **sale_number, sale_year, sale_date_raw**: Temporal identifiers  
- **catalogue / segment / elevation**: Tea classification attributes  
- **category, grade, tier**: Product-level breakdown  
- **price_mid_lkr**: Mid-price in LKR (target variable for modeling)  
- **region**: Assigned weather region  
- **fx_usd**: Exchange rate (LKR to USD)  

---

## 🌦️ Weather Features

Includes contemporaneous and lagged variables (up to 3 periods):

- **Temperature:** `temperature_2m_mean_mean` (lags 1–3)  
- **Precipitation:** `precipitation_sum_total` (lags 1–3)  
- **Sunshine Duration:** `sunshine_duration_total` (lags 1–3)  
- **Aggregated Indicator:** `avg_weather_severity`  

---

## 🧹 Data Processing Summary

- Harmonized multiple price sources into a unified schema  
- Applied rule-based mapping between tea segments and regions  
- Enforced single-region assignment per record  
- Consolidated exchange rate data into a single `fx_usd` feature  
- Removed invalid or unmatched records  
- Applied type-aware missing value handling  

---

## 🎯 Intended Use

- Time-series forecasting  
- Econometric modeling  
- Feature importance and causal analysis (e.g., weather impacts)  
- Benchmark dataset for tea market research  
