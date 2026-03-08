# Azure-to-Snowflake-Automated-Bi-Directional-Cloud-Data-Pipeline-for-Insurance-Fraud-Claims-Analytics

# Project Summary
This project delivers a fully automated, bi‑directional cloud data pipeline designed to support advanced insurance fraud detection and claims analytics. Built using Azure Blob Storage and Snowflake, the solution demonstrates how modern data engineering practices can transform raw operational data into high‑value analytical datasets that drive real business decisions.

The pipeline ingests raw customer, policy, and claims data from Azure into Snowflake on a scheduled basis, applies robust data modeling and transformation logic, and produces four curated analytical datasets: Fraud Risk Alerts, Claims Cycle Time Summary, Customer Lifetime Value, and Loss Ratio Summary. These curated outputs are then automatically exported back to Azure, enabling downstream analytics, reporting, and integration with BI tools or operational systems.

The system is fully automated end‑to‑end. Snowflake Tasks orchestrate daily ingestion, transformation, and reverse‑ETL exports, ensuring that analytics consumers always have access to fresh, trustworthy data. The project incorporates production‑grade engineering patterns, including storage integrations, scheduled orchestration, SQL‑based data modeling, fraud‑rule logic, and cloud‑native file exports.


# Pipeline Components
**1. Azure → Snowflake Ingestion**

Azure Blob Storage container holds raw CSV files

Snowflake STORAGE INTEGRATION securely connects to Azure

External stage + COPY INTO load raw data into Snowflake tables

A Snowflake Task automates daily ingestion

**2. Curated Analytics Layer (SQL Modeling)**

Four business‑ready analytical views were created:

**✔ Fraud Risk Alerts**

Flags suspicious claims using:

High fraud score

Early claims after policy start

Fast settlements

Long‑pending claims

High‑value claims

Produces a risk category and binary fraud flag

**✔ Claims Cycle Time Summary**

Measures the time between claim filing and settlement

Supports operational efficiency KPIs

Enables trend analysis by region, policy type, and claim type

**✔ Customer Lifetime Value (CLV)**

Computes customer value based on:

Total premiums

Total claims

Tenure

Profitability metrics

**✔ Loss Ratio Summary**

Calculates loss ratios by:

Region

Policy type

Month

Year

Supports financial performance monitoring

**3. Materialized Export Tables**

Each curated view is materialized into a physical table for export.This ensures stable schemas and fast export performance.

**4. Snowflake → Azure Reverse ETL**

Using COPY INTO, each curated table is exported back to Azure Blob Storage:

Compressed .csv.gz files

Organized into analytics folders

Overwritten daily to keep data fresh

This enables downstream BI tools (Power BI, Databricks, Synapse, etc.) to consume analytics‑ready data.

**5. Full Automation with Snowflake Tasks**

A single scheduled task orchestrates:

Refreshing curated tables

Exporting analytics datasets

Writing results to Azure

Runs daily at 02:30 AM GMT.

# Technologies Used

Azure Blob Storage

Snowflake

Storage Integrations

External Stages

COPY INTO

SQL Views

Tasks & Scheduling

SQL (Snowflake dialect)

Cloud Automation

Data Modeling & Analytics Engineering



This work showcases the ability to design and implement a scalable, cloud‑based data platform that bridges technical engineering with real insurance business value. It highlights expertise in Snowflake, Azure, SQL modeling, automation, and the creation of analytics assets that support fraud detection, operational efficiency, and financial performance monitoring.

# Business Value Delivered

This project demonstrates how cloud data engineering can support real insurance operations:

**Fraud Detection**

Early identification of suspicious claims

Rule‑based fraud scoring

Faster investigation workflows

**Operational Efficiency**

Claims cycle time monitoring

Bottleneck identification

SLA performance tracking

**Customer Insights**

Lifetime value segmentation

Profitability analysis

Retention strategy support

**Financial Reporting**

Loss ratio monitoring

Region and policy performance

Executive‑level KPIs
