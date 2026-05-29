# Pizza-Sales-Analysis
## Project Objective
This project analyzes a pizza restaurant's sales data to uncover business insights around revenue, order trends, customer preferences, and product performance. The goal is to help stakeholders make data-driven decisions by presenting key metrics and visual trends in an intuitive dashboard.
## Dataset Used
- <a href="https://github.com/kalappa2003/Pizza-Sales-Analysis-/blob/main/pizza_sales%20(1).csv">Dataset</a>
  
## Dashboard
- <a href="https://github.com/kalappa2003/Pizza-Sales-Analysis-/blob/main/image.png">Dashboard</a>
- <a href="https://github.com/kalappa2003/Pizza-Sales-Analysis-/blob/main/Screenshot%202026-05-29%20151855.png">Dashboards</a>

  
## 📐 KPI Requirements
The following key metrics are calculated across the dataset:

| KPI | Formula | Result |
|---|---|---|
| **Total Revenue** | SUM of all `total_price` | $817.86K |
| **Average Order Value** | Total Revenue / Total Orders | $38.31 |
| **Total Pizzas Sold** | SUM of all `quantity` | 49,574 |
| **Total Orders** | COUNT of distinct `order_id` | 21,350 |
| **Average Pizzas Per Order** | Total Pizzas Sold / Total Orders | 2.32 |


## 📈 Charts & Visualizations

### Home Page Dashboard

| Chart | Type | Insight |
|---|---|---|
| Daily Trend for Total Orders | Bar Chart | Orders peak on **Fridays & Saturdays** |
| Monthly Trend for Total Orders | Line Chart | Highest orders in **July & January** |
| % of Sales by Pizza Category | Donut Chart | **Classic** leads at 26.91% |
| % of Sales by Pizza Size | Donut Chart | **Large** dominates at 45.89% |
| Total Pizzas Sold by Category | Funnel/Bar Chart | Classic > Supreme > Veggie > Chicken |

### Best/Worst Sellers Page

| Chart | Type | Insight |
|---|---|---|
| Top 5 Pizzas by Revenue | Bar Chart | Thai Chicken & BBQ Chicken lead |
| Top 5 Pizzas by Quantity | Bar Chart | Classic Deluxe tops quantity |
| Top 5 Pizzas by Total Orders | Bar Chart | Classic Deluxe tops order count |
| Bottom 5 Pizzas by Revenue | Bar Chart | Brie Carre is lowest revenue |
| Bottom 5 Pizzas by Quantity | Bar Chart | Brie Carre has fewest sales |
| Bottom 5 Pizzas by Total Orders | Bar Chart | Brie Carre has fewest orders |

## 🔍 Key Business Insights

- **Busiest Days:** Orders are highest on **Fridays and Saturdays**
- **Peak Months:** **July and January** see the most orders
- **Top Category:** **Classic** category contributes the most to both sales and total orders
- **Top Size:** **Large** pizzas drive maximum revenue
- **Best Seller (Revenue):** The Thai Chicken Pizza (~$43K)
- **Best Seller (Quantity & Orders):** The Classic Deluxe Pizza
- **Worst Performer:** The Brie Carre Pizza (lowest revenue, quantity, and orders)

## 🗄️ SQL Queries
- <a href="https://github.com/kalappa2003/Pizza-Sales-Analysis-/blob/main/PIZZA%20SALES%20SQL%20QUERIES_SCREENSHOTSS.pdf">sql_queries</a>

All SQL queries are documented in `PIZZA_SALES_SQL_QUERIES.pdf`. Key query categories include:

- KPI calculations (Total Revenue, Avg Order Value, etc.)
- Daily and monthly order trends
- Sales percentage by category and size
- Top 5 and Bottom 5 pizza performers by revenue, quantity, and orders

**Sample Query — Total Revenue:**
sql
SELECT SUM(total_price) AS Total_Revenue 
FROM pizza_sales;

**Sample Query — Top 5 Pizzas by Revenue:**
 sql
SELECT TOP 5 pizza_name, 
       SUM(total_price) AS Total_Revenue
FROM pizza_sales
GROUP BY pizza_name
ORDER BY Total_Revenue DESC;
```


## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **SQL (MS SQL Server)** | Data extraction, aggregation, KPI calculation |
| **Power BI Desktop** | Dashboard creation and visualization |
| **Microsoft Excel / CSV** | Raw data storage |
| **GitHub** | Version control and project sharing |





