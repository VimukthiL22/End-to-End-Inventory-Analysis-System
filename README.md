# 📊 End-to-End Inventory Management System (SQL + Power BI)

An enterprise-grade inventory analysis pipeline that maps transactional supply chain data from a localized **MySQL database** into an interactive **Power BI Dashboard**. This system tracks inventory movement, monitors individual warehouse capacities across regional hubs, and flags low-stock scenarios to prevent operational bottlenecks.

---

## 🏗️ Project Architecture

The project is structured into three distinct layers:
1. **Database Layer (MySQL):** Core relational schema configuration, table architecture, and data constraints.
2. **Data Modeling Layer (Power BI Desktop):** Importing data via MySQL connector, configuring an optimized Star Schema, and building robust DAX metrics.
3. **Visualization Layer (Power BI):** Interactive executive layout focusing on operational health, volume trends, and regional distribution.

---

## 🗄️ Database Design & Schema

*The system uses a highly structured relational database named `IMS`. It is optimized to eliminate data redundancy and handle thousands of fast-moving transactional rows.

## The 5 Core Tables:
* `categories`: Groups products into logical segments for clean analytical slicing.
* `suppliers`: Tracks primary manufacturing and procurement contacts.
* `products`: Stores master records including unit costs and custom safety thresholds (`min_stock_level`).
* `warehouses`: Manages distinct physical distribution networks and maximum structural limits (`capacity`).
* `stock_transactions`: The central operational ledger tracking every supply chain inward movement (`Purchase`) and outward velocity (`Sale`).

 ##🔍 Analytical Findings
Demand and Supply Gaps: Granular line analysis captured a clear drop-off in supply chain replenishment between April and November, indicating a critical window where customer orders briefly outpaced stock injections.

High-Velocity Strain: High-velocity stock-out items (such as "Ethernet Cable 10ft" and "Laptop Stand") are unevenly concentrated, creating outsized operational pressure on the Colombo and Jaffna storage centers compared to Kandy.

###🚀 Future Developments
Machine Learning Predictive Forecasting: Integrate a Python or Azure ML extension script into Power BI to predict demand spikes and automatically adjust safety stock margins.

Automated Write-Back Alerts: Develop an automated workflow using Power Automate to text or email specific suppliers the exact moment a product's current stock triggers a Low Stock status.
