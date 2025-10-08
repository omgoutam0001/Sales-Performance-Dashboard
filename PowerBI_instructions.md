# Power BI Instructions (Blue & White theme)

1. Open Power BI Desktop.
2. Get Data -> MySQL database (or Text/CSV to import CSVs).
3. Use the `sql_queries.sql` as reference for creating views or direct queries.
4. Power Query steps to apply:
   - Change data types (Date, Decimal, Integer).
   - Remove duplicates and nulls.
   - Create calculated column: Total_Sales = Quantity * Unit_Price (if not present).
5. Suggested DAX measures:

Total Sales = SUM(Sales[Total_Sales])

Average Order Value = DIVIDE([Total Sales], DISTINCTCOUNT(Sales[Sale_ID]))

Profit Margin = DIVIDE(SUM(Sales[Profit]), [Total Sales])

6. Recommended visuals and layout (Blue & White):
   - Header: company name + date slicer
   - Top row KPI cards: Total Sales, Total Profit, Unique Customers, Avg Order Value
   - Left column: Filters (Region, Category, Date Range)
   - Center: Line chart for Monthly Revenue
   - Right: Top products bar chart, Map visual for regional revenue
7. Theme colors (example):
   - Primary: #0078D7 (Microsoft blue)
   - Accent: #FFFFFF (white backgrounds)
   - Use white tiles with blue headers and subtle shadows for contrast.
8. Export: File -> Export -> Power BI template (.pbit) to share skeleton without data.
