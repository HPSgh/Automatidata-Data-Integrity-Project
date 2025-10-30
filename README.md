# NYC Taxi Fare Prediction: Data Integrity and Feature Engineering

## Project Goal

To establish a robust, clean, and feature-rich dataset ready for training a Linear Regression Model to predict the total_amount of a New York City yellow taxi fare. This project focuses on solving critical data quality issues and engineering predictive features necessary for high-accuracy modeling.

## 💡 Strategic Context and Role

This project was undertaken as part of the Google Advanced Data Analytics Professional Certificate. The methodology, feature engineering, and strategic recommendations were independently developed and executed to meet the standards of a production-ready data pipeline.


| Element | Description |
| --- | --- |
| Client | New York City Taxi and Limousine Commission (TLC) / Automatidata |
| Objective | Predict total_amount to improve fare transparency and detect potential fraud. |
| Role | Data Analyst: Responsible for the entire Data Preparation and Integrity Phase. |


## Key Accomplishments & Value Delivered

This notebook transforms raw 2017 trip data into a model-ready asset through rigorous quality assurance and feature engineering.

| Action | Technical Deliverable | Impact |
| --- | --- | --- |
| Data Integrity | Systematic filtering of non-sensical data (negative fares, zero distances, $0$ passenger count). | Removed 0.847% of original records, ensuring the training dataset is logically sound and robust against bias. |
| Feature Engineering | Engineered two high-value time-based predictors: trip_duration_minutes and avg_speed_mph. | Provided essential context for the regression model, confirming that trip_distance and trip_duration_minutes are the primary non-financial drivers of fare price. |
| Model Readiness Check | Confirmed all core features are correctly typed and within logical boundaries (e.g., speed capped at 60 MPH). | Prevented model failure by identifying and correcting inherent data quality issues before training. |


## 🚀 Critical Strategic Finding (Pre-Modeling Plan)

Exploratory Data Analysis (EDA) revealed that the target variable, total_amount, and all primary predictors are highly right-skewed (long-tailed).

* Conclusion: This violates the assumption of normality required by linear regression.

* Next Step: Before model fitting, a logarithmic transformation must be applied to these skewed variables. This is the crucial final step to ensure high model performance and reliable results.

## Project Files

* `Automatidata-Data-Integrity-Project.ipynb`/ `Automatidata-Data-Integrity-Project.pdf`: Complete notebook containing the data cleaning, feature engineering, EDA, and strategic conclusion.

* `Executive summary.ipynb`: Formal memo reporting findings and next steps to the project management team.

* `2017_Yellow_Taxi_Trip_Data.`: The original data source used for the analysis.

_Author: Htoo Pyae Shan_
