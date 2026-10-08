# Heart Disease Predictor

Predicting the presence of heart disease from clinical measurements using Logistic Regression and Random Forest. This project was built as part of my Machine Learning/AI Engineering portfolio.

## Results
- **Accuracy:** 83.3% (both models) vs. 54% baseline
- **Key Driver:** Thalassemia test result (`thal`), chest pain type (`cp`), and major vessels (`ca`)
- **Recommendation:** Use Logistic Regression for clinical screening — higher recall on the disease class, fewer missed diagnoses

## Key Insights
1. **`thal`** (thalassemia / blood flow) is the strongest predictor at 18.4% importance
2. **`cp`** (chest pain type) and **`ca`** (number of major vessels) are also major factors at 16.7% and 12.3%
3. **`fbs`** (fasting blood sugar) had near-zero importance (0.4%), matching medical literature that it's a weak predictor in this dataset
4. Random Forest achieved the highest cross-validated accuracy (84.4%), but Logistic Regression was preferred for clinical use due to better disease-class recall

## Tech Stack
- Python (Pandas, NumPy, Scikit-learn, Matplotlib)
- Jupyter Notebook
- Git & GitHub

## How to Run
1. Clone this repo
2. Run `heart-disease.ipynb` in Jupyter
3. View the results and visualizations

## Next Steps
- Collect more data — 297 rows is small for clinical use
- Try gradient boosting (XGBoost, LightGBM)
- Add SHAP analysis for deeper interpretability
- Validate on an external dataset to test generalization