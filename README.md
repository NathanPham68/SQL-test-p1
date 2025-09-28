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
d) Lỗi cú pháp   

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
















