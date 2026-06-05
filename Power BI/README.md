**You can download my Power BI project using this link:**
[Project in Power BI](https://drive.google.com/file/d/10f38uv2rV3KQcuz9yeZxSJsgBJHwdPRM/view?usp=drive_link)

**Tasks that were solved in this file:**
1. Gross Profit: In real business, a "net" figure is rarely provided. Calculate the gross profit per transaction using the formula:
Total - Cogs (if there's no column for this, create one yourself).
2. Average Basket: Find the average check (Total) for each customer type.
3. Weekend vs. Weekday: Create a new column called "Day Type," where if dayofweek >= 5, then "Weekend," otherwise "Weekday." 
Calculate the average receipt on weekends and weekdays.
4. Top 5 Categories: Display the top 5 product lines by total revenue. Add a column with the percentage of total revenue.
5. Profitability: Find the category that generates the highest total profit (use Gross Profit from Task 3).
Hint: Revenue may be high, but profit is low due to discounts or cost price (cogs). Show this difference.
6. City Analysis: Find out which City generates the most revenue (Total) and which city has the highest average customer ratings (Rating).
7. Gender Behavior: Calculate who spends more money over time: Female or Male. And who buys more units of a product (Quantity)?
8. Cross-section (Complex Grouping): Using pivot_table, find the combination of Gender + Customer Type that has the highest median gross profit.
The median is important to eliminate the influence of randomly large checks.
9. Find the correlation (numpy.corrcoef or df.corr()) between Rating (satisfaction) and Gross Profit (profit per customer).
If the correlation is low, this is a business conclusion for the client: "A satisfied customer is not always the most profitable."

**This project used various charts and the following measures:**
1) Correlation between rating & gross profit = 
VAR Avg_rating = AVERAGE('Product Categorywise Sales'[Rating])
VAR Avg_profit = AVERAGE('Product Categorywise Sales'[Gross_Profit])
VAR Sum_product = SUMX('Product Categorywise Sales', ('Product Categorywise Sales'[Rating] - Avg_rating)*('Product Categorywise Sales'[Gross_Profit] - Avg_profit))
VAR Sumsqrt_rating = SUMX('Product Categorywise Sales', ('Product Categorywise Sales'[Rating] - Avg_rating)^2)
VAR Sumsqrt_profit = SUMX('Product Categorywise Sales', ('Product Categorywise Sales'[Gross_Profit] -Avg_profit)^2)
RETURN DIVIDE(Sum_product, SQRT(Sumsqrt_profit*Sumsqrt_rating))
2) Percent_from_total = 
VAR itemtotal = SUM('Product Categorywise Sales'[Total])
VAR commontotal = CALCULATE(SUM('Product Categorywise Sales'[Total]), ALL('Product Categorywise Sales'))
RETURN DIVIDE(itemtotal, commontotal, 0)
3) Top city by average rating = 
VAR Top_city_by_average_rating = TOPN(1, SUMMARIZE('Product Categorywise Sales', 'Product Categorywise Sales'[City], "average rating", AVERAGE('Product Categorywise Sales'[Rating])), [average rating], DESC)
RETURN CONCATENATEX(Top_city_by_average_rating, [City]&":  "&FORMAT([average rating], "#,###,###.#0"))
4) Top city by total revenue = 
VAR Top_city_by_total_revenue = TOPN(1, SUMMARIZE('Product Categorywise Sales', 'Product Categorywise Sales'[City], "total revenue", SUM('Product Categorywise Sales'[Total])), [total revenue], DESC)
RETURN CONCATENATEX(Top_city_by_total_revenue, [City]&":  "&FORMAT([total revenue], "#,###,###.#0 $"))
5) Top group by median profit = 
VAR Top_group = TOPN(1, SUMMARIZE('Product Categorywise Sales', 'Product Categorywise Sales'[Gender],'Product Categorywise Sales'[Customer_type],"Median_profit",MEDIAN('Product Categorywise Sales'[Gross_Profit])), [Median_profit], DESC)
RETURN CONCATENATEX(Top_group, [Gender]&"["&[Customer_type]&"]"&":  "&FORMAT([Median_profit], "#,###.#0 $"))
6) Top product by profit = 
VAR top_product_by_profit = TOPN(1, SUMMARIZE('Product Categorywise Sales', 'Product Categorywise Sales'[Product_line], "total profit", SUM('Product Categorywise Sales'[Gross_Profit])), [total profit],DESC)
RETURN CONCATENATEX(top_product_by_profit, [Product_line]&":  "&FORMAT([total profit], "#,###.#0 $"))
7) Who buys more units of goods = 
VAR Who_buys_more_units_of_goods = TOPN(1, SUMMARIZE('Product Categorywise Sales', 'Product Categorywise Sales'[Gender], "units of goods", SUM('Product Categorywise Sales'[Quantity])), [units of goods], DESC)
RETURN CONCATENATEX(Who_buys_more_units_of_goods, [Gender]&":  "&FORMAT([units of goods], "#,###,###"))
8) Who spends more money = 
VAR Who_spends_more_money = TOPN(1, SUMMARIZE('Product Categorywise Sales', 'Product Categorywise Sales'[Gender], "money spent", SUM('Product Categorywise Sales'[Total])), [money spent], DESC)
RETURN CONCATENATEX(Who_spends_more_money, [Gender]&":  "&FORMAT([money spent], "#,###,###.#0 $"))


