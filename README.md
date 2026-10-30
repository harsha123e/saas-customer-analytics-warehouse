# SaaS Customer Intelligence & Revenue Analytics Warehouse

## Overview

An end-to-end Data Engineering project that integrates customer activity and subscription billing data from two independent operational databases into a centralized analytical warehouse.

The project demonstrates multi-source data integration, data extraction, warehouse modeling, data quality validation, and analytical SQL using Python, SQLite, and DuckDB.

All datasets are synthetically generated for demonstration purposes.

## Technologies

- Python
- SQLite
- DuckDB
- Pandas
- NumPy
- SQL

## Architecture

```text
Application Database (SQLite) ──┐
                                ├── Python ── DuckDB Warehouse
Billing Database (SQLite) ──────┘                  │
                                                   ▼
                                            Data Validation
                                                   │
                                                   ▼
                                           Dimensional Modeling
                                                   │
                                                   ▼
                                            SQL Analytics
```

## Data Sources

**Application Database**
- Customer accounts
- Users
- Product usage events

**Billing Database**
- Subscription plans
- Subscriptions
- Invoices

## Data Warehouse

The DuckDB warehouse contains:

- **Raw schema:** Extracted source data.
- **Mart schema:** Dimension tables, fact tables, and customer-level analytical tables.

## Analytics

- Subscription and revenue performance
- Monthly Recurring Revenue (MRR)
- Revenue by subscription plan
- Product feature adoption
- Customer engagement by subscription tier
- Payment failure analysis
- Rule-based customer health and churn-risk indicators

## Dataset

- 500 customer accounts
- 3,000 users
- 50,000 product usage events
- 500 subscriptions
- 2,659 invoices

## Run the Project

Open the notebook in Google Colab:

[Open SaaS Analytics Notebook](https://colab.research.google.com/drive/1IB5RbI3AOfopsFc2TaMrVt-CFgkde2ch?usp=sharing)

Run all cells in sequence to generate the source databases, extract and integrate data, build the DuckDB warehouse, perform analytical queries, and generate customer reports.

All data is synthetically generated.
