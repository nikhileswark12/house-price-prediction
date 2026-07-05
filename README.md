# House Price Prediction
### A Machine Learning Regression Project for Estimating Median House Prices

House Price Prediction is a machine learning project that estimates the median house
value of a district based on features such as location, median income, housing age,
room and bedroom counts, population, and proximity to the ocean. The project focuses
on a complete, transparent, and beginner-accessible machine learning workflow,
covering data exploration, preprocessing, model training, evaluation, and model
comparison.

Housing prices are influenced by a combination of geographic and socioeconomic
factors that are difficult to estimate through simple rule-of-thumb reasoning.
Manual or intuition-based price estimation often fails to account for the combined
effect of location, income levels, and housing density. This project addresses that
gap by applying supervised regression techniques to a real-world dataset, allowing
house prices to be estimated in a consistent, data-driven, and reproducible way.

The project follows a single-notebook workflow built with Python, pandas, and
scikit-learn, comparing multiple regression models to identify the best-performing
approach on the given dataset.

## Vision
To build a clear, reproducible, and fully explainable regression pipeline that
demonstrates the complete machine learning workflow, from raw data to a trained
and evaluated predictive model.

## Problem Statement
Estimating housing prices accurately involves several practical challenges:

- Housing prices are affected by non-linear, interacting geographic factors.
- Categorical location data (ocean proximity) must be properly encoded for use in a model.
- Missing values in real-world datasets can break naive modeling approaches.
- Simple linear assumptions often fail to capture true price behavior.
- Without model comparison, it is difficult to know which approach is actually best suited to the data.

This project addresses these challenges through structured data cleaning, feature
encoding, and a side-by-side comparison of multiple regression models.

## Key Features
- Exploratory data analysis with correlation and distribution visualizations
- Missing value handling for incomplete housing records
- One-hot encoding of categorical location data
- Multiple regression model training and comparison
- Standardized evaluation using MAE, RMSE, and R² Score
- Feature importance visualization
- Automatic identification of the best-performing model based on R² score

## Technology Stack

| Category | Technologies |
|---|---|
| Language | Python 3.11+ |
| Environment | Jupyter Notebook |
| Data Handling | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn |

## System Architecture
This project follows a simple, linear, single-notebook architecture.

- Raw housing data is loaded directly from a CSV file into a pandas DataFrame.
- Missing values and categorical fields are cleaned and encoded prior to modeling.
- The dataset is split into training and testing sets using an 80/20 split.
- Three regression models are trained independently on the same training data.
- Each model is evaluated on the same held-out test set for a fair comparison.
- The best-performing model is identified automatically based on R² score.

This architecture keeps the workflow easy to follow, reproduce, and explain end to
end, which is intentional given the project's beginner-level scope.

## Machine Learning Pipeline
1. Dataset Loading
2. Exploratory Data Analysis
3. Missing Value Handling
4. Categorical Feature Encoding
5. Train-Test Split
6. Model Training (Linear Regression, Decision Tree, Random Forest)
7. Model Evaluation
8. Feature Importance Analysis
9. Best Model Selection

## Model Performance

**Linear Regression**

| Metric | Value |
|---|---|
| MAE | $50,670.74 |
| RMSE | $70,060.52 |
| R² Score | 0.625 |

**Decision Tree**

| Metric | Value |
|---|---|
| MAE | $44,180.85 |
| RMSE | $69,755.78 |
| R² Score | 0.629 |

**Random Forest (Final Model)**

| Metric | Value |
|---|---|
| MAE | $31,639.37 |
| RMSE | $49,038.20 |
| R² Score | 0.816 |

The Random Forest model was selected as the final model due to its clear improvement
in accuracy over both the linear and single-tree baselines, driven by its ability to
capture non-linear relationships between location, income, and housing price.

## Notebook Sections
- Load Data
- Exploratory Data Analysis
- Handle Missing Values
- Encode Categorical Data
- Train-Test Split
- Train Models
- Compare Results
- Feature Importance
- Best Model Selection

## Dataset
- **Source:** Kaggle - California Housing Prices
- **Link:** https://www.kaggle.com/datasets/camnugent/california-housing-prices
- **Records:** 20,640
- **Target Variable:** `median_house_value`

**Features**
- `longitude`
- `latitude`
- `housing_median_age`
- `total_rooms`
- `total_bedrooms`
- `population`
- `households`
- `median_income`
- `ocean_proximity`

## Design Principles
- Simplicity and Readability
- Full Explainability of Every Step
- Fair, Consistent Model Comparison
- Reproducible Results
- Clean, Minimal Project Structure
- No Hidden or Unnecessary Complexity

## Project Structure
```
House_Price_Prediction.ipynb
housing.csv
README.md
requirements.txt
```

## Setup Instructions
1. Create a virtual environment:
   ```bash
   python -m venv .venv
   ```
2. Activate the virtual environment:
   - Windows: `.venv\Scripts\activate`
   - macOS/Linux: `source .venv/bin/activate`
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## How to Run
1. Ensure the virtual environment is activated and dependencies are installed.
2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Open `House_Price_Prediction.ipynb`.
4. Run all cells from top to bottom to execute the full pipeline, train all three
   models, and print out the best-performing model based on R² score.

## Current Status

**Completed**
- Data Loading and Exploration
- Missing Value Handling
- Categorical Encoding
- Model Training (Linear Regression, Decision Tree, Random Forest)
- Model Evaluation and Comparison
- Feature Importance Visualization
- Best Model Selection

**Planned Enhancements**
- Model Persistence (saving the best model to disk)
- Hyperparameter Tuning
- Cross-Validation
- Additional Model Types (e.g. Gradient Boosting)
- Prediction Interface for New Inputs
- Deployment as a Simple Web Application