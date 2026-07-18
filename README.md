# 📉 Telecom Customer Churn Predictor using SMOTE

An educational, end-to-end machine learning application that walks through the
full churn-prediction pipeline — from raw data to a live, interactive prediction
tool — built with **Streamlit**.

It's designed to teach the *why* behind each step, not just the *how*: why
accuracy is misleading on imbalanced data, why SMOTE helps, why the default
0.5 decision threshold is rarely optimal, and how feature engineering adds
real predictive value.

## What This App Does

The app trains and compares three classifiers (Logistic Regression, Random
Forest, Gradient Boosting) to predict whether a telecom customer will churn,
then lets you explore:

1. **Data Overview** — churn rate, distributions, churn by contract type
2. **Feature Engineering** — engineered signals like `NumServices`,
   `AvgMonthlyCharge`, `ChargeRatio`, and their importance
3. **Imbalanced Data** — the "accuracy trap" and how SMOTE fixes it
4. **Threshold Tuning** — an interactive precision/recall trade-off explorer
5. **Predict Churn** — a live form that scores a hypothetical customer

## Tech Stack

| Category | Libraries |
|---|---|
| UI | `streamlit` |
| Data | `pandas`, `numpy` |
| ML | `scikit-learn`, `imbalanced-learn` (SMOTE) |
| Visualization | `matplotlib`, `seaborn` |
| Dataset access | `kagglehub` (optional) |

## App Walkthrough

| Tab | What you'll see |
|---|---|
| 📊 **Data Overview** | Churn rate, class distribution chart, churn rate by contract type |
| 🔧 **Feature Engineering** | Explanation + table of engineered features, Random Forest feature importance |
| ⚖️ **Imbalanced Data** | The "always predict No Churn" accuracy trap, before/after SMOTE comparison |
| 🎯 **Threshold Tuning** | Interactive slider — watch precision/recall/F1 shift live, precision-recall curve, confusion matrix |
| 🔮 **Predict Churn** | Fill out a form describing a customer → get a churn probability and recommendation |

Yes, via [Option B](#option-b--provide-your-own-csv) — just make sure the
column names match what `engineer_features()` and `preprocess()` expect
(see `app.py`), or adjust those functions accordingly.
