# Revenue Leakage & Billing Efficiency Analysis (SQL)

## Overview

This project uses SQL to analyze revenue leakage and billing efficiency across an ERP-style project billing lifecycle. The goal is to identify where revenue is getting delayed, blocked, or lost between cost capture, billing, accounting, and GL posting.

It is designed to simulate the type of enterprise analysis performed in Oracle Cloud PPM / ERP environments.

---

## Business Problem

In project-based organizations, costs may be incurred on time while billing and accounting lag behind. This creates revenue leakage, delayed invoicing, and weak financial visibility.

This project answers questions such as:

- How much value is still unbilled?
- Which business units have the highest billing leakage?
- Where are transactions getting stuck in Draft or On Hold status?
- Which billed transactions have not yet been posted to GL?
- What is the aging profile of unbilled costs?

---

## Dataset

This project includes four related tables:

### 1. `projects.csv`
Project master data:
- `project_id`
- `project_name`
- `business_unit`
- `legal_entity`
- `project_type`
- `project_status`
- `manager_name`
- `customer_name`
- `start_date`

### 2. `costs.csv`
Cost transactions captured against projects:
- `cost_id`
- `project_id`
- `cost_date`
- `cost_type`
- `cost_amount`
- `cost_status`
- `billable_flag`

### 3. `billing.csv`
Billing lifecycle status for each cost transaction:
- `billing_id`
- `cost_id`
- `project_id`
- `billing_status`
- `billed_amount`
- `billed_date`
- `invoice_status`

### 4. `accounting.csv`
Accounting and GL posting outcomes:
- `accounting_id`
- `cost_id`
- `project_id`
- `accounting_status`
- `gl_posted_flag`
- `accounting_date`

---

## Tools Used

- SQL
- CSV datasets
- ERP / Oracle-style business logic
- Relational joins
- Aggregations
- Window functions

---

## Analysis Approach

The project is organized into SQL scripts covering:

### KPI Queries
Core business metrics such as:
- total cost amount
- total billed amount
- billing rate
- unbilled exposure by business unit

### Exception Analysis
Identification of:
- billed transactions not posted to GL
- Draft and On Hold transactions
- projects with highest exception volume

### Aging Analysis
Breakdown of unbilled cost into aging buckets:
- 0–30 days
- 31–60 days
- 61–90 days
- 90+ days

### Window Functions
Advanced SQL techniques used to:
- calculate running project cost
- rank projects by unbilled exposure
- compare project billing rate to business-unit average

---

## Key Insights You Can Expect

Typical findings from this dataset include:

- A meaningful share of cost is trapped in Draft or On Hold billing status
- Some business units carry much higher unbilled exposure than others
- A subset of billed transactions remains unposted to GL, creating accounting delays
- Older transactions accumulate disproportionately in the 90+ day bucket
- Window functions reveal which projects are outliers within each business unit

---

## Business Recommendations

Based on the analysis, likely recommendations include:

### 1. Reduce Draft / On Hold Backlog
Prioritize high-value stuck transactions and define SLA targets for billing completion.

### 2. Monitor GL Posting Delays
Track billed-but-unposted transactions separately to improve accounting transparency.

### 3. Escalate Aged Unbilled Costs
Review 90+ day items regularly to prevent revenue leakage from becoming permanent.

### 4. Benchmark Business Units
Use billing rate and exception volume to identify underperforming teams.

### 5. Create an Exception Dashboard
Turn these SQL outputs into a Tableau or Power BI dashboard for finance and operations leadership.

---

## Project Structure

```text
revenue-leakage-sql-analysis
│
├── README.md
├── data
│   ├── projects.csv
│   ├── costs.csv
│   ├── billing.csv
│   └── accounting.csv
│
└── sql
    ├── schema.sql
    ├── kpi_queries.sql
    ├── exception_analysis.sql
    ├── aging_analysis.sql
    └── window_functions.sql
```

---

## Portfolio Value

This project demonstrates:

- multi-table SQL analysis
- joins across ERP-style datasets
- aggregation and KPI logic
- exception detection
- aging analysis
- window functions
- business-focused interpretation of SQL outputs

---

## Suggested Next Step

A strong extension of this project would be to load the SQL outputs into Tableau and create a:
- Revenue Leakage Dashboard
- Billing Efficiency Scorecard
- Exception Control Tower

That would create a very strong SQL + Tableau portfolio combination.
