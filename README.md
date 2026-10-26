# 🩺 Medical Cost Prediction

**Machine Learning | Linear Regression**

Can we estimate medical insurance charges using age, BMI, smoking status, and other information? In this project, we explore an insurance dataset, train a Linear Regression model, and compare predicted charges with actual values.

## Dataset

- **Source:** [Medical Cost Personal Datasets — Kaggle](https://www.kaggle.com/datasets/mirichoi0218/insurance)
- **File:** `insurance.csv`
- **Size:** 1,338 records and 7 columns
- **Target:** `charges` (billed medical insurance charges)
- **Features:** `age`, `sex`, `bmi`, `children`, `smoker`, `region`

The CSV file is read locally from the same folder as the notebook. It has no missing values. The original data contains one duplicate row, which is retained in this beginner project.

## Project Workflow

1. Load and explore the data with Pandas
2. Visualize charges by smoking status and age, and check numeric correlations
3. Convert categorical features into numeric columns with `pd.get_dummies()`
4. Split the data into **80% training** and **20% test** sets
5. Train a **Linear Regression** model and make predictions
6. Evaluate with **MAE, RMSE, and R²** and compare actual vs. predicted charges

## Results

Results from the notebook's test split (`random_state=42`):

| Metric | Value |
|---|---:|
| MAE | 4,181.19 |
| RMSE | 5,796.28 |
| R² | 0.784 |

These are evaluation results on one held-out split, not guaranteed performance on new populations.

## Run Locally

Keep these files in the same folder:

```text
medical-cost-prediction/
├── Medical_Cost_Prediction.ipynb
├── insurance.csv
└── README.md
```

Open `Medical_Cost_Prediction.ipynb` in JupyterLab or Jupyter Notebook and run the cells in order. Python packages used: **pandas, matplotlib, seaborn, scikit-learn**.

## Limitations

This is an educational regression exercise using a small public dataset of US insurance charges. The model does not establish causal relationships or provide medical advice, insurance pricing advice, or reliable individual healthcare-cost forecasts. More extensive validation would be needed for real-world use.

## Data Attribution

Dataset: [Medical Cost Personal Datasets on Kaggle](https://www.kaggle.com/datasets/mirichoi0218/insurance). Review the dataset's license and reuse conditions before redistributing its CSV file.
