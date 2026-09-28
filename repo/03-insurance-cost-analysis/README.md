# Insurance Cost Analysis

## Business problem

Predict an individual's annual medical insurance charges from demographic and lifestyle attributes
(age, sex, BMI, number of children, smoking status, region), and identify which factors drive cost
the most — the kind of analysis an insurer would use to sanity-check risk-based pricing.

## Dataset

Medical insurance cost records (age, gender, BMI, children, smoker status, region, charges). Loaded
directly from a public CSV URL in the notebook.

## Approach

1. **Import & prepare** — add column headers (the raw CSV has none), replace `'?'` placeholders with
   proper `NaN`.
2. **Data wrangling** — impute missing values (mean for `age`, most-frequent for `smoker`), round
   `charges` to 2 decimal places.
3. **Exploratory data analysis** — regression plot of `charges` vs. `bmi`, boxplot of `charges` by
   `smoker` status, full correlation matrix.
4. **Model development** — single-feature baseline (`smoker` only) vs. a full 6-feature regression,
   then a scale + polynomial + regression pipeline evaluated in-sample.
5. **Model refinement** — 80/20 train/test split, plain Ridge regression vs. Ridge on second-degree
   polynomial features, both evaluated on the held-out test set.

## How to run

Open `insurance_cost_analysis.ipynb` in Colab or Jupyter (needs internet access to load the
dataset) and run all cells top to bottom. Fill in the **Key Findings & Recommendation** section at
the end with your actual R² values once it's run.

## Tech stack

pandas · NumPy · Matplotlib · Seaborn · scikit-learn (LinearRegression, Ridge, Pipeline,
StandardScaler, PolynomialFeatures, train_test_split, r2_score)
