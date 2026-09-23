# Predicting House Prices with Linear Regression

Predicts house price from area, location, number of rooms, and age, and
walks through the full pipeline from cleaning to model interpretation.

## Project structure
```
house-price-prediction/
├── data/
│   └── house_data_raw.csv                 # Raw dataset (see note below)
├── notebooks/
│   └── house_price_prediction.ipynb       # Full, executed pipeline
└── README.md
```

## Dataset
`data/house_data_raw.csv` is a generated dataset (1,200+ rows) in the same
schema as Kaggle's popular "Housing Price Prediction Data" dataset:
`SquareFeet, Bedrooms, Bathrooms, Neighborhood, YearBuilt, Price`. Prices
follow a realistic linear relationship with noise (bigger, newer, more
urban homes cost more). A small, seeded set of cells has been perturbed
with inconsistent category casing, a few missing values, and a handful of
duplicate rows so the notebook's data-cleaning section has real messiness
to fix.

**To use real data instead:** search "house price prediction dataset" on
Kaggle for the Ames Housing dataset or the "House Prices: Advanced
Regression Techniques" competition data, download it into `data/`, and
adjust the column names referenced in Section 2 of the notebook to match.
The rest of the pipeline works the same way regardless of source.

## How to run
```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
jupyter notebook notebooks/house_price_prediction.ipynb
```

## Pipeline
1. Load & inspect data, null check, descriptive stats, price distribution
2. Feature selection discussion (markdown)
3. Data cleaning (nulls, duplicates, inconsistent categories)
4. EDA
5. Feature engineering (`Age`) & One-Hot Encoding
6. Correlation heatmap
7. Train/test split (80/20)
8. Train Linear Regression
9. Evaluate: MSE, RMSE, R²
10. Actual vs. predicted scatter plot
11. Residual plot
12. Coefficient analysis (standardized coefficients)
13. Bonus: Ridge & Lasso comparison

## Results
| Model              | MAE     | RMSE    | R²     |
|---------------------|---------|---------|--------|
| Linear Regression     | 17,686  | 22,291  | 0.9766 |
| Lasso                  | 17,686  | 22,291  | 0.9766 |
| Ridge                  | 17,698  | 22,301  | 0.9766 |

`SquareFeet` is the dominant price driver, with `Neighborhood` (location)
and room counts also contributing meaningfully.
