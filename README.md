# 🚲 Bicycle Rental Data Analysis & Predictive Modeling

This project presents an end-to-end data analysis and predictive modeling workflow based on a bicycle rental dataset. The main objectives were to understand the factors influencing **rider satisfaction** and **rental cost**, while applying various data science techniques including feature engineering, dimensionality reduction, statistical testing, and machine learning.

---

## 📊 Project Objectives

- Analyze factors impacting rider satisfaction.
- Predict bicycle rental costs.
- Evaluate dimensionality reduction and feature selection techniques.
- Compare classification and regression models.
- Provide actionable recommendations for pricing and service optimization.

---

## 🧹 Data Preprocessing

- **Conversion & Cleaning**: Dataset originally in XLSX, converted to CSV.
- **Missing Value Imputation**: Custom function using feature-based "neighbors" with median (numeric) or mode (categorical).
- **Outlier Detection**: Visual checks revealed no major outliers.
- **Feature Creation**: New variables created including speed, cost per km, and cost per minute.
- **Encoding & Scaling**: Applied OneHotEncoding, LabelEncoding, MinMaxScaler, and StandardScaler depending on the feature type and algorithm requirements.

---

## ⚙️ Feature Engineering & Dimensionality Reduction

- **Feature Selection**: Random Forest used to identify variables most relevant to satisfaction.
- **PCA**: Reduced to 20 components, retaining 99.5% of variance.
- **LDA**: Reduced to 2 linear discriminants optimized for classification.

---

## 📈 Statistical Analysis

- Contingency tables for city vs. weather, city vs. bike model, and bike model vs. satisfaction.
- Normality testing using Shapiro-Wilk (none of the variables followed a normal distribution).
- ANOVA and t-tests confirmed no significant differences in cost across satisfaction levels or between cities.
- Covariance and correlation analysis showed strong relationships between duration and cost.

---

## 🤖 Machine Learning Models

### 🔍 Classification – Predicting Rider Satisfaction

- Models tested: Decision Tree, Random Forest, KNN.
- Variants: original, scaled, PCA-reduced, and LDA-reduced datasets.
- Results: Low accuracy and F1-score across all configurations.
- Conclusion: Satisfaction likely depends on subjective factors not included in the dataset.

### 💰 Regression – Predicting Rental Cost

- Best results from Random Forest Regressor (high R², low MAE/MSE).
- Hyperparameter tuning via GridSearchCV.
- 10-fold cross-validation confirmed generalization and performance.

---

## 🧩 Key Conclusions

- The dataset contains inconsistencies (e.g., extreme speed values).
- Rider satisfaction could not be predicted reliably with available data.
- Cost prediction was successful, mainly due to strong correlation with duration and distance.
- Improving data quality and including more contextual or subjective features is essential.

---

## 📚 References

- [DataTab – ANOVA & T-Test](https://datatab.net/tutorial/unpaired-t-test)  
- [IBM – Supervised vs. Unsupervised Learning](https://www.ibm.com/think/topics/supervised-vs-unsupervised-learning)  
- [BuiltIn – Step-by-step PCA Guide](https://builtin.com/data-science/step-step-explanation-principal-component-analysis)  
- [Corporate Finance Institute – Covariance](https://corporatefinanceinstitute.com/resources/data-science/covariance/)

---

## 🔗 GitHub Repository

[https://github.com/CCT-Dublin/ca2-AntonioGiambra](https://github.com/CCT-Dublin/ca2-AntonioGiambra)
