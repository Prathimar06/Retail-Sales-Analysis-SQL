# Retail-Sales-Analysis-SQL
# Retail Sales Data Analysis Using SQL

## 📖 Project Summary

This project focuses on analyzing retail sales data using SQL to perform data cleaning, transformation, and business analysis. The objective is to convert raw sales data stored in a CSV file into meaningful insights by applying structured SQL queries. The project demonstrates a practical Business Intelligence and Analyst workflow using SQL as the primary tool.

---

## 📂 Dataset Description

The dataset is provided in CSV format and contains retail sales transaction data. Key columns include:

- Transaction ID
- Sale Date
- Product Category
- Product Name
- Quantity Sold
- Unit Price
- Total Sales
- Customer Information

The raw dataset may contain missing values, inconsistencies, and unstructured records that require cleaning before analysis.

---

## 🛠️ Tools & Technologies

- **Query Language:** SQL  
- **Dataset Format:** CSV  
- **Database:** MySQL / PostgreSQL / SQLite  
- **SQL File:** `Retail_Sales.sql`

---

## 🔄 Project Workflow

### **1. Data Import**
- The CSV dataset is imported into a relational database table.
- Data types are defined appropriately for numeric, date, and text columns.

---

### **2. Data Cleaning Using SQL**
All data cleaning operations are performed directly using SQL queries. This includes:

- Handling missing or NULL values
- Removing invalid records (such as negative quantities or prices)
- Standardizing categorical values (product categories, names)
- Eliminating duplicate records
- Formatting and validating date fields

SQL is used for cleaning to ensure data consistency and maintain a structured analytical workflow.

---

### **3. Data Transformation**
After cleaning, SQL queries are used to:
- Create derived columns such as total sales value
- Aggregate transactional data at category and product levels
- Prepare datasets suitable for business analysis

---

### **4. Data Analysis Using SQL**
The cleaned dataset is analyzed using SQL queries to answer key business questions such as:

- What is the total revenue generated?
- Which product categories contribute the most to sales?
- Which products are top performers?
- How do sales trends vary over time?

---

## 📊 Sample SQL Query

```sql
SELECT product_category, SUM(total_sales) AS revenue
FROM retail_sales
GROUP BY product_category
ORDER BY revenue DESC;
