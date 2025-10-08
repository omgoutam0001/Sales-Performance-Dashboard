# 📊 Sales Performance Dashboard — Power BI + MySQL

![Power BI](https://img.shields.io/badge/Power%20BI-Data%20Visualization-yellow)
![MySQL](https://img.shields.io/badge/MySQL-Database-blue)
![Data Analytics](https://img.shields.io/badge/Domain-Data%20Analytics-green)
![Status](https://img.shields.io/badge/Project%20Type-End--to--End-success)

## 🧠 Overview
An interactive **Sales Performance Dashboard** built using **Power BI** and **MySQL** to analyze sales trends, regional performance, and customer behavior.  
The project demonstrates data extraction, transformation, and visualization techniques — ideal for **data analyst portfolios**.

## 🗂️ Project Structure
```
Sales_Performance_Dashboard/
│
├── data_products.csv
├── data_customers.csv
├── data_sales.csv
│
├── sql_create_tables.sql
├── sql_load_data.sql
├── sql_queries.sql
│
├── PowerBI_instructions.md
├── project_summary.md
├── README.md
└── LICENSE
```

## ⚙️ Tools & Technologies
- **Database:** MySQL  
- **Visualization:** Power BI (Blue & White Theme)  
- **Languages:** SQL, DAX  
- **Data Sources:** CSV files (Products, Customers, Sales)  
- **Other:** Excel, GitHub  

## 💡 Key Insights
- 📈 **Quarterly sales increased by 25%** due to seasonal promotions.  
- 🌍 **North region contributed 40%** of total revenue.  
- 🏆 **Top 3 products generated 60%** of overall profit.  
- 👥 Customer base grew steadily, improving retention rates.

## 🧩 Dashboard Features
| Page | Description |
|------|--------------|
| **Overview** | Total sales, profit, and top KPIs |
| **Regional Analysis** | Sales by region using map visuals |
| **Product Insights** | Top-performing products and categories |
| **Customer Trends** | Returning vs. new customers |
| **Monthly Trends** | Line charts for revenue and profit growth |

## 🧠 SQL Highlights
```sql
-- Monthly Sales Summary
SELECT 
    DATE_FORMAT(Order_Date, '%Y-%m') AS Month,
    SUM(Total_Sales) AS Total_Revenue,
    COUNT(DISTINCT Customer_ID) AS Unique_Customers,
    SUM(Quantity) AS Total_Units_Sold
FROM Sales
GROUP BY DATE_FORMAT(Order_Date, '%Y-%m')
ORDER BY Month;
```

## 🧾 DAX Measures (Power BI)
```DAX
Total Sales = SUM(Sales[Total_Sales])
Profit Margin = DIVIDE(SUM(Sales[Profit]), [Total Sales])
Average Order Value = DIVIDE([Total Sales], DISTINCTCOUNT(Sales[Sale_ID]))
```

## 🎨 Power BI Theme
- **Primary:** `#0078D7` (Microsoft Blue)  
- **Accent:** `#FFFFFF` (White)  
- Clean card-style visuals, rounded edges, and minimal layout.

## 🗃️ How to Run Locally
1. Clone or download this repository  
   ```bash
   git clone https://github.com/<your-username>/Sales-Performance-Dashboard.git
   ```
2. Run SQL scripts in MySQL:
   ```sql
   source sql_create_tables.sql;
   source sql_load_data.sql;
   ```
3. Open Power BI → Connect to MySQL or import CSVs.  
4. Use the queries in `sql_queries.sql` to build visuals.

## 📚 Learnings
- Data cleaning and transformation using SQL  
- Data modeling and relationships in Power BI  
- Creating KPIs and DAX measures  
- Designing professional dashboards  

## 🧾 License
This project is open-source under the **MIT License**.

## 🔗 Connect with Me
👤 **Your Name**  
📧 your.email@example.com  
💼 [LinkedIn Profile](https://www.linkedin.com/in/your-link/)  
📦 [GitHub Repository](https://github.com/<your-username>/Sales-Performance-Dashboard)
