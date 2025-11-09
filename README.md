EV Charging Cost Prediction using Machine Learning and Explainable AI
Overview

This project presents an end-to-end data science workflow for analyzing Electric Vehicle (EV) charging station data and predicting charging costs using CatBoost Regression with explainability powered by SHAP.
It combines data analytics, machine learning, and business intelligence visualization to deliver insights into factors influencing EV charging costs and to support decision-making for optimizing station performance.

Objectives

Analyze large-scale EV charging datasets to extract patterns and relationships.

Predict the approximate charging cost per session using advanced machine learning algorithms.

Identify the most influential factors affecting charging cost using SHAP explainability.

Visualize model performance and key business KPIs using an interactive Power BI dashboard.

Key Features

Data Integration and Cleaning

Combined multiple publicly available EV datasets into a unified structure.

Performed preprocessing using Excel Power Query and Python.

Created derived KPI: Energy Cost Efficiency.

Removed inconsistencies and missing values using pandas and NumPy.

Exploratory Data Analysis (EDA)

Conducted exploratory analysis to understand distributions, outliers, and trends.

Visualized insights using Matplotlib and Seaborn (correlation matrix, boxplots, trend lines).

Extracted insights on:

Average charging duration by vehicle model.

Average energy consumption by user type.

Most active states and cities by total energy consumption.

Time-of-day and day-of-week charging behavior patterns.

SQL-Based Analytical Queries
Utilized pandasql to perform key aggregations and insights such as:

Top 5 cities with the highest total energy consumption.

Average charging cost per charger type.

Average duration per vehicle model.

Cities with the highest average charging cost.

Demand comparison by user type and charger type.

Most frequent charging time windows and active days.

Machine Learning Model (CatBoost Regressor)

Implemented a CatBoost Regression model to predict Charging Cost (USD).

Applied TimeSeriesSplit for temporal data validation.

Used RandomizedSearchCV for hyperparameter optimization.

Employed feature pooling (CatBoost Pool) for efficient categorical encoding.

Evaluated using MAE, RMSE, and R² metrics.

Model Explainability (SHAP)

Implemented SHAP (SHapley Additive exPlanations) for interpreting feature importance.

Visualized contribution of each feature to cost predictions.

Identified the most significant predictors:

Day of Week

Vehicle Model

Time of Day

Charger Type

City

State of Charge (Start % and End %)

Energy Cost Efficiency

Interactive Dashboard (Power BI)

Built a dynamic Power BI dashboard to visualize:

Actual vs Predicted Charging Cost (Scatter Plot)

Error Distribution (Histogram)

SHAP Feature Importance (Bar Chart)

Performance KPIs (MAE, RMSE, R², Average Costs)

Used a modern layout and background theme for clarity and professional presentation.

Project Architecture
EV Charging Station Analysis + Cost Prediction
│
├── Dashboard/
│   └── EV Charging Cost Prediction Dashboard.pbix
│
├── EV Datasets/
│   ├── master_corrected_data.xlsx
│   ├── ev_cleaned_data.xlsx
│   ├── EV charging Dataset.xlsx
│   ├── EV Final Data.xlsx
│   └── analysis_results.xlsx
│
├── ML/
│   ├── catboost_ev_ML_model.cbm
│   ├── predictions_vs_actual.csv
│   ├── shap_feature_importance.csv
│   ├── shap_features_TEST.csv
│   └── shap_values_TEST.npy
│
└── ev_cost_prediction_colab.ipynb

Technologies and Tools
Category	Tools and Libraries
Data Handling	Python, pandas, NumPy, Excel (Power Query, Pivot Tables)
Visualization	Matplotlib, Seaborn, Power BI
Machine Learning	CatBoost, Scikit-learn
Explainability	SHAP
Querying and Analysis	pandasql (SQL in Python)
Model Validation	train_test_split, TimeSeriesSplit, RandomizedSearchCV
Model Performance Summary
Metric	Value
Mean Absolute Error (MAE)	0.50
Root Mean Square Error (RMSE)	0.72
Coefficient of Determination (R²)	1.00
Average Actual Cost	22.55
Average Predicted Cost	22.55
Results and Insights

The model achieved near-perfect predictive performance (R² ≈ 1.0) due to strong feature correlations and proper parameter tuning.

Day of Week, Vehicle Model, and Time of Day are the strongest predictors of charging cost.

Energy efficiency and charger type significantly impact charging cost variations.

SHAP plots confirm that the model is interpretable and behaves consistently with business intuition.

The Power BI dashboard provides a unified view of predictions, errors, and key influencing features.

Folder Summary

EV Datasets/ – Original and processed datasets used for model training and analysis.

ML/ – Machine learning model, explainability outputs, and prediction results.

Dashboard/ – Final Power BI visualization integrating model insights.

ev_cost_prediction_colab.ipynb – Main notebook covering data cleaning, EDA, modeling, and SHAP analysis.

How to Run the Project

Clone this repository:

git clone https://github.com/themdsaqib29/EV-Charging-Station-Analytics-and-Charging-Cost-Prediction.git


Open the notebook in Google Colab or Jupyter.

Install dependencies:

pip install pandas numpy matplotlib seaborn catboost shap pandasql scikit-learn


Run the notebook cells sequentially to reproduce the results.

Open the Power BI file (.pbix) to explore the interactive dashboard.

Future Scope

Integrate live EV charging station data through APIs for real-time analytics.

Extend the model to predict charging demand or energy utilization.

Deploy the predictive model as a web application for operational insights.

Incorporate more advanced interpretability frameworks such as LIME or ELI5.

Dataset Link

Google Drive Link - https://drive.google.com/drive/folders/1XmI-0Cvyj1Mvaa1vOJz75SdZUClLYyCj?usp=sharing

Author

Mohamed Saqib N
Final Year B.Tech – Computer Science Engineering (Big Data Analytics)
SRM Institute of Science and Technology, Vadapalani Campus

License

This project is released under the MIT License.
You are free to use, modify, and distribute this work with proper attribution.

Repository Link

GitHub Repository – EV Charging Station Analytics and Charging Cost Prediction