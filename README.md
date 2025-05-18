# Toddler Autism Detection

This project aims to identify early signs of Autism Spectrum Disorder (ASD) in toddlers using behavioral screening data. It includes a complete pipeline from data preprocessing and exploratory analysis to machine learning modeling and interactive dashboard visualization.

---

##  Dataset

- Source: `toddler_autism.csv`
- Features include responses to behavioral questions (A1 to A10), age in months, gender, family history, ethnicity, and more.
- Target: `Class/ASD Traits` (Yes/No indicating ASD risk)

---

##  Techniques Used

- **Data Preprocessing**
  - Null check, label encoding, renaming columns
  - Balancing the dataset with `RandomOverSampler`
  - Feature scaling using `StandardScaler`
- **Exploratory Data Analysis**
  - Count plots, pie charts, pairplots, heatmaps
  - Correlation analysis with behavioral indicators
- **Modeling**
  - Logistic Regression
  - XGBoost Classifier
  - Support Vector Classifier (SVC)
- **Evaluation**
  - Confusion matrix
  - ROC AUC scores
  - Over 97% validation accuracy on models

---

 How to Run:
git clone https://github.com/Indhusrikrishnaraj/toddler-autism-detection.git
cd toddler-autism-detection
pip install -r requirements.txt

##  Run the notebook
jupyter notebook notebook.ipynb

##  OR run the dashboard
python app.py

 Visual Dashboard (Dash):
- Interactive dropdown to select features
- View histograms by ASD diagnosis or gender
- Run locally at: http://127.0.0.1:8050

  Confusion Matrix generated
  ROC AUC > 97% for all models


---

##  Results

| Model                | Training AUC | Validation AUC |
|---------------------|--------------|----------------|
| Logistic Regression | 1.00         | 1.00           |
| XGBoost             | 1.00         | 1.00           |
| SVM (RBF Kernel)    | 1.00         | 0.979          |

---

##  Future Work

- Integrate more clinical or longitudinal features  
- Extend the dashboard with prediction capabilities  
- Deploy the app as a public web service

---

##  Libraries Used

- pandas, numpy — Data manipulation  
- seaborn, matplotlib, plotly — Visualization  
- scikit-learn, xgboost, imbalanced-learn — ML and sampling  
- Dash — Interactive web application

---

##  Preprocessing Highlights

- Categorical columns encoded with LabelEncoder  
- Missing values handled and visualized  
- Features engineered (e.g., `sum_score`, `ind`)  
- Correlation heatmaps and pairplots generated  

---

##  Data Summary

- 1054 entries, 19 columns  
- Balanced after oversampling with `RandomOverSampler`  
- Strong correlation (0.81) between Qchat score and ASD trait  

---

##  Model Performance Notes

- Logistic Regression and XGBoost reached perfect accuracy  
- SVM performed slightly lower on validation set (~97.9%)  
- Feature scaling improved convergence and performance  
- Confusion matrix and ROC AUC used for evaluation  

---

##  Target Column

- `Class/ASD Traits` — binary classification target (0 = No ASD Traits, 1 = Yes ASD Traits)  

---

##  Important Notes

- Works in Jupyter + Dash  
- Designed for local runs; no cloud deployment included (yet)  
- Tested on Python 3.10  

---

##  Inspiration

Created to support early detection of ASD traits in toddlers through interpretable machine learning insights and interactive visualizations for clinicians and parents.

