# PRCP-1016: Heart Disease Prediction & Clinical Risk Modeling

Binary classification pipeline predicting heart disease presence from patient clinical and stress-test measurements (`values.csv` and `labels.csv`).

## Key Results
* **Dataset:** 180 patient records (144 train / 36 held-out test)
* **Best Model:** L2-Regularized Logistic Regression (`C=0.05`) with leakage-safe preprocessing (`RobustScaler` + `OneHotEncoder`)
* **Performance:** `0.8913` CV ROC-AUC | `0.9656` Test ROC-AUC
* **Clinical Threshold:** Optimized to `0.32` via F2-score, achieving **`1.00` recall** (`16/16` heart disease cases caught, 0 missed)
* **Explainability:** Validated key risk drivers (`num_major_vessels`, `thal_reversible_defect`, `chest_pain_type_4`) using Log-Odds coefficients, Odds Ratios, and SHAP beeswarm plots

## Repository Files
* `PRCP-1016-HeartDiseasesPred.ipynb` — Full EDA, modeling, threshold tuning, SHAP explainability, and `joblib` export
* `values.csv` & `labels.csv` — Raw feature and target datasets
