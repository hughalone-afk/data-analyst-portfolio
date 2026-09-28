# Data Analyst Portfolio

Four end-to-end analytics projects, built from coursework practice and completed independently,
plus a folder of reference labs from the underlying course material.

## Projects

| # | Project | Business framing | Techniques |
|---|---------|-------------------|------------|
| 1 | [House Sales Price Prediction](01-house-sales-price-prediction/) | Data analyst at a real estate investment trust, valuing acquisition targets in King County, WA | Data wrangling, EDA, multiple linear regression, pipelines, Ridge regression, polynomial features |
| 2 | [Laptop Price Prediction](02-laptop-price-prediction/) | Estimating a fair retail price for a laptop from its specs | Missing-data handling, feature engineering, correlation analysis, polynomial regression, cross-validation, Grid Search |
| 3 | [Insurance Cost Analysis](03-insurance-cost-analysis/) | Predicting individual medical insurance charges from demographic/lifestyle data | Data cleaning, EDA, multiple regression, Ridge regression, train/test evaluation |
| 4 | [Automobile Sales Analysis](04-automobile-sales-analysis/) | Understanding how recessions have hit an automaker's sales by vehicle type, 1980–2023 | Matplotlib/Seaborn visualization, EDA, plus an interactive Plotly Dash dashboard |

Each project folder has its own README with the business problem, approach, and how to run it.

## How to run any project

Every notebook loads its dataset directly from a public URL via `pandas.read_csv()`, so it needs an
internet connection. Open them in:
- **Google Colab** (upload the `.ipynb` or open from GitHub) — no local setup needed, or
- **Jupyter/VS Code locally** — requires `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`.

Run all cells top to bottom. Plots and R²/MSE values will render as you go — fill in the "Key
Findings" section at the end of each notebook with your actual numbers (most cells in Project 4's
notebook already have real output baked in from a previous run).

Project 4's dashboard (`automobile_sales_dashboard.py`) is a script, not a notebook — it needs a
local Python environment (`pip install dash pandas plotly`, then `python automobile_sales_dashboard.py`),
since Colab doesn't run a Dash server well.

## Tech stack

Python · pandas · NumPy · Matplotlib · Seaborn · Plotly Express · Dash · scikit-learn (Linear/Ridge
regression, Pipelines, PolynomialFeatures, GridSearchCV, cross-validation)

## `coursework-reference/`

Walkthrough notebooks from the underlying course (IBM's "Data Analysis with Python"), followed
along on the instructor's own automobile-pricing dataset. These demonstrate the same techniques but
aren't original analysis — kept here as supporting evidence of course completion, not listed as
standalone projects. If you took the same course, you'll recognize these; that's expected, and is
exactly why they're filed separately from the three projects above rather than presented as
portfolio pieces themselves.
