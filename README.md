#  Student Stress Prediction System

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Scikit-Learn](https://img.shields.io/badge/ML-ScikitLearn-orange)
![Model](https://img.shields.io/badge/Model-RandomForest-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

Machine Learning models for predicting **student stress levels** and **menstrual-cycle related stress patterns** to support a **mental health monitoring system**.

---

# 📊Models

| Model | Algorithm | Dataset Size | Features | Performance |
|------|------|------|------|------|
| Stress Level Predictor | Random Forest Classifier | 1100 | 15 | **88.18% Accuracy** |
| Period Stress Predictor | Random Forest Regressor | 897 | 2 | **R² = 0.832** |

---

#  Project Structure

```
.
├── period_model.ipynb
├── stress_model.ipynb
├── classifier.joblib
├── periods.xlsx
├── StressLevelDataset.csv
└── README.md
```

---

#  Model 1 — Stress Level Predictor

**Target Variable**

```
stress_level
```

| Value | Meaning |
|------|------|
| 0 | No Stress |
| 1 | Mild |
| 2 | Moderate |
| 3 | High |

### Best Hyperparameters

```python
{
'n_estimators': 50,
'max_depth': None,
'min_samples_leaf': 2,
'min_samples_split': 2
}
```

### Performance

| Metric | Score |
|------|------|
Accuracy | **88.18%** |
Cross Validation | **~88%** |

---

#  Model 2 — Menstrual Cycle Stress Predictor

**Features**

| Feature | Description |
|------|------|
period_flow | Flow intensity |
expected_vs_actual_date_difference | Cycle deviation |

### Model

```
RandomForestRegressor
n_estimators = 100
random_state = 42
```

### Performance

| Metric | Score |
|------|------|
Mean Squared Error | **0.274** |
R² Score | **0.832** |
Accuracy (±0.5) | **65.56%** |

---

# ⚙️ Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Joblib

---

#  System Architecture

```
User Data
   │
   ▼
Data Preprocessing
   │
   ▼
Feature Engineering
   │
   ▼
Random Forest Models
   │
   ├── Stress Level Predictor
   └── Period Stress Predictor
   │
   ▼
Predictions
   │
   ▼
Mental Health Dashboard
```

---

#  Usage

### Load Model

```python
import joblib

model = joblib.load("classifier.joblib")
```

### Predict

```python
prediction = model.predict(input_data)
```

---

#  Use Case

This system enables:

- Stress level prediction  
- Menstrual-cycle stress analysis  
- Early mental health monitoring  
-  Stress trend visualization  

---

# 👩‍💻 Author

Developed for **Student Mental Health Monitoring System**
