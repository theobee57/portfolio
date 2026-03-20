# Revenue Leakage & Billing Efficiency Analysis (SQL)

## Overview

This project analyzes revenue leakage and billing efficiency across an ERP-style project lifecycle using SQL.

The objective is to identify where revenue is delayed, blocked, or lost between cost capture, billing, accounting, and general ledger posting.

The analysis simulates real-world enterprise scenarios commonly encountered in Oracle Cloud PPM / ERP environments.

---

## Business Problem

In project-based organizations, costs are often incurred before billing and accounting processes are completed.

This creates:

- delayed revenue recognition
- reduced financial visibility
- operational inefficiencies

This project answers key business questions:

- How much revenue remains unbilled?
- Where are billing bottlenecks occurring?
- Which transactions are not reaching the general ledger?
- How long are transactions aging before billing?

---

## Dataset

The analysis uses four related tables:

- **projects** — project and organizational data
- **costs** — cost transactions
- **billing** — billing lifecycle status
- **accounting** — accounting and GL posting

These tables simulate real ERP data structures with realistic lifecycle behavior.

---

## Tools & Techniques

- SQL (PostgreSQL-compatible syntax)
- Multi-table joins
- Aggregations and KPI calculations
- Window functions
- Analytical modeling
- DataLab (DataCamp) / DuckDB-based SQL workflow

---

## Analysis Approach

The project is structured into four analytical layers:

### 1. KPI Analysis
- total cost
- total billed
- billing rate
- unbilled exposure

### 2. Exception Analysis
- Draft and On Hold transactions
- billed but not posted to GL

### 3. Aging Analysis
- 0–30 days
- 31–60 days
- 61–90 days
- 90+ days

### 4. Advanced SQL (Window Functions)
- running totals
- project ranking
- benchmarking vs business unit average

---

## Key Insights

### 1. Significant Revenue Remains Unbilled

A portion of cost transactions remains in **Draft or On Hold status**, delaying revenue realization and impacting cash flow.

### 2. Billing Efficiency Varies by Business Unit

Some business units demonstrate lower billing rates, indicating operational inefficiencies or process delays.

### 3. GL Posting Delays Reduce Financial Visibility

A subset of billed transactions has not been posted to the general ledger, creating gaps in financial reporting.

### 4. Aging Risk Concentrated in Older Buckets

Unbilled transactions accumulate in the **90+ day bucket**, increasing the risk of permanent revenue leakage.

### 5. High-Risk Projects Identified via Ranking

Window-function analysis highlights projects with the highest unbilled exposure within each business unit.

---

## Business Recommendations

### 1. Reduce Draft / On Hold Backlog
Prioritize high-value transactions and enforce billing SLAs.

### 2. Improve GL Posting Timeliness
Track billed-but-unposted transactions as a separate KPI.

### 3. Monitor Aging Regularly
Escalate items older than 60–90 days.

### 4. Benchmark Business Units
Use billing efficiency metrics to identify underperforming teams.

### 5. Implement an Exception Control Dashboard
Provide real-time visibility into billing lifecycle issues.

---

## Key Outputs

### KPI Summary

![KPI Summary](visuals/kpi_summary.png)

**Insight:** Billing efficiency varies significantly across business units, indicating inconsistent billing processes and potential operational bottlenecks.

---

### Unbilled Exposure by Business Unit

![Unbilled Exposure](visuals/unbilled_exposure.png)

**Insight:** A disproportionate share of revenue remains unbilled in certain business units, highlighting areas where billing backlog is concentrated.

---

### Aging Analysis

![Aging Analysis](visuals/aging_analysis.png)

**Insight:** A large portion of unbilled transactions falls into older aging buckets (60+ days), increasing the risk of delayed or lost revenue.

---

### GL Posting Exceptions

![GL Exceptions](visuals/gl_exceptions.png)

**Insight:** Some billed transactions have not been posted to the general ledger, creating gaps between operational billing and financial reporting.

---

## Advanced SQL Visualizations

### Running Project Cost (Window Function)

![Running Project Cost](visuals/running_project_cost.png)

**Insight:** Project costs accumulate steadily over time, demonstrating how delays in billing can cause a growing gap between incurred cost and recognized revenue.

---

### Top Ranked Projects by Unbilled Exposure

![Top Unbilled Projects](visuals/top_unbilled_projects.png)

**Insight:** A small number of projects account for a large share of unbilled exposure, suggesting targeted intervention could significantly reduce backlog.

---

### Project Billing Rate vs BU Average

![Billing Rate vs BU Average](visuals/billing_rate_vs_bu_avg.png)

**Insight:** Several projects fall below their business unit’s average billing rate, indicating underperformance and potential process inefficiencies.

---

## SQL Queries

All SQL logic used in this project is available in the `sql/` folder.

Included scripts:

- `schema.sql`
- `kpi_queries.sql`
- `exception_analysis.sql`
- `aging_analysis.sql`
- `window_functions.sql`

These scripts include:
- one-line internal documentation at the top of each query
- business-friendly output aliases
- PostgreSQL-compatible SQL syntax

---

## Project Structure

```text
revenue-leakage-sql-analysis
│
├── README.md
├── QUICK_START.txt
├── data
│   ├── projects.csv
│   ├── costs.csv
│   ├── billing.csv
│   └── accounting.csv
│
├── sql
│   ├── schema.sql
│   ├── kpi_queries.sql
│   ├── exception_analysis.sql
│   ├── aging_analysis.sql
│   └── window_functions.sql
│
└── visuals
    ├── kpi_summary.png
    ├── unbilled_exposure.png
    ├── aging_analysis.png
    ├── gl_exceptions.png
    ├── running_project_cost.png
    ├── top_unbilled_projects.png
    └── billing_rate_vs_bu_avg.png
