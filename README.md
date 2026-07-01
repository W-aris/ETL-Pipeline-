# 🚀 End-to-End Data Engineering Pipeline with Databricks

An end-to-end Data Engineering project built using **Databricks**, **PySpark**, **Delta Lake**, and **Unity Catalog**. This project implements a scalable ETL pipeline that ingests raw CSV data, transforms it into a dimensional data model, and supports both full and incremental loading for analytical reporting.

---

## 📌 Project Overview

This project demonstrates a modern Data Engineering workflow by building a complete ETL pipeline consisting of:

- Data Ingestion from CSV files
- Data Cleaning & Transformation using PySpark
- Dimension Table Creation
- Fact Table Processing
- Full Load & Incremental Load
- Delta Lake Storage
- Unity Catalog Integration
- Modular Notebook Architecture

The pipeline follows the **Medallion Architecture** and **Star Schema** concepts for efficient data warehousing.

---

## 🏗️ Project Architecture

```
                    CSV Files
                        │
                        ▼
              Databricks Volume
                        │
                        ▼
            Data Ingestion (PySpark)
                        │
                        ▼
             Data Transformation
                        │
        ┌───────────────┴───────────────┐
        ▼                               ▼
 Dimension Tables                 Fact Tables
        │                               │
        └───────────────┬───────────────┘
                        ▼
                  Delta Lake Tables
                        │
                        ▼
                 Analytics & Reporting
```

---

## 📂 Project Structure

```
End_to_End_Data_Engineering/
│
├── 1_setup/
│   ├── setup_catalog
│   ├── utilities
│   └── dim_date_table_creation
│
├── 2_dimension_data_processing/
│   ├── 1_customers_data_processing.ipynb
│   ├── 2_products_data_processing.ipynb
│   └── 3_pricing_data_processing.ipynb
│
├── 3_fact_data_processing/
│   ├── 1_full_load_fact.ipynb
│   └── 2_incremental_load_fact.ipynb
│
└── README.md
```

---

# ⚙️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Databricks | Data Engineering Platform |
| PySpark | Data Processing |
| Delta Lake | Data Storage |
| Unity Catalog | Data Governance |
| SQL | Data Querying |
| Python | ETL Logic |
| DBFS / Volumes | Data Storage |

---

# 📊 Data Pipeline Workflow

### Step 1 — Environment Setup

- Configure Unity Catalog
- Create Schemas
- Initialize Utility Functions
- Create Date Dimension

---

### Step 2 — Dimension Processing

Build all required dimension tables.

- Customer Dimension
- Product Dimension
- Pricing Dimension

Operations performed:

- Data Cleaning
- Null Handling
- Data Validation
- Surrogate Key Generation
- Duplicate Removal

---

### Step 3 — Fact Processing

The project supports two loading strategies.

### ✅ Full Load

- Loads complete dataset
- Used during first execution
- Creates the Fact Table

### ✅ Incremental Load

- Loads only newly arrived records
- Uses Delta Merge Operations
- Prevents duplicate records
- Faster execution

---

# 📁 Execution Order

Run the notebooks in the following order.

## 1️⃣ Setup

```
1_setup/setup_catalog

1_setup/utilities

1_setup/dim_date_table_creation
```

---

## 2️⃣ Dimension Processing

```
2_dimension_data_processing/

1_customers_data_processing

2_products_data_processing

3_pricing_data_processing
```

---

## 3️⃣ Fact Processing

First Run

```
1_full_load_fact
```

Subsequent Runs

```
2_incremental_load_fact
```

---

# ✨ Features

- End-to-End ETL Pipeline
- Modular Notebook Design
- PySpark Transformations
- Delta Lake Storage
- Incremental Data Loading
- Slowly Changing Dimension Support
- Reusable Utility Functions
- Unity Catalog Integration
- Scalable Architecture
- Easy Maintenance

---

# 📈 Data Engineering Concepts Used

- ETL Pipeline
- Data Warehouse
- Star Schema
- Fact & Dimension Modeling
- Incremental Loading
- Full Load Strategy
- Delta Merge
- Data Validation
- Data Cleaning
- Surrogate Keys
- Data Governance
- Partitioning
- Delta Tables

---

# 🚀 How to Run

### Clone Repository

```bash
git clone https://github.com/<your-username>/<repository-name>.git
```

---

### Open Databricks Workspace

Import all notebooks into your Databricks Workspace.

---

### Configure

Update:

- Catalog Name
- Schema Name
- Volume Path
- Source Data Location

---

### Execute Notebooks

Run notebooks sequentially:

```
Setup

↓

Dimension Processing

↓

Fact Processing
```

---

# 📊 Output

The pipeline generates:

- Customer Dimension
- Product Dimension
- Pricing Dimension
- Date Dimension
- Sales Fact Table

All data is stored as **Delta Tables** inside Unity Catalog.

---

# 📸 Project Screenshots

You can add screenshots here.

```
images/

├── architecture.png

├── pipeline.png

├── databricks.png

└── dashboard.png
```

---

# 🔮 Future Enhancements

- Workflow Automation using Databricks Jobs
- CI/CD Pipeline
- Data Quality Monitoring
- Logging Framework
- Streaming Data Pipeline
- Power BI Dashboard
- Azure Data Factory Integration
- Airflow Orchestration

---

# 👨‍💻 Author

**Mohammad Waris**

- Data Engineering Enthusiast
- PySpark | Databricks | SQL | Python

GitHub:
```
https://github.com/W-aris
```

---

# ⭐ If you found this project useful

Please consider giving the repository a **Star ⭐**.
