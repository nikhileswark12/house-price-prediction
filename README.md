# House Price Prediction

An end-to-end machine learning regression project that predicts California housing prices using custom implementations of fundamental regression algorithms. The project covers the complete machine learning workflow, from data preprocessing to model evaluation and comparison.

---

## Overview

This project demonstrates how core machine learning regression algorithms work by implementing them manually using **NumPy**, while using **scikit-learn** only for data preprocessing utilities.

The notebook follows a complete workflow:

- Data Exploration
- Data Preprocessing
- Model Implementation
- Model Training
- Model Evaluation
- Model Comparison
- Feature Importance Analysis

---

## Features

- Exploratory Data Analysis (EDA)
- Data preprocessing with Pipeline and ColumnTransformer
- Missing value handling
- Feature encoding and scaling
- Custom Linear Regression
- Custom Decision Tree Regression
- Custom Random Forest Regression
- Custom K-Nearest Neighbors Regression
- Feature Importance Analysis
- Automatic model evaluation and comparison

---

## Technology Stack

| Category | Technologies |
|----------|--------------|
| Language | Python 3.11+ |
| Environment | Jupyter Notebook |
| Data Handling | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Preprocessing | Scikit-learn |
| Models | Custom NumPy Implementations |

---

## Workflow

```text
Dataset
   │
   ▼
EDA
   │
   ▼
Preprocessing
   │
   ▼
Train-Test Split
   │
   ▼
Model Training
   │
   ▼
Model Evaluation
   │
   ▼
Performance Comparison
   │
   ▼
Feature Importance
```

---

## Model Performance

| Model | MAE | RMSE | R² Score |
|------|------:|------:|------:|
| Linear Regression | ~50,670 | ~70,059 | ~0.625 |
| Decision Tree Regression | ~40,319 | ~61,015 | ~0.715 |
| **Random Forest Regression** | **39,686.48** | **55,732.24** | **0.7617** |
| K-Nearest Neighbors Regression | ~40,737 | ~61,351 | ~0.712 |

**Best Model:** Random Forest Regression

---

## Feature Importance

The Random Forest model computes feature importance using cumulative variance reduction across all decision trees.

### Top Features

| Feature | Importance |
|---------|-----------:|
| median_income | 41.9% |
| ocean_proximity_INLAND | 24.3% |
| latitude | 11.7% |
| longitude | 10.9% |

---

## Dataset

- **Source:** California Housing Dataset (Kaggle)
- **Records:** 20,640
- **Target:** `median_house_value`

---

## Project Structure

```text
House_Price_Prediction.ipynb
housing.csv
README.md
requirements.txt
```

---

## Setup

```bash
python -m venv .venv
```

Activate the environment:

**Windows**

```bash
.venv\Scripts\activate
```

**Linux/macOS**

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Run

```bash
jupyter notebook
```

Open `House_Price_Prediction.ipynb` and run all cells.

---

## Key Learnings

- End-to-end machine learning workflow
- Data preprocessing using scikit-learn
- Manual implementation of regression algorithms
- Decision tree construction
- Random Forest ensemble learning
- Feature importance calculation
- Model evaluation using MAE, RMSE, and R²

---

## Future Improvements

- Cross-validation
- Hyperparameter tuning
- Model persistence
- Interactive prediction interface
- Web application deployment