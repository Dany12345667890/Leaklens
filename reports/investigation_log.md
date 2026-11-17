# LeakLens — Retail Revenue Investigation

## 1. Investigation brief

**Business problem**  
Management needs to understand where reported sales are failing to translate into healthy profit and which patterns deserve investigation.

**Objective**  
Identify and quantify product, discount, regional, and returns patterns associated with weak or negative profitability, then recommend three evidence-backed actions for management to test.

**Primary audience**  
Retail owner and commercial/operations managers.

**Dataset status**  
Sample Superstore dataset. Its an illustrative dataset, not evidence about a real named retailer. Confirm the exact files, fields, date coverage, and data quality during source validation.

## 2. Questions to investigate

1. Which product categories, sub-categories, and products contribute most to total profit and to total losses?
2. How do profit and profit margin vary across discount levels? This is an association analysis, not proof that discounts caused the result.
3. What share of distinct orders is returned, and where are returns concentrated?
4. How do sales, profit, margin, and order volume differ by region and customer segment?
5. Which three management actions are best supported by the evidence?

## 3. KPI definitions

| KPI | Definition | Counting rule |
|---|---|---|
| Sales | Sum of recorded Sales | Sum at transaction-line level |
| Profit | Sum of recorded Profit | Sum at transaction-line level |
| Profit margin | Total Profit divided by total Sales | Calculate from group totals; do not average row margins |
| Orders | Count of distinct Order IDs | Never use raw row count as order count |
| Average order value | Total Sales divided by distinct Order IDs | Order-level denominator |
| Return rate | Distinct returned Order IDs divided by distinct Order IDs | Deduplicate Order IDs after joining Returns |

## 4. Working hypotheses — This is not findings

- Some high-sales products or sub-categories may contribute weak or negative profit.
- Profitability may differ across discount levels.
- Returns may be concentrated in particular product groups or regions.
- Regional performance may differ because of product mix, discounts, or order volume.


## 5. Scope and limitations

- The analysis can describe patterns and associations. It cannot establish causation from this observational dataset alone.
- Do not claim to analyse inventory, stockouts, supplier costs, or advertising effectiveness unless relevant fields are found and validated.
- Regional manager names are descriptive context; do not attribute regional results to an individual manager.

## Stage 1: Initial Data Audit

**Objective**
Assess the structure and initial quality
of the three source tables.
**Results**
- Orders: 10,194 rows, 21 columns.
- Returns: 296 rows, 2 columns.
- People: 4 rows, 2 columns.
- No missing values reported.
- No exact duplicate rows reported.
- Orders contains 5,111 unique orders.

### Analytical observations
- Orders is at product-line grain.
- Order ID is not unique in Orders.
- Returns has unique Order IDs.
- People has four unique regions.

### Outstanding checks
- Validate Returns-to-Orders relationship.
- Validate Orders-to-People relationship.
- Investigate date types and ranges.



## 8. Final recommendations tracker

| Priority | Finding | Supporting evidence | Business implication | Recommended action | Limitation |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
