**Problem: The company operates in three cities but doesn't understand why profits vary.
The marketing department doesn't know which customers to focus on (men/women, locals/tourists),
and the purchasing department isn't sure which product categories are truly profitable
and which are just breaking even.**

**Purpose of the analysis:**
1. Which city is the most profitable? (The regional development department wants to open new stores there).
2. Which product category generates the most revenue and margins? (Needed for negotiations with suppliers).
3. Which gender and type of customer spends the most? (For advertising targeting).
4. Does the average order value vary depending on the day of the week or time of day? (For promotional planning).

[Data link](https://drive.google.com/file/d/1N0Ytb9EyvD0gvGG1miRP8rFl81id7SBj/view?usp=drive_link)

**I made this project in 4 platforms:**
1. Excel (power query, pivot table, DAX measures, excel functions)
2. PL/SQL
3. Python (numpy, pandas)
4. Power BI (charts, DAX measures)

**Data cleaning, duplicate removal, and other processes were performed in PowerQuery on the original dataset. All programs use the pre-processed dataset.**

**Conclusions drawn from the data analysis:**
1. The highest average bill is for Member Customer type.
2. The average bill on weekends is higher than on weekdays.
3. The top 5 product lines are: Food and beverages, Sports and travel, Electronic accessories, Fashion accessories, and Home and lifestyle.
   Their total revenue is $273,773.59, which accounts for 84.76% of total revenue.
4. The product category that generates the highest profit is Food and beverages. Correlation between total profit and total revenue by product category = 0.99.
5. Naypyitaw City generates the most revenue and has the highest average customer rating.
6. Over the entire period, women spent more money and purchased more items.
7. Normal female Customer types generated the highest median profits.
8. The correlation between average customer ratings and the profit they generate is -0.0364 (there is no relationship between these metrics).
   This means that a satisfied customer is not always the most profitable.
