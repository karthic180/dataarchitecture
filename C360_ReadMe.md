# 🧩 Customer 360 Data Architecture Project

A complete **end-to-end Data Architecture and Data Modelling project** designed to simulate a real-world enterprise Customer 360 system. This project demonstrates **data modelling, ERD design, UML modelling, ETL architecture, and analytics-ready data design**.

---

# 🚀 Project Overview

The Customer 360 system consolidates customer, order, product, and payment data into a unified model to enable:

- 360-degree customer view
- Sales and revenue analytics
- Order lifecycle tracking
- Payment and transaction analysis
- Scalable data warehouse design

---

# 🏗️ Architecture (Medallion Design)

```
Source Systems (API / CRM / ERP)
            ↓
      ETL (Python / Fabric)
            ↓
   Bronze Layer (Raw Data)
            ↓
   Silver Layer (Cleaned Data)
            ↓
   Gold Layer (Star Schema Model)
            ↓
   Power BI / Analytics Layer
```

---

# 🧱 ERD (Entity Relationship Design)

### Core Entities

- Customer
- Address
- Order
- OrderItem
- Product
- Payment

### Relationships

- Customer → Orders (1 to Many)
- Customer → Address (1 to Many)
- Order → OrderItems (1 to Many)
- Order → Payment (1 to 1)
- Product → OrderItems (1 to Many)

---

### ERD Diagram (Text View)

```
Customer ───< Order ───< OrderItem >─── Product
    │             │
    │             └──── Payment
    │
    └───< Address
```

---

# 🧠 UML Class Diagram

This UML model represents the system-level object relationships.

```
+-------------------+
| Customer          |
+-------------------+
| CustomerID        |
| FullName          |
| Email             |
| Phone             |
+-------------------+

        1
        |
        ▼

+-------------------+
| Order             |
+-------------------+
| OrderID           |
| OrderDate         |
| Status            |
| TotalAmount       |
+-------------------+

        1
        |
        ▼

+-------------------+
| OrderItem         |
+-------------------+
| Quantity          |
| UnitPrice         |
+-------------------+

        ▲
        |
+-------------------+
| Product           |
+-------------------+
| ProductID         |
| ProductName       |
| Category          |
| Price             |
+-------------------+

+-------------------+
| Payment           |
+-------------------+
| PaymentID         |
| Method            |
| Status            |
+-------------------+
```

---

# 🧪 Data Model (Star Schema – Gold Layer)

### Fact Table:
- FactSales (Order-level metrics)

### Dimension Tables:
- DimCustomer
- DimProduct
- DimDate
- DimPayment

---

# ⚙️ Technologies Used

- SQL (PostgreSQL / SQLite)
- Python (ETL processing)
- Microsoft Fabric / Azure Concepts
- Power BI (optional visualization layer)
- Draw.io / UML tools for modelling

---

# 📊 Key Features

✔ Customer 360 unified model  
✔ Star schema design for analytics  
✔ Normalized ERD design  
✔ UML class modelling  
✔ ETL pipeline architecture  
✔ Scalable warehouse-ready structure  

---

# 📁 Project Structure

```
customer-360/
│
├── erd/
│   └── customer_erd.png
│
├── uml/
│   └── class_diagram.png
│
├── architecture/
│   └── medallion_architecture.png
│
├── sql/
│   └── create_tables.sql
│
├── etl/
│   └── pipeline.py
│
└── README.md
```

---

# 🎯 Business Value

This system enables:

- Unified customer insights
- Better decision-making through analytics
- Revenue tracking and reporting
- Scalable enterprise data architecture
- Foundation for BI dashboards

---

# 🚀 Future Enhancements

- Real-time streaming integration
- Machine learning customer segmentation
- Data governance & lineage tracking
- Cloud deployment on Azure / AWS
- API-based ingestion layer

---

# 👤 Author

Built by **Data Architect Portfolio Project**  
Focused on Data Engineering, BI, and Data Architecture design principles.
