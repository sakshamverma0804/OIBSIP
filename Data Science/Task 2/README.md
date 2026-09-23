# Car Price Prediction with Machine Learning

Predicts the selling price of a used car from brand, age, kilometers driven,
fuel type, and transmission, using the classic **CarDekho used-car dataset**
(301 real listings).

## Project structure
```
car-price-prediction/
├── data/
│   └── car_data_raw.csv         # Raw dataset (see note below)
├── notebooks/
│   └── car_price_prediction.ipynb   # Full, executed pipeline
└── README.md
```

## Dataset
`data/car_data_raw.csv` is the well-known "CAR DETAILS FROM CARDEKHO" dataset
(301 rows: Car_Name, Year, Selling_Price, Present_Price, Kms_Driven,
Fuel_Type, Seller_Type, Transmission, Owner; prices in INR Lakhs).

A small, seeded set of cells has been perturbed with inconsistent category
casing, a few missing values, and a few extra duplicate rows so the
notebook's data-cleaning section has real messiness to fix — the underlying
301 car listings are the real CarDekho data. If you'd rather use the full
Kaggle dataset ("Vehicle dataset from CarDekho" by nehalbirla, ~8,000 rows),
download it from Kaggle and drop it in `data/` — the column names match, so
the notebook works unchanged.

## How to run
```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
jupyter notebook notebooks/car_price_prediction.ipynb
```

## Pipeline
1. Load & inspect data
2. Data cleaning (nulls, duplicates, inconsistent categories)
3. Feature engineering (`Car_Age`, `Brand`)
4. EDA (price distribution, price vs fuel type, price vs age)
5. One-hot encoding
6. Correlation heatmap
7. Train/test split
8. Model training: Linear Regression, Random Forest, Gradient Boosting
9. Evaluation: MAE, RMSE, R²
10. Feature importance chart (best model)

## Results
| Model              | MAE  | RMSE | R²   |
|---------------------|------|------|------|
| Random Forest        | 0.67 | 2.06 | 0.900 |
| Gradient Boosting     | 0.69 | 2.55 | 0.847 |
| Linear Regression     | 1.10 | 2.58 | 0.843 |

Random Forest is the best-performing model on this dataset.
