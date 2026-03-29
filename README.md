# 💓 Byte to Beat: AI-Powered Cardiac Risk Detection

**Byte to Beat** is a machine learning framework which integrates multi-source clinical data to provide early detection of cardiovascular disease with high accuracy and explainability.

---

## 🚀 Key Achievements

- **Ensemble Accuracy:** Achieved a stable **87.5% accuracy** using a Voting Classifier (XGBoost + Random Forest).
- **Big Data Integration:** Scaled from a 300-row clinical dataset to a **70,000-row Master Dataset**.
- **Clinical Rigor:** Performed medical-grade data cleaning, filtering extreme blood pressure outliers (e.g., −150 to 16,000 mmHg).
- **Explainable AI (XAI):** Implemented **SHAP** to visualize biological risk factors such as ST Slope and Angina.

---

## 🛠️ Technical Pipeline used 

### 1️⃣ Data Cleaning & Integration

- **Outlier Mitigation:** Identified and removed physiologically impossible blood pressure values.
- **Standardization:** Converted age from days to years and applied median imputation for missing clinical values.
- **Feature Alignment:** Merged demographics (`cardio_base.csv`) and clinical markers (`cardiac_failure_processed.csv`) into a unified **70k-row cohort**.

---

### 2️⃣ Feature Engineering

- **BMI (Body Mass Index):** Computed from height and weight to provide a stable medical predictor.
- **Heart Stress Index:** Engineered a composite metric combining:
  - Age  
  - Max Heart Rate  
  - Resting Blood Pressure  
  to capture non-linear cardiovascular risk patterns.

---

### 3️⃣ Model Development & Explainability

- **Optimization:** Used **Optuna** for hyperparameter tuning of the Random Forest baseline.
- **Ensemble Strategy:** Built a **Voting Classifier** combining:
  - XGBoost (high precision)
  - Random Forest (model stability)
- **Error Analysis:** Performed false-negative audits and found strong model dependence on **ST-depression markers**.

---

## 📊 Model Evaluation

| Metric | Result |
|--------|---------|
| Final Accuracy | **87.5%** |
| Precision (Positive Class) | **0.90** |
| Primary Predictors | ST_Slope_Up, ap_hi (Systolic BP), Cholesterol |

---

## 📁 Repository Structure

- **byte_to_beat.ipynb** — Full research notebook containing the end-to-end pipeline  
- **data/** — Contains raw and processed datasets *(subject to original licensing)*  
- **reports/** — Final 2–3 page PDF submission for the Hack4Health challenge



