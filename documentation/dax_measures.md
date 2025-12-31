# DAX Documentation – Power BI Sales Project

## 1. Introduction to DAX

DAX (Data Analysis Expressions) is a formula language used in **Power BI**, **Power Pivot**, and **Analysis Services** to create calculated columns, measures, and tables. In this Sales Project, DAX was primarily used to calculate **KPIs**, perform **aggregations**, and enable **dynamic analysis** across dashboards.

This document explains all major DAX measures used in the project, their purpose, and business relevance.

---

## 2. Purpose of Using DAX in This Project

* To calculate total sales, quantity, and profit
* To create dynamic KPIs that respond to filters and slicers
* To analyze performance by region, product, and category
* To support time-based analysis (if date data is available)

---

## 3. Core DAX Measures Used

### 3.1 Total Sales

**Description:**
Calculates the total revenue generated from sales.

**DAX Formula:**

```
Total Sales = SUM(Sales[Sales Amount])
```

**Business Use:**
Used as a primary KPI across all dashboards to evaluate overall business performance.

---

### 3.2 Total Quantity Sold

**Description:**
Calculates the total number of units sold.

**DAX Formula:**

```
Total Quantity = SUM(Sales[Quantity])
```

**Business Use:**
Helps understand product demand and sales volume trends.

---

### 3.3 Total Profit

**Description:**
Calculates total profit earned from sales.

**DAX Formula:**

```
Total Profit = SUM(Sales[Profit])
```

**Business Use:**
Used to assess profitability and financial health.

---

### 3.4 Average Sales

**Description:**
Calculates the average sales value per transaction.

**DAX Formula:**

```
Average Sales = AVERAGE(Sales[Sales Amount])
```

**Business Use:**
Helps analyze customer purchasing behavior.

---

## 4. Time-Based DAX Measures (If Date Column Available)

### 4.1 Sales by Year

**Description:**
Calculates total sales grouped by year using date hierarchy.

**DAX Formula:**

```
Sales by Year = CALCULATE([Total Sales], YEAR(Sales[Order Date]))
```

**Business Use:**
Used in line charts to identify yearly sales trends.

---

### 4.2 Monthly Sales Trend

**Description:**
Calculates monthly sales performance.

**DAX Formula:**

```
Monthly Sales = CALCULATE([Total Sales], MONTH(Sales[Order Date]))
```

**Business Use:**
Helps identify seasonality and monthly performance variations.

---

## 5. Filter & Context-Based Measures

### 5.1 Regional Sales

**Description:**
Calculates sales dynamically based on selected region.

**DAX Formula:**

```
Regional Sales = CALCULATE([Total Sales], VALUES(Sales[Region]))
```

**Business Use:**
Supports region-based filtering and analysis.

---

## 6. DAX Functions Used

The following DAX functions were used throughout the project:

* `SUM()` – Aggregation of numeric values
* `AVERAGE()` – Mean calculation
* `CALCULATE()` – Context modification
* `VALUES()` – Filter context handling

---

## 7. Conclusion

DAX played a critical role in transforming raw sales data into meaningful insights. The measures created in this project enabled dynamic analysis across multiple dimensions such as **time**, **region**, **product**, and **category**, strengthening the overall effectiveness of the Power BI dashboards.

This DAX implementation demonstrates a strong foundation in **Power BI analytics** and **business intelligence concepts**, suitable for academic evaluation and entry-level data analyst roles.

---

**Prepared by:** Md Amshar
**Project:** Power BI Sales Analysis
**Tool:** Microsoft Excel & Microsoft Power BI
