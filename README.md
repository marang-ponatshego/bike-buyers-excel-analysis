# Bike Buyers — Excel Dashboard Analysis

An end-to-end Excel analysis of a customer dataset for a bike retailer,
identifying which customer segments are most likely to purchase a bike.
The final deliverable is an interactive dashboard with slicers for
marital status, region, and education.

**Tool:** Microsoft Excel (pivot tables, slicers, charts, dashboard)
**Dataset:** ~1,000 customer records with demographics, income,
commute distance, and purchase history

---

## Business question

> *Which customer segments should marketing target to increase bike
> purchases?*

The dataset includes both buyers and non-buyers. By breaking down
purchase behaviour by demographics, the goal is to identify the
segments with the highest purchase intent — and the segments that are
currently under-targeted.

---

## Files in this repo

| File | What it is |
|---|---|
| `bike_buyers_raw.xlsx` | Original, uncleaned dataset |
| `bike_buyers_analysis.xlsx` | Completed workbook — cleaning, pivots, and dashboard |
| `screenshots/03-dashboard.png` | Final interactive dashboard |
| `screenshots/02-pivot-table.png` | Pivot table views |
| `screenshots/01-working-sheet.png` | Cleaned working sheet |

---

## Process

### 1. Data cleaning
Standardised the raw data in the `Working Sheet`:
- Converted coded columns (M, S, F) into readable labels (Married, Single, Female, Male)
- Standardised income from shorthand ($40K → $40,000) to numeric
- Created an **Age Brackets** helper column (Adolescent / Middle Age / Old)
  so purchase behaviour could be analysed by age band rather than raw age

### 2. Pivot table analysis
Built pivot tables to answer three questions:
- **Average income per purchase**, split by gender
- **Purchase count by commute distance**
- **Purchase count by age bracket**

### 3. Dashboard
Assembled the pivot results into a single interactive dashboard with
three slicers (**Marital Status**, **Region**, **Education**). All
slicers are wired to all three charts, so filtering one updates the
entire view.

---

## Key findings

### 1. Middle-aged customers dominate purchases
The **Middle Age** bracket shows the highest purchase volume — far
above Adolescents and Older customers. Marketing budget aimed at
this segment is likely to have the highest ROI.

### 2. Gender gap in income — and purchase behaviour
Male customers who purchased had a higher average income (**$60,124**)
than male non-purchasers (**$56,208**). The pattern flips slightly for
women — female purchasers averaged **$55,774** vs. non-purchasers at
**$53,440**. In both cases, buyers had higher average income than
non-buyers.

### 3. Commute distance matters — but not in the obvious direction
The **0–1 mile** commute segment has the highest purchase count
(~200 buyers). This runs counter to the intuition that longer commutes
drive bike purchases. This suggests the target market is **urban,
short-commute customers** — not suburban long-commuters.

### 4. Overall purchase rate: 48%
Of ~1,000 customers, **481 purchased a bike**. The dataset is roughly
balanced between buyers and non-buyers, which makes it ideal for
segment analysis.

---

## What I'd do next

- Test a **logistic regression** or a simple scoring model in Excel to
  predict purchase probability by customer segment.
- Add a **purchase rate** pivot (percentage, not count) to remove bias
  from segments that are simply larger.
- Extend the dashboard with a **regional breakdown** to test whether
  purchase behaviour differs by geography.

---

## Skills demonstrated

- Data cleaning and transformation in Excel
- Helper column creation (`Age Brackets`)
- Pivot table construction and cross-tab analysis
- Interactive dashboard design with slicers
- Chart selection (bar for averages, line for categorical counts)
- Business framing — translating pivots into a targetable insight
