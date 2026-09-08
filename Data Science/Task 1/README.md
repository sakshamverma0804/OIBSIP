# Task 1 — Iris Flower Classification
**OIB-SIP Internship | Machine Learning**

## Objective
Train ML classifiers to identify the species of an iris flower (Setosa, Versicolor, Virginica) from its physical measurements.

## Tech Stack
- Python 3.10+
- scikit-learn, pandas, numpy
- matplotlib, seaborn
- Jupyter Notebook

## Project Structure
`
Task1_Iris_Classification/
 iris_classification.ipynb   # Main notebook (all code + analysis)
 requirements.txt            # Python dependencies
 README.md                   # This file
 pairplot.png                # Generated after running the notebook
 boxplots.png                # Generated after running the notebook
 heatmap.png                 # Generated after running the notebook
 violins.png                 # Generated after running the notebook
 feature_importance.png      # Generated after running the notebook
 confusion_matrices.png      # Generated after running the notebook
 accuracy_comparison.png     # Generated after running the notebook
`

## Setup & Run
`ash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Launch Jupyter Notebook
jupyter notebook iris_classification.ipynb

# 3. Run All Cells  (Kernel -> Restart & Run All)
`

## Checklist
- [x] Load Iris dataset from sklearn (no download required)
- [x] EDA: shape, dtypes, null check, descriptive statistics
- [x] Visualisations: pairplot, box plots, heatmap, violin plots
- [x] Feature selection discussion + RF importance bar chart
- [x] 80/20 stratified train/test split + StandardScaler
- [x] 4 classifiers trained: Logistic Regression, KNN, Decision Tree, Random Forest
- [x] Evaluation: accuracy, 5-fold CV, confusion matrix, classification report
- [x] Best model identified with justification
