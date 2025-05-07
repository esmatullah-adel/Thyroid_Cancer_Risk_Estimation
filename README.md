
# 🧬 Thyroid Cancer Risk Estimation

## 📌 Project Overview
Thyroid cancer is among the most common endocrine cancers. Early risk detection is critical to improve outcomes and guide timely interventions. This project aims to predict the risk level of thyroid cancer—categorized as low, medium, or high—using demographic, lifestyle, and medical features.

By analyzing a comprehensive patient dataset, we aim to:

- Identify the key contributing factors to thyroid cancer risk.
- Build predictive models to estimate risk levels for new individuals.

## 🧠 Problem Statement
Given a set of demographic and medical attributes for an individual,  
predict whether they are at low, medium, or high risk of developing thyroid cancer.

This is a supervised classification problem, where the target variable is `Thyroid_Cancer_Risk`.

## 📊 Dataset Summary
- **Total entries:** 212,691 patients  
- **Total features:** 17 columns (demographic, lifestyle, lab results, and diagnosis)

### 🧾 Key Columns:

| Feature              | Type                | Description                                               |
|----------------------|---------------------|-----------------------------------------------------------|
| Patient_ID           | Integer             | Unique identifier for each patient                        |
| Age                  | Continuous          | Age of the patient                                        |
| Gender               | Categorical         | Male or Female                                            |
| Country, Ethnicity   | Categorical         | Demographic background                                    |
| Family_History       | Categorical         | Thyroid cancer family history (Yes/No)                    |
| Radiation_Exposure   | Categorical         | Prior radiation exposure (Yes/No)                         |
| Iodine_Deficiency    | Categorical         | Iodine deficiency (Yes/No)                                |
| Smoking, Obesity, Diabetes | Categorical   | Lifestyle & medical history factors                       |
| TSH_Level, T3_Level, T4_Level | Continuous | Thyroid hormone levels                                   |
| Nodule_Size          | Continuous          | Size of thyroid nodule (mm/cm)                            |
| Thyroid_Cancer_Risk  | Categorical (target)| Risk level: low, medium, high                             |
| Diagnosis            | Categorical         | Final diagnosis (benign or malignant)                     |

> ℹ️ The column `Diagnosis` was dropped during preprocessing to prevent data leakage, as it directly overlaps with or follows the target variable.

## 🧪 Proposed Solution Methods
We implemented and compared the following supervised machine learning models:

1. **Logistic Regression**  
   A baseline linear model that outputs class probabilities. It’s interpretable and suitable for classification problems with a simple decision boundary.

2. **Random Forest**  
   An ensemble tree-based method that handles non-linearity and feature interactions well. Robust to overfitting and good with both categorical and continuous variables.

## ⚙️ Project Workflow

### Data Cleaning & Preprocessing
- Handled missing values
- Encoded categorical variables (e.g., one-hot encoding)
- Scaled continuous variables using `StandardScaler`

### Exploratory Data Analysis (EDA)
- Visualized class distributions
- Correlation heatmaps
- Feature distributions

### Model Training
- Split data into train/test sets (80/20)
- Trained Logistic Regression and Random Forest models

### Model Evaluation
- Used accuracy, precision, recall, F1-score
- Confusion matrices
