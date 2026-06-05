**You can view my Excel project online in Microsoft 365 Excel using this link:**
[Project in Excel online](https://1drv.ms/x/c/8f7ed22bb67ac06c/IQAR6hXPsajxQJKynmF3JB5WAfhX18ruPvKGX6O3Bdmj3yM?e=lz56Ku)

**Or you can download this Excel file, but keep in mind that the file must be opened in Excel version 16.0 and in more modern versions of Excel:**
[Project in Excel for download](https://docs.google.com/spreadsheets/d/19fNE1orXL3GQWZwD97zsCKbQr8RGlkcc/edit?usp=drive_link&ouid=104791159130726046761&rtpof=true&sd=true)

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

**The assignments were completed by creating a pivot table and pivot measures for each assignment separately. Each assignment was completed in a new Excel sheet.**
