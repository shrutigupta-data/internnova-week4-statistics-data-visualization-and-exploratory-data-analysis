# Week 4 Assignment: Statistics, Data Visualization & EDA

## Dataset Source
- Original file: ../week2_assignment_internnova/sales_data.csv
- Raw rows: 12
- Raw columns: 9
- Cleaned rows: 12
- Cleaned columns: 10

## Task 1: Mean, Median & Mode
- Mean of Units: 10.92
- Median of Units: 5.50
- Mode of Units: 5.00
- Explanation: The mean shows the average unit count per order. The median shows the middle value and is useful when the data has a wide spread. The mode shows the most common order size in the dataset.

## Task 2: Variance & Standard Deviation
- Variance: 192.63
- Standard Deviation: 13.88
- Explanation: Standard deviation tells us how spread out the values are from the mean. A larger value means the order sizes vary more, while a smaller value means the numbers are closer together.

## Task 3: Correlation & Probability Basics
- Selected variables: Price and Sales
- Correlation coefficient: 0.68
- Relationship: positive (moderate positive)
- Probability example: North orders = 3 / Total orders = 12 = 0.25
- Percentage: 25.0%
- Explanation: The price-to-sales relationship is positive because as the value of the product rises, the sales revenue tends to rise as well. The probability example uses the share of orders from the North region, which is 3 out of 12 orders.

## Task 4: Outlier Detection
- IQR method lower bound: -223.75
- IQR method upper bound: 486.25
- Identified outliers: [{'OrderID': 1001, 'Product': 'Laptop', 'Price': 750}, {'OrderID': 1011, 'Product': 'Laptop', 'Price': 750}]
- Explanation: Outliers are unusually high or low values that can distort the mean and hide true patterns. They should be checked carefully, not automatically removed, because some outliers are valid premium transactions.

## Task 5: Matplotlib Visualization
- Line chart: shows the daily sales trend over time and helps to see how sales change from one date to the next.
- Bar chart: compares total sales by category and shows which category contributes the most revenue.
- Pie chart: displays the share of sales by region and makes regional contribution easy to compare.
- Histogram: shows the distribution of product prices and indicates whether prices are clustered or spread out.
- Scatter plot: compares units sold with sales and helps reveal whether larger order sizes are linked to higher revenue.

## Task 6: Seaborn Visualization
- Count plot: shows how many orders came from each region.
- Box plot: displays the spread and median of product prices by region.
- Heatmap: highlights the strength of relationships between numerical variables.
- Pair plot: helps compare multiple variables at once to find patterns and clusters.

## Task 7: EDA — Data Inspection & Cleaning
### Before cleaning
- Rows: 12
- Columns: 9
- Column names: ['OrderID', 'Date', 'Region', 'Product', 'Category', 'Units', 'Price', 'Salesperson', 'Discount']
- Data types: {'OrderID': 'int64', 'Date': 'str', 'Region': 'str', 'Product': 'str', 'Category': 'str', 'Units': 'int64', 'Price': 'int64', 'Salesperson': 'str', 'Discount': 'float64'}
- Missing values: {'OrderID': 0, 'Date': 0, 'Region': 0, 'Product': 0, 'Category': 0, 'Units': 0, 'Price': 0, 'Salesperson': 0, 'Discount': 1}
- Duplicate records: 0
- Incorrect/inconsistent values: Category had inconsistent text and the Discount column had one missing value.

### Cleaning steps
1. Trim extra spaces from text fields.
2. Standardize category names to a consistent format.
3. Convert the Date column to datetime format.
4. Fill the missing Discount value with the median discount value.
5. Create a Sales column from Units × Price × (1 − Discount).
6. Remove duplicate rows if any are found.

### After cleaning
- Rows: 12
- Columns: 10
- Missing values: {'OrderID': 0, 'Date': 0, 'Region': 0, 'Product': 0, 'Category': 0, 'Units': 0, 'Price': 0, 'Salesperson': 0, 'Discount': 0, 'Sales': 0}
- Duplicate records: 0
- The cleaned dataset was saved to cleaned_sales_data.csv and dataset_after_cleaning.csv.

### Data Summary
```text
       Units   Price  Discount    Sales
count  12.00   12.00     12.00    12.00
mean   10.92  213.17      0.06   625.38
std    13.88  262.69      0.04   376.10
min     1.00    2.00      0.00   100.00
25%     3.75   42.50      0.04   389.25
50%     5.50  132.50      0.05   573.00
75%    10.50  220.00      0.08   816.50
max    50.00  750.00      0.12  1425.00
```

- Before/after cleaning evidence is saved as dataset_before_cleaning.png and dataset_after_cleaning.png in the project folder.

## Task 8: EDA — Correlation & Insights
- The numerical correlation matrix shows that Price and Sales have a positive relationship (0.68), while Units and Sales have a negative relationship (-0.65).
- Products with higher prices can generate more sales revenue even when the order size is not the highest.
- Discounting has a mild relationship with sales, which suggests that discount strategy should be reviewed carefully and not assumed to improve revenue automatically.
- Insight 1: Price is a major factor in sales revenue, so premium products matter.
- Insight 2: Unit volume alone does not guarantee higher revenue because product pricing varies substantially.
- Insight 3: Discounting should be managed strategically, since the effect on revenue is not always positive.

## Task 9: Business Recommendations
1. Focus marketing and stock attention on higher-priced products with strong sales potential, because the data shows a positive relationship between price and sales revenue.
2. Review discount decisions carefully, especially for premium products, because the dataset shows that discounting changes revenue and should not be applied without checking the sales effect.
3. Use the outlier checks to monitor unusual premium orders before making pricing changes, so valid high-value sales do not get mistaken for data problems.

## Conclusion
The original Week 2 sales dataset was inspected, cleaned, and analyzed using statistics, visualizations, and EDA methods. The results show that price, category mix, and discount strategy all influence sales outcomes. The project keeps the analysis simple, transparent, and aligned with the assignment rubric.