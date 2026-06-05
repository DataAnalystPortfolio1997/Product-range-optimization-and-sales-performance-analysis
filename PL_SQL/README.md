**You can view my PL/SQL project online in Oracle FreeSQL using this link:**
[Project in PL/SQL online](https://freesql.com/?compressed_code=H4sIAAAAAAAACq1WXW%252FbNhR9N%252BD%252FcKEXS66zfKB58IJucGO3KNpkXeYg6JNAk1cSUYnUSMqu%252Fv1AUrIt2ym0pAQMWNT9OudeHfJ8DLckp1VODEKqpNZQKplwAyUqMIoITajhUsD4fDgYDmZflosHWM7ef1lYQ1ZRE1NiMJWqHg4IYz5I3AS5f7x7v3gILy8mV9GN9X%252F8Op8tT7n%252Bs1h2Xd%252BBkYbkcAZUpto5n4%252FhAxcMTIZA1qhIikAzpN8hkQqQ0AxMXSLIBGiljSxQNWVrzJGa7W5szSbDAfilZCVYSNZp6FJGk6sIiG5TxC6FNU6ULE6UnipZlbCqu%252BHbim8VWm4JCNwAlXlVCKAkz5FBMCc1LOsSA1fKrhH7ABVS5KUBKWCD%252BB0F00AEcw%252BM1LpXY2bzOTBSu8JgTRTNiLoKry96NGXr9g4o0bglbX9tMhQQGlUJGjJiUEdwBnuPExh9ehpF8AYuI4A%252F4K1FKGD0tFh8XtzPRyeDYq7Rm8xn306YoGA3x7vbXrd1925zQ3SfRrex2x7PuS5zUru%252BGVnCNQSNN%252BRcoA6skx9nhWsUFYKrasYYkHYoNtxkLkKJiqIwtvkyOXDrjHNboc2xg2lkbNsberi6KnZwJzCaTqeT5vfbdDpyDLj3cZPikK9dgPHlxcW5fdxtRSDXqMKWyqby2PIXp7lckTx2hn1I3UczHEjFUNntXTJgqOlwkKChGSRcaQPXoORGgxR5faQQbQowGTGwUlykGrhw7wrygxdV0ZDbKM6LuN3XrC7FB%252FR6k1cS0cl2go%252FLYz6eMk4zoNzUkKJAZb9Hz4HUpp2rPw90kpv6lw1UL%252BXkpu7b859jzIhHl%252FE0Q21250R7IChi7CT8FPFOKbz1kVS43RcA6wboC06CLp3uF1LZvgms3XcHhhf4O3zAguQIUsEdyQ9bmaJgqF7TTJcvthX0ml6f8FXNlLCq6gZtJbjRVgdJmxTCvysiDDd19L%252Bx%252Ftt6duB6nC5TLJM4lZLpF0PdpuiH9lHbQSj5WprYkFWOE0i2CiaLFRfEXb9kAsFHly%252BANxDctuNsj6HAS9zh6BfIOBEn1W28hRfujtBnWGzXM5endu1L0%252F7LZ0gEiIYDj3u%252FBl%252Fzgc7ZIXT7R%252BHtva9TlxX4cHSHxQrVyDoG%252Fn8wgdG9VAXJ%252Fa7%252FH9gaouOTQyqFued9hWaDKCB4cJ9s4O5ewUd3U%252F7qqgm61PphsyEa8ZhA94x46wDt5Xh21G7OzhZ%252F3f4HhBxIm6MLAAA%253D&code_language=PL_SQL&db_version=23&code_format=false)

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

**The tasks were done using formulas such as group by, alter table (add), update (set), pivot, corr, median,  etc.**
