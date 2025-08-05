# 🧠 Semiconductor Yield Classification using Machine Learning
This project is focused on developing a classification model to predict Pass/Fail outcomes of semiconductor manufacturing processes based on sensor signal data. The goal is to assist engineers in identifying crucial factors that influence manufacturing yield, leading to improved efficiency, reduced costs, and enhanced product quality.

### 📌 Problem Statement
Semiconductor manufacturing involves highly complex and sensitive processes, monitored through hundreds of sensor signals and process measurements. Despite extensive monitoring, not all signals are relevant, and some may introduce noise.

This project aims to:

Build a machine learning classifier to predict the Pass/Fail (Yield) of a process entity.

Identify the most relevant sensor features using feature selection and model explainability.

Help process engineers reduce production cost and increase throughput by focusing on critical signals.

### 🧾 Dataset Description
File: signal-data.csv

Rows: 1,567 (each row = one manufacturing unit)

Features: 591 numerical sensor signals

Target: Pass/Fail (Label: -1 = Pass, 1 = Fail)

Challenge: High-dimensional data with potential noise, imbalance in class distribution, and missing values.

### 🛠️ Project Workflow
1. Data Preprocessing
Removed non-numeric Time column

Handled missing values:

Dropped features with >5% missing values

Removed remaining rows with missing data

Final dataset was cleaned and consistent

2. Exploratory Data Analysis (EDA)
Visualized class imbalance

Explored distribution of key signals

Heatmap for correlation (limited features for interpretability)

3. Class Balancing
Used SMOTE (Synthetic Minority Oversampling Technique) to address imbalance in the Pass/Fail target variable

4. Feature Scaling
Applied StandardScaler to normalize sensor signal values before model training

5. Model Building
Three supervised ML models were trained and evaluated:

✅ Random Forest Classifier

✅ Support Vector Machine (SVM)

✅ Naive Bayes Classifier

Each model was:

Trained on 80% of the dataset

Evaluated using confusion matrix, precision, recall, and F1-score

6. Model Comparison
All models were compared on test accuracy and F1-score

Random Forest performed best in terms of balanced accuracy and interpretability

7. Feature Importance
Extracted feature importance scores from the Random Forest model

Identified top 20 sensor signals contributing to failure prediction

### 🔍 Results
Accuracy (Random Forest): ~92%

Most important signals: Often aligned with known critical points in the manufacturing line

Engineers can now prioritize monitoring these key signals for early detection of potential failures

### 📈 Future Improvements
Apply dimensionality reduction (PCA) to simplify data further

Use advanced models like XGBoost or LightGBM for performance boosting

Add real-time predictive monitoring pipeline using saved model

Integrate domain-specific knowledge to guide feature selection

## 🧠 Learning Outcomes
Through this project, I gained hands-on experience in:

High-dimensional data handling

Class imbalance strategies

Feature selection & engineering

Building and evaluating multiple classification models

Model explainability using feature importance

### 💾 Dataset Source
Proprietary or simulated semiconductor process dataset with anonymized sensor data provided for learning purposes.
