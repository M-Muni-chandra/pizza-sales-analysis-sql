# 🍕 Pizza Sales Analysis | SQL Data Analytics Project
<img width="1536" height="1024" alt="Pizza sales Dashboard" src="https://github.com/user-attachments/assets/b57617a4-ed56-4519-bc15-c0a28b7ba2bb" />

[![SQL](https://img.shields.io/badge/SQL-MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Live Demo](https://img.shields.io/badge/Live%20Presentation-Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)](https://spiffy-pika-006b5c.netlify.app/)
[![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)]()
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)]()

> An end-to-end SQL analytics project that turns raw pizza sales transactions into actionable business insights — covering revenue trends, customer ordering behavior, and product performance, presented through a custom-built interactive web dashboard.

**🔗 [View Live Presentation](https://spiffy-pika-006b5c.netlify.app/)**

---

## 📌 Table of Contents
- [Project Overview](#-project-overview)
- [Business Problem](#-business-problem)
- [Dataset](#-dataset)
- [Tools & Technologies](#-tools--technologies)
- [Database Schema](#-database-schema)
- [Analysis Approach](#-analysis-approach)
- [Key Business Insights](#-key-business-insights)
- [Recommendations](#-recommendations)
- [Repository Structure](#-repository-structure)
- [How to Run](#-how-to-run-this-project)
- [Connect With Me](#-connect-with-me)

---

## 📊 Project Overview

This project analyzes transactional sales data from a pizza restaurant to answer real-world business questions a data analyst would be expected to solve — from basic order counts to advanced revenue-ranking logic using window functions.

The analysis is structured in three progressive tiers to demonstrate range across SQL proficiency:

| Level | Focus |
|---|---|
| **Basic** | Aggregate functions, filtering, sorting |
| **Intermediate** | Multi-table joins, date/time functions, grouping |
| **Advanced** | Subqueries, window functions (`RANK()`, `SUM() OVER()`), percentage contribution & cumulative analysis |

The final results were translated into a visual, interactive web presentation to communicate findings the way a stakeholder or hiring manager would expect — not just raw query output.

---

## 🎯 Business Problem

Pizza restaurant management needed clarity on:
- Which products drive the most revenue vs. which underperform
- When customers order most (to optimize staffing and marketing spend)
- How order value and size preferences vary
- Where menu and promotional opportunities exist

This project answers those questions purely through SQL querying and data storytelling.

---

## 🗂 Dataset

The dataset consists of four relational tables typical of a restaurant POS system:

| Table | Description |
|---|---|
| `orders` | Order ID, order date, and order time |
| `order_details` | Line-item level quantity per pizza per order |
| `pizzas` | Pizza ID, size, and price |
| `pizza_types` | Pizza name, category, and ingredients |

---

## 🛠 Tools & Technologies

- **SQL (MySQL)** — data querying, joins, aggregation, window functions
- **HTML / CSS / JavaScript** — interactive web-based presentation of insights
- **Netlify** — deployment of the presentation dashboard

---

## 🧩 Database Schema

```
pizza_types (pizza_type_id, name, category, ingredients)
        │
        ▼
   pizzas (pizza_id, pizza_type_id, size, price)
        │
        ▼
order_details (order_details_id, order_id, pizza_id, quantity)
        │
        ▼
   orders (order_id, order_date, order_time)
```

---

## 🔍 Analysis Approach

All 13 business questions were solved using pure SQL — see [`pizza_sales_analysis.sql`](./pizza_sales_analysis.sql) for the full, commented query set.

**Basic**
1. Total number of orders placed
2. Total revenue generated from pizza sales
3. Highest-priced pizza
4. Most common pizza size ordered
5. Top 5 most ordered pizza types by quantity

**Intermediate**
6. Total quantity ordered per pizza category
7. Distribution of orders by hour of the day
8. Category-wise distribution of pizza types
9. Average number of pizzas ordered per day
10. Top 3 pizza types by revenue

**Advanced**
11. Percentage contribution of each pizza type to total revenue
12. Cumulative revenue generated over time
13. Top 3 pizza types by revenue **within each category** (using `RANK() OVER (PARTITION BY ...)`)

---

## 💡 Key Business Insights

- The **Classic category** contributes the largest share of total revenue among all pizza categories.
- A handful of pizza types dominate order volume, while several varieties consistently underperform and occupy menu space without driving sales.
- Order volume peaks at distinct hours of the day, revealing clear lunch/dinner demand windows.
- Meaningful headroom exists to lift **average order value**, indicating an untapped upsell opportunity.

*(Full visual breakdown — revenue trends, category distribution, hourly demand, top/bottom performers — available in the [live presentation](https://spiffy-pika-006b5c.netlify.app/).)*

---

## ✅ Recommendations

- 🍕 Promote best-selling pizzas through combo/bundle offers
- 📈 Increase marketing spend around identified peak ordering hours
- ⚡ Use targeted discounts to boost demand for low-performing pizzas during off-peak hours
- 👥 Introduce a loyalty/rewards mechanism to retain high-frequency customers

---

## 📁 Repository Structure

```
pizza-sales-analysis/
│
├── pizza_sales_analysis.sql     # All 13 SQL queries (basic → advanced)
├── README.md                    # Project documentation
└── dataset/                     # Raw CSV data (orders, order_details, pizzas, pizza_types)
```

---

## 🚀 How to Run This Project

1. Clone the repository
   ```bash
   git clone https://github.com/M-Muni-chandra/pizza-sales-analysis.git
   ```
2. Import the dataset CSVs into your MySQL server (create a database, e.g. `pizza_sales`)
3. Run the queries in [`pizza_sales_analysis.sql`](./pizza_sales_analysis.sql) sequentially in MySQL Workbench or any SQL client
4. Explore the [live presentation](https://spiffy-pika-006b5c.netlify.app/) to see the findings visualized

---

## 📬 Connect With Me

**M Muni Chandra** — Aspiring Data Analyst

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/m-muni-chandra-a64505355/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/M-Muni-chandra)

⭐ If you found this project useful or interesting, consider giving it a star!
