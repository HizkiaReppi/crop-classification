# Crop Clasification - Final Project Data Science

## Overview
The goal of the "Crop Classification" project is to develop a predictive model that can classify different types of crops based on soil conditions, including rainfall, temperature, and pH. Additionally, the model aims to predict the production level of the identified crops.

## Business Understanding

1. **Problem Statement:**
   The agriculture industry faces challenges in optimizing crop production due to varying soil conditions. Farmers need a tool that can analyze soil parameters and provide insights into the types of crops suitable for cultivation in a particular region. Moreover, predicting the expected production level can aid in better planning and resource allocation.

2. **Objectives:**
   - Develop a machine learning model for crop classification based on soil conditions.
   - Integrate features such as rainfall, temperature, and pH to enhance classification accuracy.
   - Implement a production prediction model to estimate the potential yield of identified crops.

3. **Benefits:**
   - **Precision in Crop Selection:** Farmers can make informed decisions on which crops to cultivate based on the soil conditions, leading to better yield and resource utilization.
   - **Optimized Resource Allocation:** Efficient use of resources such as water, fertilizers, and pesticides based on predicted production levels.
   - **Risk Mitigation:** Early identification of crops suitable for specific soil conditions helps mitigate the risk of crop failure.

4. **Stakeholders:**
   - **Farmers:** Will benefit from optimized crop selection and resource management.
   - **Agricultural Experts:** Can use the model's insights to provide recommendations to farmers.
   - **AgTech Companies:** May integrate the model into precision agriculture tools.

5. **Key Performance Indicators (KPIs):**
   - **Classification Accuracy:** Measure how accurately the model predicts the crop types.
   - **Production Prediction Accuracy:** Evaluate the precision of the model in estimating crop production levels.

5. **Expected Outcome:**
   - A robust crop classification model capable of predicting suitable crops based on soil conditions.
   - A production prediction model providing estimates of potential crop yield.

## Data Understanding

This dataset consists of 189,232 entries with 5 columns covering information about soil conditions (Rainfall, Soil Temperature, pH level), crop types (Crop), and crop production yields (Production). Some general statistics indicate significant variation in soil conditions and crop production.

### Data Statistics

- **Rainfall:**
  - Mean: 693.42 mm
  - Standard Deviation: 288.99 mm
  - Minimum Value: 100.00 mm
  - Maximum Value: 3000.00 mm

- **Soil Temperature:**
  - Mean: 25.26 °C
  - Standard Deviation: 4.59 °C
  - Minimum Value: 7.00 °C
  - Maximum Value: 39.05 °C

- **Soil pH Level:**
  - Mean: 6.34
  - Standard Deviation: 0.79
  - Minimum Value: 3.00
  - Maximum Value: 8.80

- **Crop Production (Yield):**
  - Mean: 5.26
  - Standard Deviation: 14.44
  - Minimum Value: 0.00
  - Maximum Value: 955.75

### Crop Types

The dataset covers various crop types, totaling 63 different types. Some examples of crop types include 'Bajra', 'Banana', 'Rice', 'Sugarcane', and others.

## Data Preparation

### Data Types
- **Numeric Features:**
  - Rainfall, Temperature, pH, and Production are represented as float64.
  
- **Categorical Feature:**
  - Crop has been label-encoded, converting categorical data into numeric form for model compatibility.

### Encoding Categorical Data
Label encoding has been applied to the 'Crop' column, ensuring the conversion of categorical data into a format suitable for machine learning models.

### Outlier Handling
Outliers have been addressed using the Isolation Forest algorithm, a robust method for identifying anomalies in the dataset. This helps maintain the integrity of the data and prevents outliers from adversely affecting model performance.

### Feature Scaling
Numeric features have been standardized using StandardScaler, ensuring that all features contribute equally to model training, especially for algorithms sensitive to feature scales.

### Splitting the Dataset
The dataset has been split into training and testing sets using the train_test_split function, enabling the evaluation of model performance on unseen data.

## Modeling and Evaluation
- Modeling using KNN (K-Nearest Neighbors)
- The K-Nearest Neighbors (KNN) model used for classifying plant types based on soil conditions has achieved an accuracy of 99.65%. This indicates the model's ability to accurately identify plant types based on the given soil parameters.
- The precision level of the model reaches 99.65%, indicating that, among all positive predictions made by the model, the majority are indeed relevant.
- A recall rate of 99.65% indicates the model's ability to identify most of the actual positive instances.
- The high F1-score of 99.64% reflects a good balance between precision and recall.
- The Mean Absolute Error (MAE) value of 0.0245 indicates that the average prediction error is relatively small, and the model can provide fairly accurate predictions.
- The Mean Squared Error (MSE) value of 0.2262 indicates a low variance in prediction errors, and the model tends to provide consistent predictions.
- An R-squared (R²) value of 0.9965 indicates that the model can explain most of the variation in the data, suggesting a very good fit between the observed and predicted data.

##### Copyright 2023 - Hizkia Reppi
