# Retail Sales Analysis

## Description

This project analyzes a retail transactional dataset to evaluate business performance in terms of sales, profit, and profitability patterns across categories, subcategories, and regions.

The objective is to identify performance differences, detect inefficiencies, and support data-driven decision-making through a structured analytical approach and a Power BI dashboard.

---

## Dataset

The dataset contains retail transaction-level records with the following variables:

**Original variables:**

* order_date
* region
* category
* sub_category
* product_name
* sales
* quantity
* discount
* profit

**Derived variables:**

* year
* month
* month_name
* sales_per_unit
* profit_margin
* outliers_sales
* outliers_profit

The dataset represents individual sales transactions, where each row corresponds to a product-level record within an order.

The final dataset used for the dashboard is located at:

```
data/processed/superstore_dashboard.csv
```

---

## Methodology

The analysis follows a structured workflow:

1. Data exploration to understand structure and distributions
2. Data validation (data types, consistency checks)
3. Feature engineering (derived variables)
4. Dataset preparation for reporting
5. Dashboard development in Power BI

No assumptions were made beyond the available data.

---

## Dashboard

The dashboard was developed in Power BI to support exploratory and comparative analysis across key dimensions.

It includes:

* Sales by category
* Profit by subcategory
* Sales vs Profit relationship (scatter plot)
* Sales trend over time
* Sales by region
* Geographic distribution of sales

**Key KPIs:**

* Total Sales: ~2.33M
* Total Profit: ~0.29M
* Profit Margin: 12.56%

### Dashboard Preview

![Dashboard](images/dashboard_overview.png)

### Dashboard File

```
dashboard/retail_sales_dashboard.pbix
```

---

## Business Questions

The analysis is guided by the following questions:

* Which categories generate the highest sales and profit?
* How does profit behave relative to sales across products?
* Which subcategories contribute positively or negatively to profit?
* How does sales performance vary across regions?
* Are there observable inefficiencies in specific subcategories?

These questions are addressed using the available variables without extending beyond the dataset scope.

---

## Key Insights

* Technology generates the highest sales (~0.84M) and the highest profit (~0.15M), making it the main contributor at the category level.

* Profit is not strictly proportional to sales. The Sales vs Profit visualization shows dispersion, including observations with high sales and low or negative profit.

* The West region has the highest sales (~0.74M), while the South region shows the lowest (~0.39M), indicating a measurable regional performance gap.

* Profit is concentrated in a limited number of subcategories. Phones (~45K) and Paper (~35K) are the largest contributors, while some subcategories (e.g., Tables) show negative profit (~ -18K).

All insights are derived directly from aggregated measures in the dataset.

---

## Business Recommendations

Based strictly on observed patterns:

* Review subcategories with negative profit (e.g., Tables) to identify operational or pricing issues.

* Monitor the relationship between sales and profit to avoid growth that does not translate into profitability.

* Prioritize subcategories with consistent positive contribution to profit (e.g., Phones, Paper).

* Investigate regional differences to understand performance variation between West and South.

These recommendations are exploratory and should be validated with additional data before implementation.

---

## Limitations of the Analysis

The analysis is subject to the following constraints:

* No detailed cost structure is available; profit is used as provided without decomposition.

* No customer-level data is included, preventing behavioral or segmentation analysis.

* Discount impact is not isolated, limiting causal interpretation of profitability drivers.

* External factors (market conditions, competition, seasonality drivers) are not included.

* Aggregations may obscure variability at the transaction level.

The results should be interpreted within these limitations.

---

## Project Structure

```
retail_sales_analysis/

data/
    raw/
    processed/

notebooks/
    01_data_exploration.ipynb
    02_data_cleaning.ipynb

dashboard/
    retail_sales_dashboard.pbix

images/
    dashboard_overview.png

README.md
requirements.txt
.gitignore
```

---

## Tools Used

* Python (pandas, numpy)
* Jupyter Notebook
* Power BI

---

## Conclusion

The dataset shows that the business is profitable at an aggregate level (12.56% margin), but profitability is unevenly distributed across subcategories and not strictly aligned with sales volume.

The analysis identifies areas of strong contribution as well as segments with negative performance, providing a structured basis for further investigation.

No conclusions extend beyond what the data supports.
