# 🌲 Forest Cover Prediction using Machine Learning

## 📌 Project Overview
This project predicts forest cover type using machine learning models based on environmental and geographical features.

## 🚀 Key Result
- Best Model: XGBoost
- Accuracy: ~88%

## 📊 Model Comparison Table
![Comparison Table](images/comparison_table_classification_models.png) 

## 📋 Classification Report
![Classification Report](images/classification_report_XGBoost.png) 

## 🔍 Confusion Matrix
![Confusion Matrix](images/Confusion_Matrix_XGBoost.png) 

## 📊 Model Comparison (Bar Chart)
![Model Comparison](images/Model_accuracies.png)  

## 🌲 Project Report
### 📌 1. Introduction

Forest cover type prediction is an important problem in environmental science and land management. It involves identifying the type of forest cover based on various geographical and environmental features such as elevation, soil type, and distance to hydrology. Machine learning techniques can effectively model these relationships and provide accurate predictions.

## 🎯 2. Problem Statement

The objective of this project is to build a machine learning model that can predict the forest cover type (multi-class classification) based on cartographic variables such as elevation, slope, soil type, and wilderness area.

## 📊 3. Dataset Description

The dataset consists of multiple numerical and categorical features related to forest characteristics.

🔢 Continuous features: Elevation, Aspect, Slope, Distances, Hillshade values
🧩 Binary features: Wilderness Area (4 columns), Soil Type (40 columns)
🎯 Target variable: Cover_Type (7 classes representing different forest cover types)

## 🧹 4. Data Cleaning
✔ Checked for missing values → No null values found
✔ Checked for duplicate records → No duplicates found
✔ Dataset was clean and ready for analysis

## 🔍 5. Exploratory Data Analysis (EDA)
### 📌 5.1 Target Variable Analysis
Used countplot to analyze class distribution
Observed that all classes are evenly distributed (balanced dataset)
### 📈 5.2 Feature Distribution
Histograms plotted for numerical features
Observed skewness in distance-related features
Hillshade features showed relatively normal distributions
### 🔗 5.3 Correlation Analysis
Heatmap used to identify relationships between features
Some moderate correlations observed (e.g., elevation with distances)
No severe multicollinearity detected
### 📊 5.4 Feature vs Target Analysis
Boxplots used to compare numerical features with target
Certain features like elevation showed clear separation across classes
### ⚠️ 5.5 Outlier Analysis
Outliers were observed in several numerical features
These were not removed as they represent real-world geographical variations
Removing them could lead to loss of important information

## ⚙️ 6. Data Preprocessing
### 🔹 6.1 Defining Features and Target
X = input features
y = target variable
y = data["Cover_Type"]-1

Reason:
XGBoost requires class labels to start from 0. Hence, labels were shifted from (1 to 7) to (0 to 6).

## 🔹 6.2 Train-Test Split
Dataset split into training and testing sets (80:20 ratio).

## 🧪 7. Feature Engineering
Applied StandardScaler only on numerical columns
Binary features (0/1) were not scaled as they are already normalized
Scaling improves performance of models like Logistic Regression

## 🤖 8. Model Building

The following models were implemented:

Logistic Regression
Decision Tree
Random Forest
XGBoost

## 📉 9. Model Evaluation
Models were evaluated using accuracy
Final model evaluated using classification report and confusion matrix
Metrics used: Precision, Recall, F1-score

## 🔧 10. Hyperparameter Tuning
Performed using GridSearchCV
Applied on:
Random Forest
XGBoost
Improved model performance by optimizing parameters.

## 🏆 11. Final Model
XGBoost achieved the highest accuracy (~88%)
Selected as the final model.

## ⚡ 12. Challenges Faced
Handling high-dimensional data (many soil features)
Understanding feature relationships
Hyperparameter tuning complexity
Computational time during GridSearchCV
Interpreting evaluation metrics.

## 📚 13. References
Scikit-learn documentation
XGBoost documentation
Kaggle datasets and discussions
Online ML tutorials and resources

## 🧾 14. Conclusion

In this project, multiple machine learning models were developed to predict forest cover types. After thorough evaluation and hyperparameter tuning, XGBoost emerged as the best-performing model with an accuracy of approximately 88%. The model demonstrated strong and consistent performance across all classes, making it suitable for real-world applications.

## 📌 15. Summary

This project successfully applied machine learning techniques to a multi-class classification problem. Among all models, XGBoost provided the best results after tuning, demonstrating the effectiveness of ensemble learning methods.