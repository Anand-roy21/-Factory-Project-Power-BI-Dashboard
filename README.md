# -Factory-Project-Power-BI-Dashboard
A Power BI report for monitoring factory operations, covering revenue, costs, profitability, and order performance across customers and products.
📊 Dashboard Pages
1. Factory Overview
The main summary page. It gives a quick snapshot of the factory's financial health with the following visuals:
	• KPI Cards — Total Revenue, Total Cost, and Total Profit displayed at a glance, each with a dedicated icon. A secondary card shows Average Order Profit and Profit % Margin.
	• Revenue & Profit Trend (Line Chart) — Plots Total Revenue and Total Profit month-over-month to highlight seasonal patterns and growth.
	• Profit by Customer (Bar Chart) — Ranks customers by total profit contribution. Tooltips show Profit % Margin and total Quantity ordered.
	• Total Quantity Card — Displays the sum of all units ordered.
	• Filters/Slicers — Filter by Product Category, Order Date range, and Customer ID.
2. Product & Order Profitability
A deep-dive into product-level performance:
	• Product Profitability Table — Lists every product with its Total Cost, Total Revenue, Total Profit, and Profit % Margin, sorted by revenue.
	• Profit by Product (Bar Chart) — Visual ranking of products by profit, with quantity as a tooltip.
	• Quantity by Category Card — Shows total quantity sold broken down by product category.
3. Cost & Leakage
Focuses on where costs are being incurred:
	• Total Cost by Customer (Bar Chart) — Identifies high-cost customers to help spot cost leakage.
	• Total Cost by Product (Bar Chart) — Shows which products carry the heaviest cost burden.
	• Filters/Slicers — Filter by Order Date range, Product ID, and Customer ID.

🗄️ Data Model
The report is built on the following tables:
Table	Description
factory_orders	Order-level data — Order ID, Customer ID, Order Date
factory_order_lines	Line-item detail — Product ID, Quantity, Revenue, Cost, Profit per order
factory_customers	Customer master — Customer ID, Customer Name
factory_products	Product master — Product ID, Product Name, Category
Date	Date dimension table used for time-based filtering and drill-downs
Key Measures (in factory_order_lines)
Measure	Description
Total_Revenue	Sum of revenue across all order lines
Total_cost	Sum of costs across all order lines
Total_Profit	Revenue minus Cost
Profit % Margin	Profit as a percentage of Revenue
Avg Order Profit	Average profit per order
Is Complete Month	Helper measure used to exclude the current incomplete month from trend charts


🛠️ Requirements
	• Power BI Desktop — Download here (free)
	• Created using Power BI Cloud (release 2026.01)

🚀 How to Open
	1. Clone or download this repository.
	2. Open Factory_Project.pbix in Power BI Desktop.
	3. If prompted, refresh the data source or update the connection as needed.
	4. Use the slicers and filters on each page to explore the data.

📌 Notes
	• All monetary values are displayed in ₹ (INR).
	• The date range in the data spans from January 2024 through early February 2025.
	• The trend chart on the Overview page automatically excludes the current incomplete month for accurate comparisons.


