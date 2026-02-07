# Smart Irrigation Prediction using Machine Learning

## 📌 Project Overview
This project aims to predict whether irrigation is required for a crop based on
soil type, crop growth stage, and environmental conditions such as moisture index,
temperature, and humidity.

The model acts as a decision-support system for farmers, helping them optimize
water usage, reduce wastage, and prevent crop stress.

---

##  Problem Statement
To build a machine learning model that predicts whether irrigation is required
(`Yes` or `No`) using crop, soil, and environmental data.  
The problem is formulated as a **binary classification task**.

---

##  Dataset Description
The dataset contains **16,411 records**, where each row represents a crop sample
under specific environmental conditions.

### Features:
- **crop_ID**: Unique identifier for the crop (categorical)
- **soil_type**: Type of soil (categorical)
- **Seedling_Stage**: Crop growth stage (categorical)
- **MOI (Moisture Index)**: Soil moisture level (numerical)
- **temp**: Ambient temperature in °C (numerical)
- **humidity**: Relative humidity in % (numerical)

### Target:
- **result**
  - `1` → Irrigation required
  - `0` → Irrigation not required

---

##  Data Preprocessing
The following preprocessing steps were applied:
- Dataset inspection using `info()` and `isnull()`
- No missing values were found, so no imputation was required
- Column names were standardized for cleaner code
- Categorical features were encoded using **Label Encoding**
- Numerical features were scaled using **StandardScaler**
- Data was split into training and testing sets (80/20)

---

##  Models Used

### 1️ Logistic Regression (Baseline Model)
- Used for its simplicity and interpretability
- Serves as a baseline for comparison

### 2️ Random Forest Classifier (Improved Model)
- Captures non-linear relationships
- Provides better accuracy and robustness
- Allows feature importance analysis

---

##  Evaluation Metrics
The models were evaluated using:
- Accuracy
- Precision
- Recall
- F1-score

Random Forest outperformed Logistic Regression and was selected as the final model.

---

##  Feature Importance
Feature importance analysis from the Random Forest model showed that:
- **Moisture Index (MOI)**
- **Temperature**

are the most influential factors in predicting irrigation requirements, which
aligns well with real-world agricultural understanding.

---

## Final Inference
Among the models tested, the Random Forest Classifier provided better prediction
performance compared to Logistic Regression. The model effectively identifies
irrigation requirements based on soil moisture, temperature, humidity, and crop
growth stage.

This system can assist farmers in making timely irrigation decisions, optimizing
water usage, and reducing crop stress.

---

## Technologies Used
- Python
- Pandas
- Scikit-learn
- Google Colab

---

## Repository Structure

├── Smart_Irrigation_Prediction.ipynb
├── README.md
├── cropdata_updated.csv

---

## How to Run
1. Open the notebook in Google Colab or Jupyter Notebook
2. Upload the dataset (`cropdata_updated.csv`)
3. Run the notebook cells sequentially

---

## Author
**Amruha Panangipalli**  
Machine Learning / Data Science Enthusiast
