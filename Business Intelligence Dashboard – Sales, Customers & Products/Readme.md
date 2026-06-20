# Business Intelligence Dashboard – Unified Report

This project showcases a full-scale interactive Power BI dashboard built on top of a custom SQL Data Warehouse, visualizing core business insights across sales, customer behavior, and product performance.

🔗 **Explore the Interactive Report:** 
https://app.powerbi.com/view?r=eyJrIjoiYjFhMGNjZjQtYjg3Ny00ZjY1LWE1NWMtMWNmMjhiYjExZDg1IiwidCI6IjI3ZDllYmQwLWYyZjktNGFhMy1iNmY5LWM2ZDAzODI4NjEyNyJ9&pageName=42bb617d3c30d079deb2

**Built With:** Power BI | SQL Server | DAX | T-SQL

---

## Project Overview

This unified Power BI report was developed as part of a complete business intelligence workflow starting from data modeling to dashboard design. It features a centralized landing page with navigation buttons that allow users to explore different analytical views.

### Key Objectives:
- Load, clean, and model raw data using a **medallion architecture** (Bronze → Silver → Gold)
- Create a star schema to support dimensional analysis
- Design a fully navigable and interactive Power BI dashboard
- Answer 25+ real-world business questions with visual insights

---

## 📂 Dashboard Sections

Each report section is accessible via a central landing page:

- **Customer Report**
  - Customer segments (VIP, Regular, New)
  - Average monthly spend & order value
  - Age groups, gender distribution, country-level trends

- **Product Performance**
  - Product segment classification (High / Mid / Low)
  - Revenue by product category and subcategory
  - Cost analysis and quantity distribution

- **Sales Trends**
  - Cumulative sales over time
  - Monthly and yearly revenue trends
  - Moving average of prices

- **KPI Summary**
  - Total revenue, customers, orders, products
  - Average order value and average monthly revenue

- **Landing Page**
  - Navigation panel
  - LinkedIn / GitHub links
  - Quick access to each report section

---

## Technologies Used

- **Microsoft SQL Server**: Data cleaning, transformation, and modeling using T-SQL
- **Power BI Desktop**: Data visualization, DAX, dynamic navigation
- **GitHub**: Version control and code sharing
- **Data Lakehouse Structure**: Bronze (raw), Silver (cleaned), Gold (analytics)

---

## Sample Business Questions Answered

- **What is the total sales by year and by month?**  
  - Sales grew steadily from $4.3K in 2010 to a peak of *$16.3M* in 2013
  - From Jan 2010 to Jan 2014, sales showed a consistent upward trend.The highest monthly sales of *$5.3M* occurred in Q4 2013,
    indicating a seasonal sales spike.
  
- **How do yearly product sales compare to the previous year (YoY analysis)?**
  - 2013 was the strongest YoY performer, with many products growing by over 20,000%
    compared to 2012.
  - 2014 saw a sharp decline of over 90% YoY — driven by partial data and end of trend.
    Most products performed above their multi-year average only in 2013.
    
- **Who are the top 10 revenue-generating customers?**
  - The top 10 customers each contributed over $12,000 in sales, led by Nichole Nara
    and Kaitlyn Henderson. These high-value customers are excellent candidates for loyalty
    programs or personalized offers.
    
- **Which product categories contribute most to revenue?**
  - *Bikes* account for **96.46%** of total revenue, clearly leading the product portfolio.
    *Accessories* contribute **2.38%**, while *Clothing* makes up only **1.16%**.
  - This significant imbalance highlights a possible over-dependence on a single
    category and may warrant diversification strategies or category-specific marketing.
    
- **What are the best and worst performing products?**
  - The best product is *Mountain-200 Black - 46* generated **$1.37M** Belongs to *Bikes* Category.
  - And The product with the Lowest Performance is *Racing Socks and Patch Kit* generated less than **$10,000** in total revenue,
    indicating low traction.
---

## Screenshots
<img width="768" height="960" alt="Image" src="https://github.com/user-attachments/assets/8ccdd715-fdc6-4f33-b6aa-13827c3aea6e" />
<img width="768" height="960" alt="Image" src="https://github.com/user-attachments/assets/971a7761-5856-4c22-a795-7e5db12d06c2" />
<img width="768" height="960" alt="Image" src="https://github.com/user-attachments/assets/ed0f9c74-2539-4826-9b1e-88d30ecf8709" />
<img width="768" height="960" alt="Image" src="https://github.com/user-attachments/assets/dbfcd8aa-9339-44c8-bbac-9a6da37f6865" />
<img width="768" height="960" alt="Image" src="https://github.com/user-attachments/assets/01d648e3-366d-4246-ad7d-c1c07eeafc71" />
<img width="768" height="960" alt="Image" src="https://github.com/user-attachments/assets/f9dff4fc-a47d-461f-b23f-20fcb0541f1e" />

## Acknowledgement

This project is inspired by the 30-Hour SQL Bootcamp by **Data With Baraa**.  
It helped me deepen my knowledge of SQL, advanced analytics, and professional reporting in Power BI.

---

## Connect with Me

- **LinkedIn:** [Mayuresh Chourikar](https://www.linkedin.com/in/mayureshchourikar)
- **GitHub:** [Mayuresh200](https://github.com/Mayuresh200)
- **Email:** [mayureshchourikart@gmail.com]

---

> 📁 Clone or download this project to explore the `.pbix` file, see the data model, or examine the DAX measures and visuals.

