# End-to-End E-Commerce Customer Intelligence and Sales Forecasting

This is a runnable Python portfolio project that turns raw e-commerce transactions into business decisions.

It answers:

- Who are the most valuable customers?
- Which products generate the most revenue?
- Which customers are likely to stop buying?
- What are the weekly and monthly sales trends?
- Can we forecast future sales?
- Which customer segments should receive promotions?

## What the project demonstrates

- Data cleaning with Pandas and NumPy
- SQL-backed business analysis with SQLite
- Exploratory data analysis
- Feature engineering
- RFM customer segmentation
- Churn-risk modeling
- Regression-style sales forecasting
- Model evaluation
- Data visualization with Matplotlib, with optional Seaborn styling

## Project structure

```text
ecommerce_customer_intelligence/
  run_pipeline.py
  requirements.txt
  sql/business_queries.sql
  src/ecommerce_intelligence/
    analytics.py
    cleaning.py
    config.py
    data_generation.py
    database.py
    modeling.py
    reporting.py
    visualization.py
  data/
    raw/
    processed/
  reports/
    figures/
```

## Quick start

Open a terminal in this project folder and create the virtual environment once:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

Run the pipeline from the project folder:

```bash
python run_pipeline.py
```

Or, without activating the environment, run it using the project interpreter directly:

```bash
.venv/bin/python run_pipeline.py
```

On Windows, use `.venv\Scripts\python.exe` in place of `.venv/bin/python`.

The explicit virtual-environment interpreter avoids relying on a system-wide `python` command or packages installed for a different Python interpreter. The pipeline generates synthetic messy e-commerce data, cleans it, stores it in SQLite, runs customer and sales analytics, trains churn and forecasting logic, and writes all outputs into `reports/`, `data/processed/`, and `models/`.

Scikit-learn and Seaborn have built-in fallbacks if unavailable; Pandas, NumPy, and Matplotlib are required. Installing `requirements.txt` enables the full modeling and visualization path.

## Main outputs

- `reports/executive_summary.html` - client-ready summary of key decisions
- `reports/analytics_summary.json` - machine-readable metrics
- `reports/top_customers.csv` - highest-value customers
- `reports/top_products.csv` - highest-revenue products
- `reports/customer_segments.csv` - RFM and promotion targeting
- `reports/churn_risk_customers.csv` - ranked churn-risk list
- `reports/sales_forecast.csv` - 12-week forward revenue forecast
- `reports/figures/*.png` - visualizations for the report
- `data/processed/ecommerce_cleaned.csv` - cleaned transaction table
- `data/processed/ecommerce.sqlite` - SQLite analysis database

## Business interpretation

The generated report translates analytics into actions:

- Reward champions and loyal high-value buyers.
- Win back at-risk high-value customers before they lapse.
- Send targeted promotions to promising and price-sensitive groups.
- Prioritize inventory and merchandising around high-revenue products.
- Use weekly and monthly sales trends to guide revenue planning.
