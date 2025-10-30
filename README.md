# Huawei Billing & CRM Reconciliation System (Billing-Excellency-Project)

## 🎯 Purpose
This project automates the reconciliation of billing data from Huawei’s CBS (Billing System) with CRM records, focusing on customer discount accuracy and KPI adherence. It enhances transparency, ensures correct billing, and supports revenue assurance.

---

## ⚙️ How It Works

### 1. Data Ingestion
- Billing and CRM data are periodically ingested into the on-premises **Cloudera Data Lake** using **Apache NiFi**.

### 2. Reconciliation Logic
- Developed **Hive SQL** scripts to compare billing data against CRM records.
- Each billing record is classified as:
  - ✅ **Matched** – Amounts agree across both systems  
  - ⚠️ **Unmatched** – Mismatch in discount or billing values  
  - 🚫 **CRM Data Not Available** – No corresponding CRM record  
- Logic covers multiple discount types (Promo, Device, Waiver, Employee, Group, Add-on, Rental, and Community Discounts).

### 3. Report Automation
- **Oozie** orchestrates automated reconciliation runs aligned with the billing cycle (three times per month).
- Results are generated in **Excel** and integrated into **Power BI dashboards** for KPI-driven insights.

---

## 🧠 Key Contributions
- Re-engineered reconciliation logic ensuring all discounts in CBS matched CRM configurations.
- Automated workflows with Oozie for end-to-end data validation and reporting.
- Created dynamic Power BI dashboards for business users to identify incorrect billing, obsolete accounts, and excess discounts.
- Led query development, data flow design, and orchestration architecture.

---

## 💥 Impact
- Reduced manual reconciliation time and improved revenue assurance.
- Enabled proactive detection of incorrect billing and obsolete BANs.
- Enhanced customer satisfaction and operational transparency.

---

## 🧰 Tech Stack
**Apache NiFi**, **Hive SQL**, **Oozie**, **Cloudera**, **Excel Automation**, **Power BI**
