# SQL-test-p1

<img width="1200" height="527" alt="image" src="https://github.com/user-attachments/assets/ab5352ca-a750-4583-b034-c9697bda3f99" />

## Q1: In SQL, which clause is used to filter query results based on a condition?  

a) Group by  
b) Order by  
c) Where  
d) Having   

**👉🏼 Answer & Explanation:**  
- `GROUP BY` → groups rows based on column values.  
- `ORDER BY` → sorts the result set.  
- `WHERE` → filters rows **before grouping**.  
- `HAVING` → filters groups (after `GROUP BY`).  

Since the question asks about filtering rows according to a condition, the correct choice is **WHERE**.  

✅ Correct Answer: **c) WHERE**

---

## Q2: Given the Orders table below.  

| order_id  | customer_id    | amount  | order_date  |
|-----------|----------------|---------|-------------|
| 1         | 101            | 500     | 2024-01-01  |
| 2         | 102            | 300     | 2024-01-02  |
| 3         | 101            | 700     | 2024-01-03  |

what is the result of the following query?

```ruby
SELECT customer_id, SUM(amount) as total
FROM Orders
GROUP BY customer_id
```

a) customer_id: 101, total: 1200; customer_id: 102, total: 300  
b) customer_id: 101, total: 500; customer_id: 102, total: 300  
c) customer_id: 101, total: 700; customer_id: 102, total: 300  
d) Syntax error   

**👉🏼 Answer & Explanation:**  
- For customer_id = 101: amounts are 500 + 700 = 1200.  
- For customer_id = 102: amount = 300.  
- The query uses GROUP BY customer_id, which correctly groups and sums amounts.  

✅ Correct Answer: **customer_id: 101, total: 1200; customer_id: 102, total: 300**

---

## Q3: Which JOIN returns **all records from the left table**, even if there are no matching rows in the right table?  

a) INNER JOIN  
b) LEFT JOIN  
c) RIGHT JOIN  
d) CROSS JOIN  

**👉🏼 Answer & Explanation:**  
- **INNER JOIN** → only matching rows.  
- **LEFT JOIN** → all rows from the left table + matching rows from the right (NULL if no match).  
- **RIGHT JOIN** → all rows from the right table + matching rows from the left.  
- **CROSS JOIN** → Cartesian product (all combinations).  

Therefore, the correct answer is **LEFT JOIN**.  

✅ Correct Answer: **b) LEFT JOIN**

---

## Q4: Which Window Function is used to assign a ranking to rows within a partition?  

a) ROW_NUMBER()  
b) COUNT()  
c) SUM()  
d) AVG()  

**👉🏼 Answer & Explanation:**  
- `ROW_NUMBER()` → assigns a unique sequential rank to each row within a partition.  
- `COUNT()` → counts rows, not ranking.  
- `SUM()` and `AVG()` → aggregate functions, not for ranking.  

Therefore, the correct answer is **LEFT JOIN**.  

✅ Correct Answer: **a) ROW_NUMBER()**

---

## Q5: In data analysis, which of the following is **NOT** a measure of central tendency?  

a) Mean  
b) Median  
c) Mode  
d) Standard Deviation  

**👉🏼 Answer & Explanation:**  
- **Mean (Trung bình)** → measure of central tendency.  
- **Median (Trung vị)** → measure of central tendency.  
- **Mode (Giá trị thường xuyên nhất)** → measure of central tendency.  
- **Standard Deviation (Độ lệch chuẩn)** → measure of **dispersion (spread)**, not central tendency.  

✅ Correct Answer: **d) Standard Deviation**

---

## Q6: Which SQL query will return the **top 5 customers with the highest total order amount**?  

a) `SELECT customer_id, SUM(amount) FROM Orders GROUP BY customer_id LIMIT 5`  
b) `SELECT customer_id, SUM(amount) FROM Orders GROUP BY customer_id ORDER BY SUM(amount) DESC LIMIT 5`  
c) `SELECT TOP 5 customer_id, SUM(amount) FROM Orders GROUP BY customer_id`  
d) `SELECT customer_id, MAX(amount) FROM Orders GROUP BY customer_id LIMIT 5`  

**👉🏼 Answer & Explanation:**  

- (a) Groups by `customer_id` but does not sort by total, so it may return any 5 customers.  
- (b) Groups by `customer_id`, calculates total, sorts by total descending, and limits to 5 → correct.  
- (c) Similar to (b) but uses `TOP 5`, which is **SQL Server syntax**, not standard SQL (MySQL/Postgres require `LIMIT`).  
- (d) Uses `MAX(amount)` instead of total, which gives only the largest single order per customer, not total.  

✅ Correct Answer: **b) SELECT customer_id, SUM(amount) FROM Orders GROUP BY customer_id ORDER BY SUM(amount) DESC LIMIT 5**

---

## Q7: When should we use **HAVING** instead of **WHERE** in SQL?  

a) When filtering before `GROUP BY`  
b) When filtering after `GROUP BY` with aggregate functions  
c) When working with `JOIN`  
d) When sorting results  

**👉🏼 Answer & Explanation:**  

- **WHERE** → filters rows **before grouping**.  
- **HAVING** → filters results **after grouping**, often used with aggregate functions (e.g., `SUM`, `COUNT`).  
- JOIN and ORDER BY are unrelated to HAVING’s specific role.  

