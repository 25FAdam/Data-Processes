# COVID-19 Prediction Using Machine Learning

(Data Processes course - Project) 

## 📌 Project Overview

This project focuses on developing a machine learning model to predict COVID-19 positivity using synthetic patient data from two hospitals. The goal is to support early detection and optimize hospital resource allocation. The project was completed as part of the Data Processes course at Universidad Politécnica de Madrid (UPM).

## 📁 Project Structure
```
.
├── DataProcess_notebook.ipynb    # Full Python notebook with code and analysis
├── Data/                         # Folder containing CSV files
│   ├── hospital1.csv             # Synthetic patient data from hospital one
│   └── hospital2.csv             # Synthetic patient data from hospital two
└── README.md                     # Project description and instructions
└── DataProcess_presentation.pdf  # Project presentation
```

## Business & Data Mining Goals

- Business Goal:
  Enhance early detection of COVID-19 to support resource management and reduce operational costs.
  **KPI:** Cost savings from improved triage and resource allocation.
- Data Mining Goal:
  Develop a predictive model to accurately classify patients based on symptoms and comorbidities.
  **KPI:** Achieve at least 85% accuracy and an AUC above 0.72 for model evaluation.

## Dataset Description
Two synthetic datasets simulate patient records from separate hospitals:
- **Size:** 14,712 records (Hospital 1), 12,736 records (Hospital 2)
- **Features:** Age, sex, temperature, oxygen saturation, symptoms, comorbidities, and PCR test results
- **Preprocessing:** Included imputation, encoding, merging, standardization, and cyclical encoding of dates

## Key Steps

1. Exploratory Data Analysis (EDA):
   Analyzed patterns in symptoms, correlations, and trends across age groups and time periods.
2. Preprocessing Techniques:
   - One-hot encoding for categorical variables
   - Imputation using median/mode
   - Dropped incomplete or non-informative features
   - Feature engineering from date fields
3. Modeling & Tools:
   - Algorithms: Random Forest, Decision Tree
   - Balancing: SMOTE for class imbalance
   - Evaluation: Accuracy, Precision, Recall, F1-score, AUC
   - Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn
  
## ✅ Results
Best Model Performance (before SMOTE):
- Accuracy: 90%
- Precision (Positive cases): 92%
- Recall (Positive cases): 96%
- AUC: 0.74

Best Model Performance (after SMOTE):
- Accuracy: 88%
- Precision (Positive cases): 93%
- Recall (Positive cases): 93%
- AUC: 0.78

SMOTE: Synthetic Minority Oversampling Technique

**Top 5 Predictive Features:**
Age, Fever Temperature, Oxygen Saturation, Fatigue, History of Fever


## Business KPI Optimization

By accurately identifying COVID-19 cases, hospitals can:
- Prioritize high-risk patients
- Reduce unnecessary admissions
- Minimize test kit wastage
- **Business KPI Impact:** Improved early diagnosis directly reduces resource strain and overall operational costs.

## 📦 Requirements
This project uses:
- Python 3.11.9
- Pandas 2.2.3
- NumPy 1.26.4
- Matplotlib 3.9.2
- Seaborn 0.13.2
- Scikit-learn 1.5.3
- Jupyter Notebook
