# House Price Prediction

### A Machine Learning Regression Project with Custom Model Implementations

House Price Prediction is an end-to-end machine learning regression project that predicts the median house value of California districts using demographic, geographic, and housing-related features. The project demonstrates the complete machine learning workflow, including exploratory data analysis, data preprocessing, custom model implementation, evaluation, and comparison.

Unlike a typical machine learning notebook that relies entirely on library implementations, this project implements the core regression algorithms manually using **NumPy** while leveraging **scikit-learn** only for preprocessing utilities and evaluation metrics. The result is an educational, transparent, and reproducible machine learning project that explains not only *how* to use these algorithms but also *how they work internally*.

---

## Vision

To build a clear, reproducible, and educational machine learning project that demonstrates the complete regression pipeline while providing custom implementations of fundamental regression algorithms.

---

## Problem Statement

Accurately estimating housing prices is a challenging task because they are influenced by multiple geographic, demographic, and socioeconomic factors. Traditional estimation methods often fail to capture these complex relationships.

Some of the major challenges include:

- Handling missing values in real-world datasets.
- Encoding categorical variables for machine learning models.
- Capturing non-linear relationships between housing features and prices.
- Fairly comparing multiple regression algorithms.
- Understanding the internal working of machine learning algorithms instead of treating them as black boxes.

This project addresses these challenges through structured preprocessing, custom algorithm implementations, and standardized evaluation techniques.

---

## Key Features

- Exploratory Data Analysis (EDA)
- Data preprocessing using **Pipeline** and **ColumnTransformer**
- Missing value handling
- One-Hot Encoding for categorical features
- Standardization of numerical features
- Custom implementation of Linear Regression
- Custom implementation of Decision Tree Regression
- Custom implementation of Random Forest Regression
- Custom implementation of K-Nearest Neighbors Regression
- Centralized evaluation framework
- Automatic model comparison
- Automatic best model selection using R² Score

---

## Technology Stack

| Category | Technologies |
|----------|--------------|
| Language | Python 3.11+ |
| Environment | Jupyter Notebook |
| Data Handling | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Preprocessing | Scikit-learn Pipeline, ColumnTransformer |
| Model Implementation | Custom NumPy Implementations |

---

## System Architecture

```text
                    Housing Dataset
                           │
                           ▼
            Exploratory Data Analysis (EDA)
                           │
                           ▼
                 Data Preprocessing Pipeline
                           │
                           ▼
                  Train-Test Split (80/20)
                           │
        ┌──────────────┬──────────────┬──────────────┬──────────────┐
        ▼              ▼              ▼              ▼
 Linear Regression  Decision Tree  Random Forest   K-Nearest Neighbors
        │              │              │              │
        └──────────────┴──────────────┴──────────────┘
                           │
                           ▼
              Centralized Evaluation Framework
                           │
                           ▼
                 Model Performance Comparison
                           │
                           ▼
                  Automatic Best Model Selection
```

---

## Machine Learning Workflow

1. Dataset Loading
2. Exploratory Data Analysis
3. Missing Value Handling
4. Feature Encoding
5. Data Scaling
6. Train-Test Split
7. Custom Model Implementation
8. Model Training
9. Model Evaluation
10. Model Comparison
11. Best Model Selection

---

## Model Performance

| Model | MAE | RMSE | R² Score |
|------|------:|------:|------:|
| Linear Regression | ~50,670 | ~70,059 | ~0.625 |
| Decision Tree Regression | ~40,319 | ~61,015 | ~0.715 |
| **Random Forest Regression** | **~39,828** | **~57,466** | **~0.748** |
| K-Nearest Neighbors Regression | ~40,737 | ~61,351 | ~0.712 |

The **Random Forest Regression** model achieved the highest predictive performance by combining multiple decision trees trained on bootstrap samples while introducing random feature selection at every node split. This ensemble approach effectively reduced overfitting and captured complex non-linear relationships within the housing dataset.

---

## Notebook Structure

- Introduction
- Dataset Overview
- Exploratory Data Analysis
- Data Preprocessing
- Train-Test Split
- Model Evaluation Framework
- Linear Regression
- Decision Tree Regression
- Random Forest Regression
- K-Nearest Neighbors Regression
- Model Comparison
- Conclusion

---

## Dataset

**Source:** Kaggle – California Housing Prices

**Records:** 20,640

**Target Variable**

- `median_house_value`

**Input Features**

- `longitude`
- `latitude`
- `housing_median_age`
- `total_rooms`
- `total_bedrooms`
- `population`
- `households`
- `median_income`
- `ocean_proximity`

---

## Design Principles

- Simplicity
- Readability
- Explainability
- Reproducibility
- Educational Value
- Modular Design
- Clean Code

---

## Project Structure

```text
House_Price_Prediction.ipynb
housing.csv
README.md
requirements.txt
```

---

## Setup Instructions

1. Create a virtual environment

```bash
python -m venv .venv
```

2. Activate the virtual environment

**Windows**

```bash
.venv\Scripts\activate
```

**Linux / macOS**

```bash
source .venv/bin/activate
```

3. Install the dependencies

```bash
pip install -r requirements.txt
```

---

## How to Run

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
House_Price_Prediction.ipynb
```

Run every cell from top to bottom.

The notebook will automatically:

- Load and preprocess the dataset
- Train each regression model
- Evaluate model performance
- Compare all models
- Identify the best-performing model

---

## Key Learnings

This project demonstrates:

- End-to-end machine learning workflow
- Data preprocessing using Pipelines and ColumnTransformer
- Manual implementation of fundamental regression algorithms
- Recursive tree construction
- Bootstrap Aggregating (Bagging)
- Random feature selection
- Distance-based learning with K-Nearest Neighbors
- Centralized model evaluation
- Comparative performance analysis using MAE, RMSE, and R² Score

---

## Current Status

### Completed

- Exploratory Data Analysis
- Data Preprocessing Pipeline
- Linear Regression Implementation
- Decision Tree Regression Implementation
- Random Forest Regression Implementation
- K-Nearest Neighbors Regression Implementation
- Centralized Evaluation Framework
- Automatic Model Comparison
- Best Model Selection
- Comprehensive Notebook Documentation

---

## Future Improvements

- Cross-Validation
- Hyperparameter Tuning
- Feature Importance Calculation for the custom Random Forest
- Model Persistence using Joblib
- Interactive Prediction Interface
- Deployment as a Web Application