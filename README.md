# Billing-Excellency-Project
Huawei Billing & CRM Reconciliation System

Purpose:
This project automatically reconciles billing records from Huawei’s billing system with CRM data, focusing on customer discounts. It ensures accuracy, transparency, and adherence to KPIs defined by the customer.

How It Works
1. Data Ingestion

Billing and CRM data are periodically dumped into a Cloudera Data Lake using Apache NiFi.

2. Reconciliation Logic

SQL/HiveQL scripts compare billing data with CRM records, focusing on multiple discount types.

Each record is classified as:

Matched: Amounts agree in both systems

Unmatched: Data mismatch found

CRM Data Not Available: No matching CRM record

3. Report Automation

Results are batched and saved as Excel reports via Oozie workflow orchestration.

Reports are fed into Power BI dashboards for automated KPI monitoring.

Discount Types Covered
Promo Discounts

Device Discounts

Waivers (Termination, Plan, Fee)

Employee/Group Discounts

Shared Child/Business Lines

Add-on Discounts

Rental Discounts

Community Discounts

Each type uses custom logic for matching, usually joining and aggregating data from both billing and CRM dumps.

Community Discounts

Each type uses custom logic for matching, usually joining and aggregating data from both billing and CRM dumps
