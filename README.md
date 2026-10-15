# Employee_Attrition_Prediction_Models
# Employee Attrition Prediction with Feature Engineering and Threshold Tuning

Machine learning project that predicts employee attrition on the IBM HR Analytics Employee Attrition dataset (1,470 employees, about 16% attrition), with engineered features and decision-threshold tuning.

## Repository contents
| File | Description |
|---|---|
| `Attrition_Model_Notebook.ipynb` | Full model notebook (EDA, feature engineering, modelling, tuning, importance) |
| `Evaluation_Report.docx` | Model evaluation and comparison report |
| `Business_Interpretation_Report.docx` | Findings and recommendations for HR |

## Approach
- **Classification target:** Attrition (Yes/No)
- **Algorithms:** Logistic Regression, Decision Tree, Random Forest, XGBoost
- **Data split:** 75/25 stratified train-test split
- **Feature engineering:** IncomeToLevel, TenureRatio, PromotionGap, StabilityScore, SatisfactionIndex
- **Metrics:** Accuracy, Precision, Recall, F1, ROC-AUC
- **Improvement:** 10-fold stratified cross-validation, RandomizedSearchCV tuning, decision-threshold tuning, permutation importance
- **Optional regression task:** predicting PerformanceRating, with a data-leakage check

## Key findings
- XGBoost gave the best ROC-AUC after tuning (about 0.86).
- Threshold tuning raised F1 from 0.52 to 0.58 and precision from 0.45 to 0.57, with a small drop in recall.
- Overtime, the satisfaction index, stock options and income are the strongest drivers.
- PerformanceRating is fully determined by PercentSalaryHike in this dataset. Without that column it cannot be predicted from the other fields.

## How to run (Google Colab)
1. Upload `Attrition_Model_Notebook.ipynb` to Google Colab.
2. Click Runtime > Run all.
3. The dataset downloads automatically; if it fails, you will be asked to upload the CSV.

## Dataset
IBM HR Analytics Employee Attrition: https://github.com/IBM/employee-attrition-aif360
