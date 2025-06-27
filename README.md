🚲 Bicycle Rental Data Analysis & Predictive Modeling
This project presents an end-to-end data analysis and predictive modeling workflow based on a bicycle rental dataset. The main objectives were to understand the factors influencing rider satisfaction and rental cost, while applying various data science techniques including feature engineering, dimensionality reduction, statistical testing, and machine learning.

📊 Project Objectives
Analyze factors impacting rider satisfaction.

Predict bicycle rental costs.

Evaluate dimensionality reduction and feature selection techniques.

Compare classification and regression models.

Provide actionable recommendations for pricing and service optimization.

🧹 Data Preprocessing
Conversion & Cleaning: Dataset originally in XLSX, converted to CSV.

Missing Value Imputation: Custom function using feature-based "neighbors" with median (numeric) or mode (categorical).

Outlier Detection: Visual checks revealed no major outliers.

Feature Creation: New variables created including speed, cost per km, and cost per minute.

Encoding & Scaling: Applied OneHotEncoding, LabelEncoding, MinMaxScaler, and StandardScaler depending on the feature type and algorithm requirements.

⚙️ Feature Engineering & Dimensionality Reduction
Feature Selection: Random Forest used to identify variables most relevant to satisfaction.

PCA: Reduced to 20 components, retaining 99.5% of variance.

LDA: Reduced to 2 linear discriminants optimized for classification.

📈 Statistical Analysis
Contingency Tables: Explored relationships between city, bike model, and weather.

Normality Testing: Shapiro-Wilk test suggested non-normal distributions.

ANOVA & T-Tests: No significant difference found between satisfaction levels or cities in terms of cost.

Covariance & Correlation: Strong linear relationship between duration and cost (Covariance = 289, R² ≈ 0.82).

🤖 Machine Learning Models
🔍 Classification – Predicting Rider Satisfaction
Models tested: Decision Tree, Random Forest, KNN.

Data variations: original, scaled, PCA-reduced, LDA-reduced.

Results: Low accuracy and F1-scores across all models.

Conclusion: Rider satisfaction likely depends on subjective or unrecorded variables not captured in the dataset.

💰 Regression – Predicting Rental Cost
Best performance from Random Forest Regressor (high R², low MAE/MSE).

Hyperparameter tuning with GridSearchCV.

10-fold cross-validation confirmed generalization and robustness.

🧩 Key Conclusions
The dataset suffers from quality issues (e.g., implausible values like 23 km in 5 minutes).

Rider satisfaction cannot be accurately predicted with available variables.

Cost prediction was successful thanks to strong relationships with duration and distance.

Improving data quality and completeness is essential, especially for subjective factors.

Final recommendation: use the optimized Random Forest model for cost estimation and revisit data collection strategy for satisfaction modeling.
