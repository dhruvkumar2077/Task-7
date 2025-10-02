# 🛒 Task 7 – Sales Summary using SQLite & Python

## 📖 Objective
This project connects **Python with a SQLite database** to pull sales information and generate both **basic** and **advanced summaries** with visualizations.  
The goal is to practice SQL inside Python, perform simple aggregations, and create sales charts.

---

## ⚙️ Tools Used
- Python (3.8+)  
- SQLite (built into Python, no installation needed)  
- Pandas  
- Matplotlib  
- Google Colab / Jupyter Notebook  

---

## 📂 Files in this Repository
- `Sales Summary using SQLite & Python.ipynb` → Jupyter Notebook (main implementation).  
- `sales_data.db` → SQLite database file with sample data.  
- `sales_chart.png` → Revenue by product (bar chart).  
- `sales_summary_table.png` → Tabular output of summary.  
- `README.md` → Documentation (this file).  

---

## 🗄️ Database Schema
**Table: `sales`**

| Column   | Type    | Description                  |
|----------|---------|------------------------------|
| id       | INTEGER | Primary Key (auto increment) |
| product  | TEXT    | Product Name                 |
| quantity | INTEGER | Quantity Sold                |
| price    | REAL    | Price per Unit               |

---

## 📊 SQL Query Used

SELECT
    product,
    SUM(quantity) AS total_qty,
    ROUND(AVG(price),2) AS avg_price,
    SUM(quantity * price) AS revenue
FROM sales
GROUP BY product
ORDER BY revenue DESC

---

## 🔑 Key Insights

🔥 Top Selling Product (by Quantity): Headphones (35 units)

💰 Highest Revenue Product: Laptop (₹424,000)

📈 Phones also contribute significantly with ₹259,500 revenue.

🎯 Headphones, while highest in units, contribute less revenue compared to laptops and phones.
