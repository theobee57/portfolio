## Executive Project Portfolio Performance & Risk (PPM Analytics)
This project demonstrates executive portfolio analytics for an integrated Project Portfolio Management (PPM) environment. The dashboard combines financial performance, delivery risk, and resource capacity to support prioritization and leadership decision-making.

### Executive Project Portfolio Performance & Risk Overview
An integrated dashboard combining financial performance, delivery health, and resource capacity to support executive portfolio decisions.

![Revenue Health/Risk](/images/ppm1_dashboard.png)

### Portfolio Financial Baseline
Executive KPIs establish approved budget, actual spend, remaining headroom, and budget consumption across the portfolio.

![Revenue Health/Risk](/images/ppm2_kpis.png)

### Portfolio Spend Is Concentrated Across a Small Number of Portfolios
A limited set of portfolios account for the majority of approved spend, increasing exposure if delivery performance declines.

![Revenue Health/Risk](/images/ppm3_budget.png)

### Delivery Risk Is Unevenly Distributed Across the Portfolio
Certain portfolios exhibit a disproportionate number of projects behind schedule, independent of total budget size.

![Revenue Health/Risk](/images/ppm4_delivery_risk.png)

### Systemic Resource Pressure Drives Delivery Risk
Multiple roles exceed utilization thresholds during peak execution periods, indicating structural capacity constraints rather than isolated issues.

![Revenue Health/Risk](/images/ppm5_resource_capacity.png)

### High-Value Projects Behind Schedule Require Immediate Attention
Mapping project value against schedule variance highlights where executive intervention can deliver the greatest impact.

![Revenue Health/Risk](/images/ppm6_matrix.png)

## Business Background

CDK Global encountered ongoing challenges in managing financial controls, delivery performance, and resource capacity across multiple projects using the Oracle Cloud Project Portfolio Management (PPM) platform.

Senior leadership needed to address a recurring question.

Where is the portfolio exposed, what causes this exposure, and where should intervention be prioritized?

Without an integrated executive dashboard, CDK Global risks multi-million-dollar losses from unchecked budget overruns and potential schedule delays on key projects. Executives require a dashboard that consolidates budget performance, schedule risk, and resource pressure into a single executive view.

## Business Objectives

The objective was to design a portfolio dashboard that enables leadership to:

1. Understand the overall portfolio financial condition.
2. Identify delivery risk beyond acceptable tolerance.
3. Detect systemic resource capacity pressure.
4. Prioritize high-value projects requiring intervention.
5. Explore risk tolerance scenarios.

## Data Overview

### Core entities

* Projects (portfolio, type, region, planned budget, progress)
* Project budgets (labor and non-labor categories)
* Time-phased actual costs
* Time-phased revenue / value realization
* Resources and roles
* Monthly resource assignments (hours and labor cost)
* Calendar month dimension

Each table was modeled at the appropriate level of detail and linked by logical relationships to prevent duplication and ensure data accuracy.

## Metrics Defined

Total Planned Budget: Sum of approved project budgets across the portfolio.

Actual Cost to Date: Cumulative actual costs recorded for all projects.

Budget Variance: The difference between the approved budget and actual cost.

Budget Consumed: Ratio of actual cost to approved budget.

Schedule Variance: The difference between the actual and planned percent complete.

Delivery Risk Status: Parameter-driven classification of projects based on schedule variance tolerance.

Role Utilization: Ratio of assigned hours to available capacity per role per month.

Capacity Risk Status: Classification of roles as Overallocated, Balanced, or Underutilized based on utilization thresholds.

## Analytical Approach

I applied a layered, validation-first approach to the analysis. Parameters governed analytical logic instead of filtering data, allowing leadership to explore different risk tolerances without recalculating base metrics. My approach included the following steps:

Step 1 - Financial Baseline: Established CFO-approved totals before introducing trends and segmentation.

Step 2 - Delivery Health: Evaluated schedule performance independently from financial indicators.

Step 3 - Resource Utilization: Modeled capacity pressure using explicit, defensible assumptions.

Step 4 - Portfolio Segmentation: Integrated finance, delivery, and resources to expose priority areas.

Step 5 - Executive Assembly: Developed a single-page dashboard for the steering committee.

## Executive Dashboard Design

### KPIs Section

A KPI row provides immediate context, linking each metric directly to a decision. 

KPI 1: Total Portfolio Budget to understand the scope and scale of the financial commitment.

KPI 2: Actual Cost to Date, so we can assess spending efficiency against the planned numbers.

KPI 3: Budget Variance, to identify any immediate financial discrepancies that require attention.

KPI 4: Budget Consumed, so we can evaluate the rate of expenditure relative to budgeted resources and adjust as necessary.

These KPIs address portfolio size and budget utilization efficiency.

### Key Insights Section

Insight 1: Portfolio spend is concentrated in a few portfolios, increasing exposure if delivery issues occur.

Insight 2: Schedule risk is unevenly distributed and does not always correlate with budget size.

Insight 3: Several roles exceed utilization thresholds during peak periods, indicating ongoing capacity pressure.

Insight 4: Several high-budget projects are behind schedule, representing significant delivery risk.

## Recommendations

Based on the analysis, I recommend the following actions.

1. Prioritize high-value, high-risk projects by intervening in projects combining large budgets with negative schedule variance.
2. Manage systemic resource pressure by rebalancing capacity or sequencing work to reduce ongoing role overutilization.
3. Explicitly align risk tolerance by using parameter-driven thresholds to ensure delivery expectations match the organization's risk profile.
4. Maintain portfolio balance by ensuring interventions address both large portfolios and smaller, high-risk areas.

## Why This Project Matters

The dashboard goes beyond reporting isolated metrics and supports leadership decisions in the following ways. By equipping executives with insights that drive confident decision-making, we can envision a future in which leadership accurately steers the portfolio toward strategic objectives, ensuring optimal resource utilization and project success.

* Design trustworthy KPIs. 
* Integrate finance, delivery, and resource data seamlessly.
* Use parameters for scenario-based decision support.
* Communicate portfolio risk clearly and concisely.

## Follow Up

With additional data, I would expand this work by:

* Modeling forecasted Estimate-at-Completion (EAC)
* Analyzing delivery risk by project phase
* Simulating capacity adjustments and schedule impact
* Integrating benefits realization metrics

## Final Note

This project demonstrates my approach to enterprise analytics challenges.

Validate first, integrate carefully, and design dashboards that leaders can act on immediately.

## Design Tools

* Tableau 
*  Parameters 
* Calculated Fields