✅ Correct Answer: **b) When filtering after GROUP BY with aggregate functions**

---

## Q8: In a dataset with a normal distribution, approximately what percentage of the data lies within ±1 standard deviation from the mean?  

a) 50%  
b) 68%  
c) 95%  
d) 99%  

**👉🏼 Answer & Explanation:**  

This comes from the **Empirical Rule (68-95-99.7 rule):**  
- ±1 standard deviation → ~68% of the data  
- ±2 standard deviations → ~95%  
- ±3 standard deviations → ~99.7%  

Therefore, the correct answer is:  

✅ Correct Answer: **b) 68%**

---

## Q9: In SQL, a CTE (Common Table Expression) is used to:  

a) Create a temporary result set that can be reused within the same query  
b) Create an index on a table  
c) Remove duplicate data  
d) Backup the database  

**👉🏼 Answer & Explanation:**  

- A **CTE** is a named temporary result set defined using `WITH`, which can be referenced multiple times within a query.  
- It does not create indexes, remove duplicates, or backup databases.  

✅ Correct Answer: **a) Create a temporary result set that can be reused within the same query**

---

## Q10: Which of the following is **NOT** a method for handling *missing values* in data analysis?  

a) Removing rows with missing values  
b) Replacing with mean/median values  
c) Forward fill or backward fill  
d) Duplicating rows with complete values   

**👉🏼 Answer & Explanation:**  

- (a) Dropping rows with missing values → valid method.  
- (b) Imputing with mean/median → valid method.  
- (c) Forward fill / backward fill → valid method, especially for time series.  
- (d) Duplicating rows with complete values → **not a missing value handling technique**, it distorts the dataset.  

✅ Correct Answer: **d) Duplicating rows with complete values**

---

## Q11: In SQL, the **COALESCE** function is used to:  

a) Concatenate text strings  
b) Return the first non-null value in a list  
c) Convert data types  
d) Calculate the sum of values  

**👉🏼 Answer & Explanation:**  

- (a) Concatenation is done with `CONCAT` or `||`, not `COALESCE`.  
- (b) `COALESCE` returns the **first non-null value** from the list of arguments.  
- (c) Type conversion is done with `CAST` or `CONVERT`.  
- (d) Summation is done with `SUM()`.  

✅ Correct Answer: **b) Return the first non-null value in a list**

---

## Q12: When analyzing revenue trends over time, which metric is most suitable to evaluate the **growth rate**?  

a) Absolute revenue value  
b) Month-over-Month growth rate  
c) Average revenue value  
d) Mode of revenue  

**👉🏼 Answer & Explanation:**  

- (a) Absolute revenue shows the size of sales but not growth.  
- (b) Month-over-Month (MoM) growth rate measures how revenue changes relative to the previous period, which directly reflects growth speed.  
- (c) Average revenue gives overall central value but doesn’t show growth trend.  
- (d) Mode shows the most frequent value, irrelevant for growth.  

✅ Correct Answer: **b) Month-over-Month growth rate**

---

## Q13: In A/B testing, a p-value < 0.05 usually means:  

a) There is no difference between the two groups  
b) The result is statistically significant  
c) More data is needed  
d) The test failed  

**👉🏼 Answer & Explanation:**  

- (a) Incorrect — A low p-value suggests that there *is* a difference unlikely due to chance.  
- (b) Correct — A p-value < 0.05 indicates that the result is **statistically significant**, meaning we reject the null hypothesis at the 5% significance level.  
- (c) Not necessary unless sample size is too small, but p < 0.05 already suggests significance.  
- (d) The test did not fail; it found a significant difference.  

✅ Correct Answer: **b) The result is statistically significant**

---

## Q14: Which SQL statement will find products with revenue higher than the average revenue of all products?  

```ruby
SELECT product_id, revenue
FROM Products
WHERE revenue > ___
```

a) AVG(revenue)  
b) (SELECT AVG(revenue) FROM Products)  
c) AVERAGE(revenue)  
d) SUM(revenue) / COUNT(*)  

**👉🏼 Answer & Explanation:**  

- (a) AVG(revenue) cannot be used directly in WHERE without aggregation.  
- (b) A subquery (SELECT AVG(revenue) FROM Products) correctly computes the average revenue across all products and compares each row’s revenue.  
- (c) AVERAGE() is not a valid SQL function.  
- (d) SUM(revenue)/COUNT(*) would also give the average, but it must be in a subquery; using it directly in WHERE will cause an error.  

✅ Correct Answer: **b) (SELECT AVG(revenue) FROM Products)**

---

## Q15: In data visualization, which chart is most suitable to show the **correlation** between two continuous variables?  

a) Pie chart  
b) Bar chart  
c) Scatter plot  
d) Line chart  

**👉🏼 Answer & Explanation:**  

- (a) Pie chart is for proportions, not correlation.  
- (b) Bar chart is for categorical vs. numeric comparisons.  
- (c) Scatter plot is the best way to visualize the relationship/correlation between two continuous variables by plotting data points on an x-y axis.  
- (d) Line chart is useful for time series trends, not correlation in general.  

✅ Correct Answer: **c) Scatter plot**


