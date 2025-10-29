# Obesity Weight Category Prediction

Predict obesity level (`WeightCategory`) from health and lifestyle data.

**Best Kaggle Public Score**: `0.92037+`  
**Local CV Accuracy**: `0.91377`  
**Runtime**: 15-25 minutes (Google Colab Free Tier)  
**Model**: Ensemble (XGBoost)

---

## Dataset

| File | Rows | Description |
|------|------|-----------|
| `train.csv` | ~15,532 | Training data with labels |
| `test.csv` | ~7,766 | Test data (predict `WeightCategory`) |
| `ObesityDataSet.csv` | 2,111 | Extra data for augmentation |

---

## Features Used (21 total)

### Numerical (10)
- `Age`, `Height`, `Weight`  
- `FCVC`, `CH2O`  
- `BMI`, `BMI_squared`  
- `Diet_Quality`, `Age_log`, `Weight_Height_Ratio`

### Categorical (4 → 10 one-hot)
- `Gender`, `family_history_with_overweight`, `CALC`, `Age_Group`

### Ordinal (1)
- `CAEC`

> Dropped: `FAF`, `TUE`, `NCP`, `FAVC`, `SMOKE`, `SCC`, `MTRANS`, `Sedentary_Score`, `Physical_Activity_Index`

---

## How to Run (Google Colab)

### 1. Upload Files
Go to google collab
Upload these files to `/content/`:
- `train.csv`
- `test.csv`
- `ObesityDataSet.csv`

###expected output
Number of features after preprocessing: 21
Best Params: {'classifier__xgb__n_estimators': 250, ...}
Tuned CV Accuracy: 0.91899
Improved submission file created: /content/submission_improved.csv



obesity-prediction/
├── train.csv
├── test.csv
├── ObesityDataSet.csv
├── submission_improved.csv     ← Your Kaggle submission
├── optimized_ensemble_obesity_prediction.py
└── README.md                   ← This file

