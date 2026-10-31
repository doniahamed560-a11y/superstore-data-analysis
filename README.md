# Superstore Sales – Exploratory Data Analysis

An end-to-end data analysis project on the **Superstore** retail dataset using Python. It covers data understanding, cleaning (including IQR-based outlier removal), feature engineering, GroupBy analysis, visualization, and a final EDA with business insights.


## Dataset

- **Source:** [Superstore Dataset – Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
- **Size:** 9,994 rows × 21 columns
- **Description:** Each row is one sales transaction, with details about the order, customer, product, shipping, and profit.

| Column | Description |
|---|---|
| Order ID / Order Date / Ship Date | Order identifier and dates |
| Customer ID / Customer Name | Customer information |
| Segment | Consumer, Corporate, or Home Office |
| Country / City / Region | Geographic location |
| Category / Sub-Category / Product Name | Product classification |
| Sales / Quantity / Discount / Profit | Core financial metrics |

## Project Workflow

1. **Dataset Understanding** – loaded the data with `kagglehub` and inspected it (`head`, `info`, `describe`, `shape`).
2. **Data Cleaning** – no missing values or duplicates; verified data types; removed `Sales` outliers with the IQR method and kept both the original (`df`) and outlier-free (`df_new`) versions for comparison.
3. **Feature Engineering** – `Shipping_Duration`, `Profit_Ratio`, `product_rank`.
4. **Data Analysis (GroupBy)** – sales/profit by category, region, segment, sub-category, and ship mode, before and after outlier removal.
5. **Visualization** – boxplot (before vs. after), histogram, and scatter plot, each with an interpretation.
6. **EDA** – combined all steps and extracted key insights.

## Key Insights

1. **Discounts hurt profitability:** many loss-making transactions, especially in *Furniture*, mostly due to high discounts.
2. **Technology drives profit:** highest average sales and average profit per order.
3. **Regional differences:** *West* and *East* generate the highest profit.
4. **Unbalanced sales distribution:** most sales are small, while a few large transactions contribute heavily to revenue.
5. **Shipping:** *Same Day* is the fastest ship mode and *Standard Class* the slowest.

## Tools & Libraries

Python 3 · Pandas · NumPy · Matplotlib · Seaborn · KaggleHub · Jupyter Notebook

## How to Run

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
pip install numpy pandas matplotlib seaborn kagglehub jupyter
jupyter notebook Data_Analysis_Project.ipynb
```

The dataset is downloaded automatically through `kagglehub`.

## License

For educational purposes.
