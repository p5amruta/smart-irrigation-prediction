# Smart Irrigation Prediction using Machine Learning

##  Project Overview
This project focuses on predicting irrigation requirements for crops using
machine learning. The prediction is based on soil type, crop growth stage,
and environmental conditions such as moisture index, temperature, and humidity.

The model serves as a decision-support system for farmers, helping them
optimize water usage, reduce wastage, and prevent crop stress.

---

##  Problem Statement
The objective of this project is to build a machine learning model that predicts
the irrigation requirement category for a crop based on soil and environmental conditions
conditions.

This is formulated as a **classification problem**, where the output represents
different irrigation requirement levels. Accurate prediction helps farmers make
timely and informed irrigation decisions under varying environmental conditions.

---

##  Dataset Description
The dataset contains **16,411 crop records**, where each record represents a crop
sample observed under specific environmental conditions.

### Features:
- **crop_ID**: Unique identifier for the crop (categorical)
- **soil_type**: Type of soil (categorical)
- **Seedling_Stage**: Crop growth stage (categorical)
- **MOI (Moisture Index)**: Soil moisture content (numerical)
- **temp**: Ambient temperature in °C (numerical)
- **humidity**: Relative humidity percentage (numerical)

### Target Variable:
- **result**: Irrigation requirement category (multi-class)

---

## Data Preprocessing
The following preprocessing steps were applied:

- Dataset inspection using `info()` and `isnull()`
- No missing values were found, so no imputation was required
- Column names were standardized for cleaner and safer code usage
- Categorical features were encoded using **Label Encoding**
- Numerical features were scaled using **StandardScaler**
- Data was split into training and testing sets using an 80:20 ratio

---

##  Models Used

### 1️ Logistic Regression (Baseline Model)
- Used as a baseline classifier
- Provides interpretability and simplicity
- Limited in handling non-linear patterns and minority classes

### 2️ Random Forest Classifier (Improved Model)
- Captures non-linear relationships
- Handles class imbalance more effectively
- Provides feature importance for explainability

---

## 📊 Results and Evaluation Metrics

### Logistic Regression Results
- **Accuracy:** 82%
- Performed well on majority classes
- Failed to correctly classify the minority class (class 2)

This limitation is attributed to the linear nature of Logistic Regression and
class imbalance in the dataset.

---

### Random Forest Results
- **Accuracy:** 99%
- High precision, recall, and F1-score across all classes
- Successfully classified the minority class

Random Forest significantly outperformed Logistic Regression by capturing
complex interactions between soil and environmental factors.

---

##  Feature Importance
Feature importance analysis from the Random Forest model showed that:

- **Moisture Index (MOI)**
- **Temperature**

are the most influential factors in determining irrigation requirements.
This aligns well with real-world agricultural knowledge.

---

## ✅ Final Inference
Among the models evaluated, the Random Forest Classifier provided the best
overall performance. It effectively handled class imbalance and non-linear
relationships, producing accurate predictions across all irrigation categories.

The model can be used as a reliable decision-support system to help farmers
optimize irrigation practices, reduce water wastage, and prevent crop stress.

---

## 🛠️ Technologies Used
- Python
- Pandas
- Scikit-learn
- Google Colab

---

## Repository Structure

```
├── Smart_Irrigation_Prediction.ipynb
├── README.md
├── cropdata_updated.csv
```




---

## 🚀 How to Run
1. Open the notebook in Google Colab or Jupyter Notebook
2. Upload the dataset (`cropdata_updated.csv`)
3. Run the notebook cells sequentially

---
