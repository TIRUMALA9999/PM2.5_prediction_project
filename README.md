# PM2.5 / AQI Prediction Project — End-to-End ML (Classification + Regression)

![Python](https://img.shields.io/badge/Python-Data%20Science-blue)
![ML](https://img.shields.io/badge/ML-Scikit--learn%20%7C%20XGBoost-orange)
![AirQuality](https://img.shields.io/badge/Domain-Air%20Quality%20%28PM2.5%20%2F%20AQI%29-green)

**Target audience:** Recruiters / Hiring Managers  
**Style:** Resume-focused • Interview-ready • Explainable (portfolio)

This repository contains a complete course project for **predicting air quality** using **PM2.5 pollutant measurements and weather features**. It includes:
- **AQI Level Classification** (EPA categories) from PM2.5 + meteorological features
- **PM2.5 Regression** to predict numeric concentration values
- A full set of deliverables (executive summary, report, architecture doc, slides) and reproducible notebooks

---

## Key highlights (30-second recruiter summary)

- Built an end-to-end ML workflow to predict **daily air quality levels** using **PM2.5 + weather data**.
- Engineered features including **lagged pollutant variables** to model temporal effects.
- Trained and compared multiple models:
  - **Classification:** Decision Tree, Random Forest, KNN, SVM, Logistic Regression, **XGBoost**, **MLP**
  - **Regression:** Linear Regression, Random Forest Regressor (+ k-fold CV)
- Achieved **~97.8% best classification accuracy** (MLP), with **~96.61%** as the next-best baseline (Logistic Regression) on the same task.
- Delivered a professional project package: **executive summary + full report + architecture + presentation**.

**ATS keywords:** Air Quality, PM2.5, AQI, Supervised Learning, Feature Engineering, Time-lag Features, Classification, Regression, Random Forest, XGBoost, Neural Networks (MLP), Model Evaluation, Cross-Validation, Pandas, Scikit-learn.

---

## Problem statement

Air pollution—especially **PM2.5**—is a major health risk. This project predicts air quality using a combination of:
- **Daily PM2.5 concentration**
- **Weather variables** (temperature, humidity, wind, etc.)
- **Lagged pollutant features** to capture delayed effects

The output is either:
1) **AQI category** (public-friendly classification), or  
2) **PM2.5 concentration** (numeric regression).

---

## Repository contents (what’s included)

```
PM2.5_prediction_project-main/
├─ Predicting_AQI_Levels.ipynb        # Multi-class AQI classification (RF/KNN/XGBoost + comparisons)
├─ pm2.5prediction.ipynb              # PM2.5 regression (Linear Regression + RF + CV metrics)
│
├─ merged2018-19.xlsx                 # Merged dataset (PM2.5 + weather)
├─ air_quality_datasets (3).zip       # Raw/aux datasets (source package)
│
├─ pm2.5-sources-air-quality.jpg      # Domain context graphic
├─ pm25_by_month_boxplot.png          # Exploratory plot artifact
│
├─ 5340 executive summary.docx        # High-level summary + key results
├─ 5340 project report.docx           # Full report (methods, evaluation, conclusions)
├─ 5340 project.docx                  # Project writeup
└─ ADTA 5340 project presentation.pptx# Slide deck presentation
```

---

## Approach (interview-explainable)

### 1) Data preparation
- Combine PM2.5 and weather data into one daily dataset (`merged2018-19.xlsx`)
- Handle missing values and clean feature columns
- Convert PM2.5 into **EPA AQI categories** for classification

### 2) Feature engineering
- Add **lagged PM2.5 features** (previous day(s)) to capture temporal dependence
- Standardize/scale features for models sensitive to feature scale (e.g., Logistic Regression, SVM, MLP)

### 3) Modeling
**Classification (AQI levels):**
- Decision Tree, Random Forest, KNN, SVM, Logistic Regression, XGBoost, MLP

**Regression (PM2.5 prediction):**
- Linear Regression, Random Forest Regressor
- k-fold cross-validation, RMSE/MAE/MSE

### 4) Evaluation
- **Classification:** Accuracy, confusion matrix, classification report
- **Regression:** RMSE, MAE, MSE + cross-validation averages

---

## Results (from project deliverables)

- **Best AQI classification accuracy:** **~97.8%** (MLP)  
- **Strong baseline:** **~96.61%** (Logistic Regression)  

See:
- `5340 executive summary.docx` for the condensed results
- `5340 project report.docx` for full discussion and conclusions

---

## How to run locally

### Option A) Run notebooks
```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

pip install pandas numpy scikit-learn matplotlib seaborn xgboost openpyxl jupyterlab
jupyter lab
```

Open:
- `Predicting_AQI_Levels.ipynb`
- `pm2.5prediction.ipynb`

### Option B) Quick data check (Excel)
- `merged2018-19.xlsx` contains the merged dataset used in experiments.

---

## Interview talking points (copy/paste)

- “I converted continuous PM2.5 into **EPA AQI categories** so results are explainable for the public and actionable.”
- “Lagged PM2.5 features capture temporal effects—yesterday’s pollution impacts today’s AQI.”
- “I benchmarked multiple models and selected the best based on validation metrics and interpretability.”
- “I used both **classification** and **regression** framing to cover real-world needs: alerts (categories) and forecasting (values).”
- “This pipeline is transferable to other time-dependent forecasting tasks (energy, demand, traffic, sensors).”

---

## Resume bullet points (copy/paste)

- Built an end-to-end ML pipeline to predict **air quality (PM2.5/AQI)** using pollutant and weather features, including **time-lag feature engineering** to model temporal effects.  
- Trained and benchmarked multi-class classifiers (Random Forest, SVM, KNN, Logistic Regression, **XGBoost**, **MLP**) to predict **EPA AQI categories**, achieving **~97.8% best accuracy**.  
- Developed PM2.5 regression models (Linear Regression, Random Forest Regressor) and evaluated performance using **RMSE/MAE/MSE** with **k-fold cross-validation**.  
- Produced a complete project package (executive summary, technical report, architecture doc, and presentation) communicating methods, evaluation, and actionable insights.

---

## Author

**Tirumala Teja Yegineni**  
GitHub: https://github.com/TIRUMALA9999
