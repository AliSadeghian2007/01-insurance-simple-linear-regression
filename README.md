# Insurance Cost Prediction: Simple Linear Regression

## Overview
This project predicts individual medical insurance expenses from a single feature, **age**, using simple linear regression. It covers the basic ML workflow: loading and exploring data, splitting into train and test sets, training a model, and evaluating it.

## Dataset
**Medical Cost Personal Datasets** from Kaggle (by Miri Choi):
https://www.kaggle.com/datasets/mirichoi0218/insurance

1,338 rows with the columns `age`, `sex`, `bmi`, `children`, `smoker`, `region` and `expenses`. There are no missing values. In this project only `age` (input) and `expenses` (target) are used.

## Approach
1. Explored the data (`info`, `head`, `describe`, missing values).
2. Plotted age vs expenses with a scatter plot.
3. Split the data into 80% train and 20% test (`random_state=0`).
4. Trained a `LinearRegression` model on the training set only.
5. Evaluated on the test set with R² and MAE.
6. Plotted the regression line over the train and test points.

## Results
| Metric | Value |
|--------|-------|
| R² (test) | ≈ 0.125 |
| MAE (test) | ≈ $9,147 |
| Coefficient of `age` | ≈ 240 |

## Key Takeaways
- Expenses increase with age: each extra year adds about $240 on average.
- R² is low, so age alone explains only a small part of the variation in expenses. The scatter plot shows three separate bands, which suggests other variables also matter.
- The next step is to add more features with multiple linear regression.

## Project Structure
```
01-insurance-simple-linear-regression/
├── data/
│   └── insurance.csv
├── insurance-simple-linear-regression.ipynb
├── requirements.txt
└── README.md
```

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook
```
Then open `insurance-simple-linear-regression.ipynb` and run all cells.
