# Laptop Price Prediction

## Business problem

Estimate a fair retail price for a laptop from its hardware specs (CPU speed, RAM, storage type and
size, screen size, GPU, category, OS), and identify which specs actually move the price — useful
for pricing new SKUs or flagging listings that are over/under-priced for their specs.

## Dataset

A laptop-specs dataset (~230 rows) with price plus ~10 hardware/category attributes. Loaded
directly from a public CSV URL in the notebook.

## Approach

This project was originally worked through as four separate hands-on labs; `laptop_price_prediction.ipynb`
consolidates them into one continuous pipeline:

1. **Data wrangling** — handle missing values (mean for continuous, mode for categorical), fix data
   types, convert units (kg→lb, cm→in), normalize CPU frequency, bin price into Low/Medium/High, and
   one-hot encode the `Screen` attribute.
2. **Exploratory data analysis** — regression plots and Pearson correlation for continuous features
   (CPU frequency, screen size, weight), boxplots for categorical features (category, GPU, OS,
   CPU core count, RAM, storage), and a GPU × CPU-core pivot table/heatmap against price.
3. **Model development** — single-variable regression (CPU frequency), multiple-variable regression
   (7 features), polynomial regression (degrees 1/3/5), and a full scale + polynomial + regression
   pipeline.
4. **Model evaluation & refinement** — train/test split, cross-validation, an overfitting check
   across polynomial degrees 1–5, and a Grid-Search-tuned Ridge regression as the final model.

`lab-notebooks/` holds the four original labs individually completed, if you want to see each stage
in isolation or compare it against the consolidated version.

## How to run

Open `laptop_price_prediction.ipynb` in Colab or Jupyter (needs internet access to load the
dataset) and run all cells top to bottom. Fill in the **Key Findings & Recommendation** section at
the end with your actual numbers once it's run.

## Tech stack

pandas · NumPy · Matplotlib · Seaborn · SciPy (Pearson correlation) · scikit-learn (LinearRegression,
Ridge, Pipeline, PolynomialFeatures, train_test_split, cross_val_score, GridSearchCV) · tqdm
