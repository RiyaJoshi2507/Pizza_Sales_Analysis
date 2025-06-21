🍕 Pizza Sales Dashboard

📌 Project Description

This end-to-end Pizza Sales project analyzes transactional data from a pizza store to uncover insights into revenue, ordering trends, best-selling pizzas, and sales distribution. The analysis is implemented using SQL, Power BI, Tableau, Excel, and Python. The goal is to help the business optimize inventory, plan marketing campaigns, and increase revenue.

🎯 Objectives

Analyze key business metrics such as total revenue, order count, and best-selling items

Identify high-performing pizza categories and sizes

Understand time-based ordering patterns (hourly, weekly)

Build interactive dashboards using multiple tools for various stakeholders

🛠 Tools & Technologies

SQL Server Management Studio (SSMS) – for querying and metric aggregation

Power BI – for dynamic dashboards

Tableau – for interactive, visual storytelling dashboards

Excel – for static dashboarding and charts

Python (Pandas, Matplotlib, Seaborn) – for programmatic data exploration and visualization

📊 Key KPIs (via SQL)

KPI	Description

Total Revenue	Total income from pizza sales
Average Order Value	Average revenue per order
Total Pizzas Sold	Total number of pizzas sold
Total Orders	Number of distinct customer orders
Average Pizza per Order	Pizzas sold per order (on average)

🔍 Analysis Queries Included

Hourly Trend for Pizza Sales

Weekly Order Volume

Sales % by Pizza Category and Size

Top/Bottom 5 Pizzas by Revenue, Quantity, Orders

Example:

sql

SELECT pizza_category, 
       SUM(total_price) AS total_revenue, 
       SUM(total_price)*100.0 / (SELECT SUM(total_price) FROM pizza_sales) AS pct 
FROM pizza_sales 
GROUP BY pizza_category
ORDER BY pct DESC;

📈 Dashboards

🟢 Power BI Dashboard

Visual KPI cards for revenue, orders, quantity

Slicers by category and size

Hourly & weekly trend charts

Top/bottom performance visuals

🔵 Tableau Dashboard

Visual stories comparing categories and best sellers

Heatmaps and time series trends

Filters for deep-dive analysis

🟠 Excel Dashboard

Pivot-based summaries

Static visualizations for quick reporting

Revenue breakdown by size, category, and pizza name

🐍 Python Analysis

Data cleaning using Pandas

Exploratory Data Analysis (EDA)

Bar plots and line charts using Matplotlib & Seaborn

💡 Key Insights

Top-selling category: Classic pizzas

Best-selling size: Medium pizzas dominate both in volume and revenue

Peak order hours: 6 PM to 8 PM

Top 5 Pizzas account for over 30% of total revenue

Bottom 5 Pizzas can be reviewed for potential removal or improvement

📁 File Structure

sql

/Pizza_Sales_Sql Query.docx        -- SQL queries for KPI and analysis
/Pizza_Sales_report_Dashboard.pbix -- Power BI dashboard
/Pizza sales Report.twbx           -- Tableau workbook
/Pizza_Sales_Dashboard.xlsx        -- Excel dashboard
/Pizza_Sales_python.ipynb          -- Python notebook
/README.md                         -- Project report and summary

🚀 Future Scope

Integrate time series forecasting to predict daily/weekly demand

Add customer segmentation (e.g., high-value vs. low-value orders)

Build a web-based dashboard interface using Flask + Plotly

🙋‍♀️ Author
Riya Joshi
