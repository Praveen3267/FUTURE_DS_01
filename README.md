# Future Interns — Task 1: Business Sales Performance Analytics

## Project Overview

This project analyzes the Sample Superstore sales dataset to understand business sales performance, profitability, product categories, regional results, monthly trends, and discount patterns. The goal is to turn transaction-level data into practical business insights and recommendations.

**Internship track:** Data Science & Analytics  
**Task:** Task 1 — Business Sales Performance Analytics  
**Primary tool:** Python in Jupyter Notebook

## Objectives

- Measure overall sales, profit, order volume, customer count, and units sold.
- Identify top-performing products and product categories.
- Compare sales and profit across regions.
- Examine monthly sales and profit trends.
- Identify loss-making product sub-categories.
- Explore how total profit varies across discount levels.
- Suggest practical actions that could improve profitability.

## Tools and Libraries

- Python
- Jupyter Notebook
- pandas — data loading, cleaning, grouping, and analysis
- NumPy — numerical operations, where needed
- Matplotlib — charts and visualizations

## Dataset

The analysis uses the **Sample Superstore** dataset. The dataset contains 9,994 records and 21 columns, including order dates, customer and location fields, product category and sub-category, sales, quantity, discount, and profit.

The dataset was inspected for data types, missing values, and duplicate rows. In the notebook's initial checks, all 9,994 rows had values in the listed columns, and no completely duplicated rows were found. Order Date and Ship Date were converted to datetime values for time-based analysis.

If sharing this project publicly, follow the dataset provider's license and attribution requirements. If redistribution of the raw CSV is not permitted, do not include the dataset in the repository; instead, explain where the reviewer can obtain it.

## Analysis Performed

1. **Data inspection and preparation**
   - Reviewed dataset dimensions, column names, data types, missing values, and duplicate rows.
   - Converted date columns to datetime format.
   - Reviewed descriptive statistics for sales, quantity, discount, and profit.

2. **Overall business performance**
   - Calculated total sales and profit, unique orders, unique products, unique customers, units sold, and overall profit margin.

3. **Product and category performance**
   - Ranked products by sales and profit.
   - Compared total sales, profit, and units sold across Technology, Furniture, and Office Supplies.
   - Aggregated performance by product sub-category.

4. **Regional performance**
   - Compared sales, profit, order counts, and units sold across West, East, Central, and South.

5. **Monthly trends**
   - Aggregated sales and profit by order month.
   - Visualized changes over time from January 2014 through December 2017.

6. **Discount and profitability analysis**
   - Compared total sales and profit at different discount levels.
   - Identified sub-categories with negative total profit.

## Key Findings

### Overall performance

| Metric | Result |
|---|---:|
| Total sales | $2,297,200.86 |
| Total profit | $286,397.02 |
| Unique orders | 5,009 |
| Unique products | 1,850 |
| Unique customers | 793 |
| Units sold | 37,873 |
| Overall profit margin | 12.47% |

*Profit margin is calculated as total profit divided by total sales.*

### Category performance

| Category | Sales | Profit | Profit margin |
|---|---:|---:|---:|
| Technology | $836,154.03 | $145,454.95 | 17.40% |
| Furniture | $741,999.80 | $18,451.27 | 2.49% |
| Office Supplies | $719,047.03 | $122,490.80 | 17.04% |

Technology had the highest sales and profit. Furniture generated substantial sales but had a much lower profit margin than the other categories.

### Regional performance

| Region | Sales | Profit |
|---|---:|---:|
| West | $725,457.82 | $108,418.45 |
| East | $678,781.24 | $91,522.78 |
| Central | $501,239.89 | $39,706.36 |
| South | $391,721.90 | $46,749.43 |

West led in both sales and profit. Central generated more sales than South but less profit, making it a useful region for further investigation.

### Monthly trends

- Highest monthly sales in the analyzed period: **November 2017 — $118,447.82**.
- Lowest monthly sales in the analyzed period: **February 2014 — $4,519.89**.
- Highest monthly profit in the analyzed period: **December 2016 — $17,885.31**.
- Lowest monthly profit in the analyzed period: **January 2015 — -$3,281.01**.

Monthly results fluctuate. These observations describe this dataset and should not be treated as a forecast.

### Sub-category performance

| Sub-category | Sales | Profit |
|---|---:|---:|
| Tables | $206,965.53 | -$17,725.48 |
| Bookcases | $114,880.00 | -$3,472.56 |
| Supplies | $46,673.54 | -$1,189.10 |
| Copiers | $149,528.03 | $55,617.82 |
| Phones | $330,007.05 | $44,515.73 |
| Accessories | $167,380.32 | $41,936.64 |

Tables had the largest loss among the sub-categories shown. Copiers, Phones, and Accessories were strong profit contributors.

### Discount analysis

In the analyzed data, some higher discount levels were associated with negative total profit. For example, transactions with a 30% discount had total profit of **-$10,369.28**, while the 70% discount group had total profit of **-$40,075.36**.

This is an observational comparison, not proof that discounts alone caused the losses. Discount groups differ in transaction counts, products, and sales values, so a deeper analysis would be needed before making causal claims.

## Business Recommendations

1. **Investigate Furniture profitability.** Review costs, prices, discount levels, and product mix, especially for Tables and Bookcases.
2. **Review high-discount transactions.** Check whether large discounts are being applied to products or orders that already have low margins. Consider approval rules or minimum-margin checks.
3. **Learn from profitable products.** Examine the sales channels, customer segments, and pricing of strong contributors such as Copiers, Phones, and Accessories.
4. **Investigate the Central region.** Compare its product mix, discount patterns, and sub-category results with the West and East.
5. **Monitor sales and profit together.** A high sales total does not necessarily mean a product or category is profitable.
6. **Track monthly performance.** Continue monitoring sales, profit, and margin to understand recurring patterns before planning inventory or promotions.

These recommendations identify areas to investigate; they do not establish the cause of any loss.

## Project Files

The intended project structure is:

```text
FUTURE_DS_01/
├── Task1_Sales_Analysis.ipynb
├── README.md
└── charts/
```

The notebook contains the Python code, tables, and visualizations. Add exported chart images to the `charts/` folder if you choose to include them.

## How to Run

1. Install Python and Jupyter Notebook, or use an existing Jupyter environment.
2. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib
   ```

3. Place the dataset where the notebook expects it, or update the CSV file path in the notebook.
4. Open `Task1_Sales_Analysis.ipynb` in Jupyter.
5. Run the notebook cells from top to bottom.

**Note:** The CSV filename and path in the notebook must match your local file. If the dataset is not included in the public repository, obtain it separately from its original source and follow its terms.

## Limitations

- This is a descriptive analysis of historical transaction data.
- Relationships between discounts and profit are not, by themselves, evidence of causation.
- The analysis does not include cost breakdowns beyond the provided profit field, nor does it build a predictive model.
- Business recommendations should be validated with additional operational and financial context.

## Author

Prepared as a portfolio project for the Future Interns Data Science & Analytics internship.

---

*This README summarizes the analysis currently performed in the notebook. Update it if the notebook, charts, or project scope changes.*
