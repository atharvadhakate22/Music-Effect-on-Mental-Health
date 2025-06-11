# 🎵 Music Recommendation System for Mental Health

## 📄 R Script Description: `cp.ds.R`

This R script builds a machine learning pipeline to **classify the psychological effects of music** (e.g., Improve, No Effect) using survey data.

---

## 🔧 Key Features

- **Data Preprocessing**
  - Loads dataset `ds11.csv`
  - Removes irrelevant columns (`Timestamp`, `column_to_delete`, `Permissions`)
  - Filters out entries labeled as `"Worsen"` in `Music.effects`
  - Converts categorical columns into factors
  - Imputes missing values using `missForest`
  - Balances the dataset using the `ROSE` algorithm

- **Feature Selection**
  - Ranks features using `randomForest`
  - Selects the **top 10** features based on `MeanDecreaseGini`

- **Machine Learning Models**
  - **Random Forest (RF)** — Tuned using `mtry`
  - **Support Vector Machine (SVM)** — Linear kernel
  - **Decision Tree (DT)** — Using `rpart`
  - **Logistic Regression (LR)** — Using `glm`
  - **XGBoost** — Tuned with parameters like `nrounds`, `max_depth`, `eta`
  - **AdaBoost** — Implemented via `boosting` (base learners: `rpart`)

- **Model Evaluation**
  - Splits data: **70% Train / 30% Test**
  - Evaluates with:
    - **Confusion Matrix**
    - **ROC Curves**
    - **AUC Scores**

---

## 🎯 Purpose

To automatically classify how music affects an individual's mental state, enabling personalized music recommendations that promote mental well-being.

---

## 📦 Packages Used

- `randomForest`, `xgboost`, `adabag`, `e1071`, `glm`, `rpart`
- `missForest`, `ROSE`, `caret`, `caTools`
- `ggplot2`, `reshape2`, `FSelector`

---

## 📌 Summary

This script ensures:
- Clean and balanced data
- Smart feature selection
- Diverse model comparison
- Insightful evaluation

It forms the backbone of a mental health–focused music recommendation system using R.

---
