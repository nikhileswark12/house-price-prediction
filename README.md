# House Price Prediction

An end-to-end Machine Learning regression project that predicts California housing prices using custom implementations of fundamental regression algorithms. This project demonstrates the complete machine learning workflow, from data exploration and preprocessing to model training, evaluation, hyperparameter tuning, and feature importance analysis.

Unlike conventional machine learning projects that rely entirely on pre-built libraries, the core regression algorithms are implemented manually using **NumPy**, while **scikit-learn** is used only for preprocessing utilities and evaluation metrics.

---

# Project Overview

This project aims to provide a practical understanding of regression algorithms by building them from the ground up and comparing their performance on a real-world housing dataset.

The notebook walks through every stage of a typical machine learning project, including:

- Exploratory Data Analysis (EDA)
- Data Preprocessing
- Custom Model Implementation
- Model Training
- Hyperparameter Tuning
- Model Evaluation
- Feature Importance Analysis
- Model Comparison

---

# Features

- Exploratory Data Analysis (EDA)
- Data preprocessing using Pipeline and ColumnTransformer
- Missing value handling
- Feature encoding and scaling
- Custom Linear Regression
- Custom Decision Tree Regression
- Custom Random Forest Regression
- Custom K-Nearest Neighbors Regression
- Custom Hyperparameter Tuning Framework
- Custom Random Forest Feature Importance
- Centralized Evaluation Pipeline
- Automatic Model Comparison
- Automatic Best Model Selection

---

# Technology Stack

| Category | Technologies |
|----------|--------------|
| Programming Language | Python 3.11+ |
| Development Environment | Jupyter Notebook |
| Data Processing | Pandas, NumPy |
| Data Visualization | Matplotlib, Seaborn |
| Preprocessing | Scikit-learn (Pipeline, ColumnTransformer, StandardScaler, OneHotEncoder, SimpleImputer) |
| Model Implementation | Custom NumPy Implementations |

---

# Workflow

```text
California Housing Dataset
            │
            ▼
 Exploratory Data Analysis
            │
            ▼
 Data Preprocessing
            │
            ▼
 Train-Test Split
            │
            ▼
 Model Implementation
 ├── Linear Regression
 ├── Decision Tree Regression
 ├── Random Forest Regression
 └── K-Nearest Neighbors Regression
            │
            ▼
 Hyperparameter Tuning
            │
            ▼
 Model Evaluation
            │
            ▼
 Feature Importance Analysis
            │
            ▼
 Best Model Selection
```

---

# Models Implemented

| Model | Description |
|--------|-------------|
| Linear Regression | Custom implementation using the Normal Equation |
| Decision Tree Regression | Custom recursive regression tree using variance reduction |
| Random Forest Regression | Custom ensemble of decision trees using bootstrap sampling and random feature selection |
| K-Nearest Neighbors Regression | Custom distance-based regression using Euclidean distance |

---

# Hyperparameter Tuning

A custom hyperparameter tuning framework was developed without using **GridSearchCV** or **RandomizedSearchCV**. Every parameter combination is evaluated using the project's centralized evaluation pipeline, and the best configuration is automatically selected based on the highest **R² Score**.

### Best Parameters

| Model | Best Parameters |
|--------|-----------------|
| Decision Tree Regression | `max_depth = 10`, `min_samples_split = 10` |
| Random Forest Regression | `n_estimators = 50`, `max_depth = 15`, `min_samples_split = 5`, `max_features = "sqrt"` |
| K-Nearest Neighbors Regression | `n_neighbors = 11` |

---

# Model Performance

| Model | MAE | RMSE | R² Score |
|------|------:|------:|------:|
| Linear Regression | ~50,670 | ~70,059 | ~0.625 |
| Decision Tree Regression | ~40,319 | ~61,015 | ~0.720 |
| **Random Forest Regression** | **39,686.48** | **55,732.24** | **0.7617** |
| K-Nearest Neighbors Regression | ~40,737 | ~61,351 | ~0.720 |

**Best Performing Model:** Random Forest Regression

---

# Feature Importance

The custom Random Forest implementation computes feature importance using cumulative variance reduction across all decision trees. The importance values are normalized to provide an interpretable measure of each feature's contribution to the final predictions.

### Most Important Features

| Rank | Feature | Importance |
|-----:|----------|-----------:|
| 1 | `median_income` | 41.9% |
| 2 | `ocean_proximity_INLAND` | 24.3% |
| 3 | `latitude` | 11.7% |
| 4 | `longitude` | 10.9% |

---

# Dataset

**Dataset:** California Housing Prices

**Source:** Kaggle

**Number of Records:** 20,640

**Target Variable**

- `median_house_value`

**Features**

- longitude
- latitude
- housing_median_age
- total_rooms
- total_bedrooms
- population
- households
- median_income
- ocean_proximity

---

# Repository Structure

```text
House_Price_Prediction.ipynb
housing.csv
README.md
requirements.txt
```

---

# Getting Started

## Clone the Repository

```bash
git clone <repository-url>
cd house-price-prediction
```

## Create a Virtual Environment

```bash
python -m venv .venv
```

### Windows

```bash
.venv\Scripts\activate
```

### Linux / macOS

```bash
source .venv/bin/activate
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
House_Price_Prediction.ipynb
```

Run all notebook cells from top to bottom.

The notebook will automatically:

- Load the dataset
- Perform preprocessing
- Train all custom regression models
- Tune model hyperparameters
- Evaluate each model
- Compare model performance
- Generate feature importance
- Select the best-performing model

---

# Key Learnings

This project demonstrates:

- End-to-end Machine Learning workflow
- Data preprocessing using Scikit-learn Pipelines
- Manual implementation of regression algorithms
- Recursive Decision Tree construction
- Bootstrap Aggregating (Bagging)
- Random feature selection in Random Forests
- Euclidean distance-based KNN regression
- Hyperparameter tuning without GridSearchCV
- Feature importance using variance reduction
- Model evaluation using MAE, RMSE, and R² Score

---

# Future Improvements

- K-Fold Cross-Validation
- Model Persistence using Joblib
- Interactive Prediction Interface
- Web Application Deployment