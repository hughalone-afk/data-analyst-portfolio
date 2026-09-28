# House Sales Price Prediction — King County, WA

## Business problem

Acting as a data analyst for a real estate investment trust, determine the market price of a
residential property from its features (square footage, bedrooms, bathrooms, floors, location,
condition, grade, etc.), so the Trust can evaluate whether a listed price is fair before acquiring
a property.

## Dataset

House sale prices for King County (which includes Seattle), covering homes sold between May 2014
and May 2015. ~21,600 rows, 21 features. Loaded directly from a public CSV URL in the notebook —
originally sourced from [Kaggle](https://www.kaggle.com/harlfoxem/housesalesprediction).

## Approach

1. **Data wrangling** — inspect data types, drop identifier columns, impute missing bedroom/bathroom
   values with the column mean.
2. **Exploratory data analysis** — distribution of floor counts, waterfront-view price outliers via
   boxplot, `sqft_above` vs. price via regression plot, full correlation matrix.
3. **Model development** — build up from a single-feature model (`sqft_living`) to an 11-feature
   multiple regression, then wrap scaling + polynomial features + regression in a single pipeline.
4. **Model evaluation & refinement** — train/test split, Ridge regression (α = 0.1), and a
   polynomial-feature + Ridge combination, comparing test-set R² across all of the above.

## How to run

Open `house_sales_price_prediction.ipynb` in Colab or Jupyter (needs internet access to load the
dataset) and run all cells top to bottom. Fill in the **Key Findings & Recommendation** section at
the end with your actual R² values once it's run.

## Tech stack

pandas · NumPy · Matplotlib · Seaborn · scikit-learn (LinearRegression, Ridge, Pipeline,
StandardScaler, PolynomialFeatures, train_test_split)
