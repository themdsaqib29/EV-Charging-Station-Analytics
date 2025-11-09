# EV Charging Station Analytics and Cost Prediction

## Overview
This project provides an end-to-end data science pipeline for analyzing EV charging station data and predicting charging costs using machine learning. It integrates data cleaning, exploratory analysis, feature engineering, CatBoost regression modeling, SHAP explainability, and Power BI visualization for actionable insights in electric vehicle (EV) infrastructure analytics.

---

## Project Structure
EV-Charging-Station-Analytics/
│
├── Colab Notebook/ # Python notebook for data cleaning, EDA, ML, and SHAP explainability
├── Dashboard/ # Power BI dashboard (charging cost prediction + feature importance)
├── EV Dataset/ # Contains sample_data.csv (for demo)
├── ML/ # Model outputs, SHAP values, and predictions
├── README.md # Documentation file
└── .gitignore # Git ignore rules for large/unnecessary files

---

## Workflow Summary

### 1. Data Preparation (Excel + Power Query)
- Combined multiple EV datasets using **Excel Power Query** and **PivotTables**
- Created a new KPI: **Energy Cost Efficiency**
- Exported the final cleaned dataset for ML processing

### 2. Data Cleaning and Analysis (Python / Google Colab)
- Used **pandas**, **numpy**, and **matplotlib** for preprocessing and exploration
- Visualized trends and relationships with **seaborn** and **correlation heatmaps**
- Conducted statistical analysis and handled missing/inconsistent data

### 3. SQL-Based Data Insights (pandasql)
- Derived key insights such as:
  - Top 5 cities with highest energy consumption  
  - Average charging cost per charger type  
  - Average charging duration by vehicle model  
  - City with the highest EV charging cost  
  - Day and time with peak charging demand

### 4. Machine Learning (CatBoost Regressor)
- Built a **CatBoost Regression Model** for charging cost prediction  
- Applied:
  - `train_test_split` for data partitioning  
  - `TimeSeriesSplit` for temporal validation  
  - `RandomizedSearchCV` for hyperparameter tuning  
  - `Pool` for efficient CatBoost training  
- Achieved:
  - **MAE:** 0.50  
  - **RMSE:** 0.72  
  - **R² Score:** 0.99  

### 5. Explainability (SHAP)
- Implemented **SHAP (SHapley Additive exPlanations)** for model interpretability  
- Identified top features influencing EV charging cost:  
  1. Day of Week  
  2. Vehicle Model  
  3. Time of Day  
  4. Charger Type  
  5. City  

### 6. Visualization (Power BI)
- Created an interactive dashboard integrating ML results, metrics, and explainability
- Components include:
  - KPI cards (Actual Cost, Predicted Cost, MAE, RMSE, R²)
  - Actual vs Predicted Cost Scatterplot
  - Error Distribution Histogram
  - SHAP Feature Importance Chart
- Designed for both **data scientists** and **business analysts**

---

## Dataset Link
Full dataset available on Google Drive: [Google Drive Link](https://drive.google.com/drive/folders/1XmI-0Cvyj1Mvaa1vOJz75SdZUClLYyCj?usp=sharing)

Sample dataset for demo: `EV Dataset/sample_data.csv`

---

## Power BI Dashboard
Download the dashboard file: [EV Charging Cost Prediction Dashboard (.pbit)](https://drive.google.com/drive/folders/1Iug3IIS_4P4CrEPuEa3HcEHV99IQh5iG?usp=sharing)

---

## Colab Notebook
Access the full analysis and model notebook on Google Colab:  
[Open in Colab](https://colab.research.google.com/drive/18IQL5beIHNGG4XOhmSH_LHKhzqq0nCzD?usp=sharing)

---

## Tech Stack

| Category | Tools / Libraries |
|-----------|-------------------|
| **Programming Language** | Python |
| **Data Processing** | pandas, numpy |
| **Visualization** | matplotlib, seaborn, Power BI |
| **Machine Learning** | CatBoost, scikit-learn |
| **Explainability** | SHAP |
| **SQL Queries** | pandasql |
| **Development Platform** | Google Colab |
| **Version Control** | Git & GitHub |

---

## Key Results

| Metric | Value |
|---------|--------|
| Avg Actual Cost | 22.55 |
| Avg Predicted Cost | 22.55 |
| MAE | 0.50 |
| RMSE | 0.72 |
| R² Score | 0.99 |

**Top Features by Importance (SHAP):**  
Day of Week, Vehicle Model, Time of Day, Charger Type, City

---

## Conclusion
This project demonstrates how **machine learning** and **explainable AI** can improve decision-making for EV infrastructure planning.  
By integrating **SHAP explainability** with **Power BI visual analytics**, it bridges the gap between model interpretability and business insights — providing a robust, data-driven approach to EV charging cost prediction.

---

## Future Scope
- Expand to real-time EV charging data APIs
- Incorporate geographical visualizations using Power BI maps
- Deploy model as a web service for live cost predictions

---

## License
This project is released under the **MIT License**.  
You are free to use, modify, and distribute this work with proper attribution.

---

## Author
**Mohamed Saqib**  
Final Year B.Tech, Computer Science Engineering (Big Data Analytics)  
SRM Institute of Science and Technology 

LinkedIn: [LinkedIn Profile](https://www.linkedin.com/in/mohamed-saqib1029)  
GitHub: [https://github.com/themdsaqib29](https://github.com/themdsaqib29)
