# Superstore Sales Analysis

Exploratory data analysis of the Sample - Superstore dataset (9,994 order lines from Jan 2014 to Dec 2017) to find out where the business is making a profit, where it's losing money and how the discount structure affects profitability.

**Tools:** Python, Pandas, NumPy, Matplotlib

## Key numbers

| Metric | Value |
|---|---|
| Total Sales | 2,297,200.86 |
| Total Profit | 286,397.02 |
| Overall profit margin | 12.47% |
| Total Orders | 5,009 |
| Total Customers | 793 |
| Average Order Value | 458.61 |
| Average Order Profit | 57.18 |

## What the notebook covers

- Data checks (shape, data types, null values) and date feature engineering (Year, Year-Month)
- Sales, profit and profit margin by **Category**, **Sub-Category**, **Segment** and **Region**
- Top 10 cities by sales
- Yearly sales and profit trends, year-over-year growth and yearly margin
- Monthly sales and profit trends
- Top 10 best-selling products
- **Discount analysis:** sales, total profit, average profit and margin at each discount level
- Loss-making products

## Key findings

1. Furniture is the weak spot. It accounts for 32.3% of sales and only 6.4% of profit. Its margin is 2.49% as opposed to 17.40% for Technology and 17.04% for Office Supplies.
2. Some of the sub-categories are actually making a loss. Tables (-17,725), Bookcases (-3,473) and Supplies (-1,189) are all loss making, whilst Copiers are making 19.4% of the total profit from just 6.5% of sales.
3. Discounts in excess of 20% destroy profit. The margin drops from 29.51% (no discount) to 11.82% at 20% and becomes negative at 30% (-10.05%). All discount levels above 30% have a negative total profit. The correlation between discount and profit is -0.219.
4. Central has the lowest margin at 7.92% (West at 14.94%). Central's average discount is 24.0% (West at 10.9%).
5. Sales and profit both increased from 2014 to 2017 (+51.4% and +88.6% respectively). Sales were down 2.83% in 2015 but profit was up 24.37% that year, again due to improved margins in Technology and Office Supplies. In 2017 margins declined by 0.69pp despite sales increasing by 20.36%.
6. Sales are seasonal. The three peak months of the year are September, November and December and these three months account for 51.6% of total sales.
7. High sales don't necessarily equate to high profit. 4 of the top 10 cities by sales and 4 of the top 10 best selling products are all loss making.
8. 301 of the 1,850 products are loss making (total loss 77,068). The biggest losses are the Cubify CubeX 3D Printer Double Head (-8,880) and the Lexmark MX611dhe Monochrome Laser Printer (-4,590).

## Recommendations

| Finding | Recommendation |
|---|---|
| Profit turns negative above 20% discount | Cap discounts at 20% |
| Furniture margin is only 2.49% | Review furniture pricing and discount policy |
| Tables and Bookcases lose money | Limit discounts on these sub-categories |
| Central region has a very high discount level | Fix the discount policy in Central first |
| 70% discount orders caused large losses on machines | Add an approval rule for large discounts |
| 51.6% of sales are from September to December | Plan your stock and staffing for those months.
| 2017 growth was less profitable | Track margin monthly, not just sales |

## Limitations

- There's no cost column in the dataset so we can't actually confirm the reason for the losses at the high discount levels. The analysis simply shows that discount and loss are moving in tandem, not that one causes the other.
- It's only for the four year period (2014 to 2017) so doesn't really allow you to see any long term trends.
- The loss making products are grouped by Product Name, the best sellers by Product ID and Product Name.

## Project structure

```
.
├── Sample - Superstore.csv
├── Superstore_Sales_Analysis.ipynb
└── README.md
```

## How to run

1. Install the libraries:
   ```bash
   pip install pandas numpy matplotlib jupyter
   ```
2. Ensure that Sample - Superstore.csv is in the same folder as the notebook.
3. In the first data loading cell, change the file path from /content/Sample - Superstore.csv (for Google Colab) to Sample - Superstore.csv.
4. Run all cells.

## Author

Rahul Mishra
