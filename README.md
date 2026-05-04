# Account Statistics Dashboard
**Power BI | DAX | Power Query | Financial Services Analytics**

A two-page interactive Power BI report built to surface actionable insights for credit union leadership. The dashboard analyzes 100,000 account records across five Texas regions spanning January 2024 to April 2026, covering eight product categories, nine member age groups, and 87 ZIP codes. Every visual was intentionally placed to answer a different business question — no two visuals repeat the same story.

---

## The Business Problem

Credit unions and financial institutions need to answer three questions every month:

- **Where are we growing?** Which regions, ZIP codes, and products are gaining members
- **Where are we losing?** Which segments have high closure rates or negative net growth
- **Who are our members?** How do different age groups behave across products and channels

This dashboard answers all three at the ZIP level, the product level, the age group level, and over time with the ability to drill into any combination using slicers and filters.

---

## Screenshots

> All screenshots are filtered to the **Lending** major category for visual clarity. The dashboard supports full cross-filter across all 8 product categories, 5 regions, and 28 months.

### Page 1 — Accounts Statistics

**Visual 1 — Account Analysis by ZIP**
Top N ZIP codes by accounts opened and closed (stacked bars by product), plus a diverging net growth bar chart showing top 5 growing ZIPs (green) and top 5 declining ZIPs (red). Major = Lending, Top N = 5.
![Account Analysis by Zip](screenshots/page1_zip_analysis.png)

**Visual 2 — Accounts Opened vs Closed by Age Group**
Butterfly bar chart showing opened vs closed per age bracket, with product breakdown panels below showing which lending products are driving opens and closes per demographic segment.
![Age Group Analysis](screenshots/page2_age_group.png)

**Visual 3 — Product Growth and YOY Monthly Matrix**
Stacked bar chart ranking all lending products by total opened and closed, with a net growth line overlaid. Below it is a scrollable YOY matrix showing month-by-month account counts and percentage change vs prior year per product. YOY% is blank for 2024 months as no prior year data exists — this is correct behavior, not missing data.
![Product Growth](screenshots/page3_product_growth.png)

---

### Page 2 — Trend Analysis (Line Charts View)

The Trend Analysis page has a **bookmark-driven toggle** at the top — clicking Line Charts shows visual trend lines, clicking Grid Charts replaces every chart with a precise data table. Both views use the same slicers and time buttons so the numbers always match.

**Visual 4 — Opened vs Closed by Month**
Three trend lines over 28 months: Accounts Opened (green), Accounts Closed (yellow), Net Growth (orange). The green line trending upward into 2026 with a stable gap above the yellow line shows healthy and growing portfolio momentum for the Lending category. Time button set to 3Y.
![Trend Analysis Line Charts](screenshots/page4_trend_line.png)

**Visual 5 — Accounts Opened and Closed by Age Group Over Time**
Two side-by-side line charts tracking Under 40 (light blue), 40 to 60 (dark blue), and 60 plus (orange) monthly. Under 40 dominates both opens and closes and shows a clear upward trajectory into early 2026, confirming younger members are the fastest-growing lending segment.
![Age Group Trend](screenshots/page5_age_trends.png)

**Visual 6 — Product Growth Over Time**
Monthly accounts opened per lending product overlaid on a single chart. Shows which products are gaining momentum and which are flattening. The Flex Credit Reserve orange spike in early 2026 is a notable outlier worth investigating for a targeted campaign opportunity.
![Product Growth Over Time](screenshots/page6_product_over_time.png)

**Visual 7 — Monthly Opened vs Closed by Product**
Monthly net flow (opened minus closed) per product per month. Lines fluctuate around 40 to 90 range showing consistent monthly activity across all 5 lending products with no product consistently dipping toward zero.
![Monthly Net Flow](screenshots/page7_monthly_net_flow.png)

---

### Page 2 — Trend Analysis (Grid Charts View)

Clicking the **Grid Charts** button activates the bookmark and replaces all line charts with four precise data tables. This view is designed for analysts and stakeholders who need exact numbers rather than visual trends. The same slicers, time buttons, and filters apply so the numbers shown match exactly what the line charts represent.

**Grid Table 1 — Opened vs Closed by Month** shows monthly totals with a Net Growth column — useful for reconciliation and monthly reporting.

**Grid Tables 2 and 3 — Accounts Opened and Closed by Age Group** show month-by-row, age bucket (Under 40, 40 to 60, 60 plus) by column with row totals — directly usable in executive reports without exporting.

![Grid Charts Top](screenshots/page8_grid_charts.png)

**Grid Table 4 — Product Growth Over Time** and **Grid Table 5 — Monthly Opened vs Closed by Product** show the same product-level data from the line charts as precise numbers per month per product with column totals. Express Auto Finance leads with 24,962 total opens across the period.

![Grid Charts Products](screenshots/page9_grid_charts_products.png)

---

## Dashboard Pages

### Page 1 — Accounts Statistics

**Slicers:** Month | Region | Major Product Category | Product
**Reset Button:** Top right corner resets all slicers to default

---

#### Visual 1 — Account Analysis by ZIP (Top N)

A dynamic Top N slicer (default 5, adjustable) surfaces the best and worst performing ZIP codes by accounts opened and accounts closed side by side as stacked bar charts, broken down by product within each ZIP.

Below these sits a diverging bar chart showing Net Growth by ZIP with green bars for positive growth and red bars for negative. This combination tells leadership exactly which geographic pockets are growing and which are declining without needing to scroll through a table.

**Business value:** Branch managers can identify underperforming ZIP codes for targeted outreach campaigns. Marketing can allocate direct mail budgets to high-growth ZIPs to accelerate momentum.

---

#### Visual 2 — Accounts Opened vs Closed by Age Group

A horizontal butterfly bar chart showing opened vs closed accounts per age bracket from under 10 through 80 plus. The gap between the two bars is the net growth story per demographic.

Below it sit two product breakdown charts showing which specific products are driving opens and closes within each age segment.

**Why three visuals instead of one:** The top chart answers how many. The bottom two answer what products and in which direction. Together they form a complete demographic picture that a single chart cannot.

**Business value:** A credit union can see that ages 20 to 39 drive the highest loan volume while ages 60 plus carry the highest average balances. This directly informs which products to cross-sell to which segments and where to focus member retention efforts.

---

#### Visual 3 — Product Growth and YOY Monthly Matrix

A ranked stacked bar chart showing total accounts opened and closed per product with a net growth line overlaid. Products are sorted by total volume so the highest-performing products are immediately visible.

Below it is a scrollable Year over Year matrix showing monthly opened counts per product from January 2024 onward.

**YOY columns explained:**
- YOY Number = raw account count for that month
- YOY Percent = percentage change vs same month prior year
- YOY Percent is blank for 2024 months because there is no 2023 equivalent to compare against. Starting January 2025 the percentage change vs January 2024 is calculated and displayed. This is intentional and correct behavior, not missing data.

**Business value:** Product managers can spot which products are growing year over year and which are plateauing. A declining net growth line on a high-volume product is an early warning signal for intervention.

---

### Page 2 — Accounts Trend Analysis

**Slicers:** Region | Major Product Category | Product
**Time Buttons:** YTD | 1Y | 3Y | 5Y | Max
**View Toggle:** Line Charts | Grid Charts (bookmark-driven)
**Reset Button:** Top right corner resets all filters

---

#### The Line Charts and Grid Charts Toggle

This is the most important UX feature in the report. A bookmark button at the top of the page switches the entire view between two modes.

**Line Charts mode** shows trend lines for visual pattern recognition — useful for spotting growth trajectories, seasonal dips, and product divergence over time.

**Grid Charts mode** replaces every chart with a precise data table showing the exact same information as numbers. This is for when a stakeholder asks for the exact number in a specific month — the answer is one click away without leaving the page or opening a separate report.

This design means the dashboard serves two audiences simultaneously: executives who want to see the trend and analysts who need the exact figure.

---

#### Visual 4 — Opened vs Closed by Month

Three lines tracked over the full date range: Accounts Opened (green), Accounts Closed (yellow), Net Growth (orange). The gap between opened and closed lines represents the health of the portfolio at any point in time.

**Business value:** A narrowing gap between opened and closed is an early warning that growth is slowing before it turns negative. Leadership can see this months before it shows up in a quarterly report.

---

#### Visual 5 and 6 — Accounts Opened and Closed by Age Group Over Time

Three age category lines (Under 40, 40 to 60, 60 plus) tracked monthly on both the opened and closed sides. Comparing these two charts side by side reveals which age groups have rising closure rates even when their open counts look healthy.

**Business value:** If the 40 to 60 segment shows rising closures alongside flat opens, that is a retention problem in the credit union's most valuable balance-holding demographic. This visual catches that signal early.

---

#### Visual 7 — Product Growth Over Time

All lending products overlaid on a single line chart showing monthly accounts opened per product per month. Useful for identifying which products are gaining momentum and which are flattening. The Flex Credit Reserve spike in early 2026 is an outlier worth investigating — a sudden surge in a single product month signals either a successful campaign or a data event worth reviewing.

---

#### Visual 8 — Monthly Opened vs Closed by Product

Net position per product per month. When a product line dips below zero it means more accounts closed than opened that month, which is an immediate alert for the product team.

---

#### Grid Charts View

When Grid Charts is active all eight visuals become precise data matrices:

- Opened vs Closed by Month table with Net Growth column
- Accounts Opened by Age Group matrix (month by age bucket with totals)
- Accounts Closed by Age Group matrix
- Product Growth Over Time matrix (month by product)
- Monthly Opened vs Closed by Product with net values

---

## Key Insights the Dashboard Surfaces

**Digital and Lending products are the growth leaders**
Account openings in lending and digital categories have grown consistently from January 2024 through April 2026. Close rates in these categories remain lower than mortgage and equity products indicating strong member retention post-acquisition.

**Ages 20 to 39 drive volume, ages 60 plus drive balance**
The 20 to 39 cohort opens the most accounts but carries lower average balances. The 60 plus cohort opens fewer accounts but holds significantly higher balances per account. A wealth management or IRA cross-sell campaign targeting 55 to 65 year olds at the moment of loan payoff would have high revenue impact.

**Rural ZIP codes show negative net growth**
Several rural Texas ZIP codes consistently appear in the bottom five net growth ZIPs. These are candidates for a digital-first service model rather than continued branch investment.

**Mortgage and equity accounts have the highest closure rates**
This is consistent with a high interest rate environment. Members are paying off or refinancing out of these products faster than new originations can replace them. A rate-alert or refinance-trigger campaign would directly address this trend.

**The Under 40 segment is the fastest growing demographic**
Under 40 account openings show a clear upward trend from mid-2024 through early 2026. This segment skews heavily toward digital and lending products. Investing in mobile-first features and instant-approval lending for this cohort has the highest growth multiplier.

---

## How This Helps a Financial Institution

| Leadership Level | What They Use | Decision It Drives |
|---|---|---|
| Board and C-Suite | Net Growth by ZIP, Age Group butterfly chart | Capital allocation, branch investment decisions |
| Product Managers | Product Growth bar chart, YOY matrix | Product roadmap prioritization, pricing strategy |
| Branch Managers | Top N ZIP analysis with product breakdown | Local marketing campaigns, staffing decisions |
| Risk and Compliance | Close rate trends, negative net growth ZIPs | Early warning on portfolio health |
| Marketing | Age group analysis | Segment-specific campaign targeting |
| Data and Analytics | Grid Charts view, time intelligence buttons | Precise reporting, month-over-month reconciliation |

---

## Dataset

| Attribute | Detail |
|---|---|
| Total Records | 100,000 |
| Time Range | January 2024 to April 2026 (28 months) |
| Regions | Houston, Dallas, Austin, San Antonio, Rural |
| Product Categories | BNK (Banking), DGT (Digital), EQT (Equity), INV (Investments), LND (Lending), MRT (Mortgage), RET (Retail), WLT (Wealth) |
| Age Groups | 9 brackets from under 10 through 80 plus |
| ZIP Codes | 87 Texas ZIP codes |
| Counties | 19 Texas counties |

**Key columns:**

| Column | Description |
|---|---|
| LOAD_YEAR and LOAD_MONTH | Period of record |
| REGION, COUNTY, ZIP | Geographic dimensions |
| AGE_GROUP | Member age bracket |
| MAJOR, MINOR, PRODUCT | Three-level product hierarchy |
| TOTAL_OPEN_CNT | Total open accounts in segment |
| TOTAL_AMT | Total balance in segment |
| CURR_MONTH_OPEN_CNT | Accounts opened this month |
| CURR_MONTH_CLS_CNT | Accounts closed this month |
| CURR_MONTH_CO_CNT | Charge-offs this month |
| CURR_MONTH_OLB_CNT and AMT | Online banking activity |
| CURR_MONTH_IN_BRANCH_CNT and AMT | In-branch transaction activity |
| CURR_MONTH_ITM_CNT and AMT | Interactive Teller Machine activity |
| CURR_MONTH_ATM_CNT and AMT | ATM transaction activity |

---

## Technical Implementation

**Power Query**
- Combined LOAD_YEAR and LOAD_MONTH into a single Date column for time intelligence
- Set ZIP as Text type to preserve leading zeros and enable map visuals
- All amount columns typed as Decimal Number

**DAX Measures**

```
-- Net Growth includes charge-offs as an additional deduction from growth
-- Formula: Opened minus (Closed plus Charge-Offs)
TOTAL_NETGROWTH =
SUM('AccountStatistics'[CURR_MONTH_OPEN_CNT])
- (SUM('AccountStatistics'[CURR_MONTH_CLS_CNT]) + SUM('AccountStatistics'[CURR_MONTH_CO_CNT]))


-- Dynamic Top N and Bottom N ZIP measure
-- Returns positive net growth for top N ZIPs, negative for bottom N ZIPs, blank for all others
-- The * 1000000 + ZIP trick breaks ties deterministically using ZIP code as a tiebreaker
-- REMOVEFILTERS on PRODUCT ensures ZIP ranking is based on total across all products
TOPNBOTTOMN_NETGROWTH =
VAR RankDesc = TOPN(
    N[N Value],
    ALL('AccountStatistics'[ZIP]),
    CALCULATE(
        [TOTAL_NETGROWTH] * 1000000 + VALUE(SELECTEDVALUE('AccountStatistics'[ZIP])),
        REMOVEFILTERS('AccountStatistics'[PRODUCT])
    ),
    DESC
)
VAR RankAsc = TOPN(
    N[N Value],
    ALL('AccountStatistics'[ZIP]),
    CALCULATE(
        [TOTAL_NETGROWTH] * 1000000 + VALUE(SELECTEDVALUE('AccountStatistics'[ZIP])),
        REMOVEFILTERS('AccountStatistics'[PRODUCT])
    ),
    ASC
)
VAR SelMet = SELECTEDVALUE('AccountStatistics'[ZIP])
RETURN
SWITCH(
    TRUE(),
    SelMet IN SELECTCOLUMNS(RankDesc, "ZIP", 'AccountStatistics'[ZIP]), [TOTAL_NETGROWTH],
    SelMet IN SELECTCOLUMNS(RankAsc, 'AccountStatistics'[ZIP]), -ABS([TOTAL_NETGROWTH]),
    BLANK()
)


-- YOY % change vs same month prior year
-- Returns blank when no prior year data exists (all of 2024 will show blank)
YOY% =
VAR CurrentCount = SUM('AccountStatistics'[TOTAL_OPEN_CNT])
VAR PrevCount =
    CALCULATE(
        SUM('AccountStatistics'[TOTAL_OPEN_CNT]),
        FILTER(
            ALL('AccountStatistics'),
            'AccountStatistics'[PRODUCT] = SELECTEDVALUE('AccountStatistics'[PRODUCT]) &&
            'AccountStatistics'[LOAD_YEAR] = SELECTEDVALUE('AccountStatistics'[LOAD_YEAR]) - 1 &&
            'AccountStatistics'[LOAD_MONTH] = SELECTEDVALUE('AccountStatistics'[LOAD_MONTH])
        )
    )
RETURN DIVIDE(CurrentCount - PrevCount, PrevCount) * 100


-- YOY absolute count difference vs same month prior year
YOY# =
VAR CurrentCount = SUM('AccountStatistics'[TOTAL_OPEN_CNT])
VAR PrevCount =
    CALCULATE(
        SUM('AccountStatistics'[TOTAL_OPEN_CNT]),
        FILTER(
            ALL('AccountStatistics'),
            'AccountStatistics'[PRODUCT] = SELECTEDVALUE('AccountStatistics'[PRODUCT]) &&
            'AccountStatistics'[LOAD_YEAR] = SELECTEDVALUE('AccountStatistics'[LOAD_YEAR]) - 1 &&
            'AccountStatistics'[LOAD_MONTH] = SELECTEDVALUE('AccountStatistics'[LOAD_MONTH])
        )
    )
RETURN (CurrentCount - PrevCount)


-- Date selection table powering the YTD / 1Y / 3Y / 5Y / Max buttons
-- Each button filters the report to a different rolling date window
DateSelection =
VAR TodayDate = TODAY()
VAR YearStart = DATE(YEAR(TodayDate), 1, 1)
VAR OneYStart = EDATE(TodayDate, -12)
VAR ThreeYStart = EDATE(TodayDate, -36)
VAR FiveYearStart = EDATE(TodayDate, -60)
VAR MaxStart = MIN('AccountStatistics'[Month])
RETURN
UNION(
    ADDCOLUMNS(CALENDAR(YearStart, TodayDate), "Selection", "YTD", "Order", 1),
    ADDCOLUMNS(CALENDAR(OneYStart, TodayDate), "Selection", "1Y", "Order", 2),
    ADDCOLUMNS(CALENDAR(ThreeYStart, TodayDate), "Selection", "3Y", "Order", 3),
    ADDCOLUMNS(CALENDAR(FiveYearStart, TodayDate), "Selection", "5Y", "Order", 4),
    ADDCOLUMNS(CALENDAR(MaxStart, TodayDate), "Selection", "Max", "Order", 5)
)
```

**Bookmarks**
- Line Charts bookmark shows all line chart visuals and hides grid tables
- Grid Charts bookmark shows all matrix visuals and hides line charts
- Toggle button on page header switches between both views instantly

**Time Intelligence**
- YTD, 1Y, 3Y, 5Y, Max buttons implemented via bookmark and date slicer combinations
- Date table created in Power Query with Year, Month, Quarter, and MonthName columns

**Reset Button**
- Placed top right on both pages
- Clears all slicer selections and returns the report to default All view

---

## Repository Structure

```
account-statistics-powerbi/
├── Account Statistics.pbix              Power BI report file
├── texas_100k.csv                       Source dataset (100,000 rows)
├── README.md                            This file
└── snapshots/
    ├── page1_zip_analysis.png           ZIP Top N analysis with diverging net growth
    ├── page2_age_group.png              Age group butterfly chart with product breakdown
    ├── page3_product_growth.png         Product growth bar chart with YOY matrix
    ├── page4_trend_line.png             Opened vs closed trend lines (3Y view)
    ├── page5_age_trends.png             Age group trend lines opened and closed
    ├── page6_product_over_time.png      Monthly accounts opened per product over time
    ├── page7_monthly_net_flow.png       Monthly net flow per product
    ├── page8_grid_charts.png            Grid Charts view top two tables
    └── page9_grid_charts_products.png   Grid Charts view product tables
```

---

## Tools and Skills Demonstrated

- Power BI Desktop (visuals, bookmarks, slicers, drill-through, time intelligence)
- DAX (measures, YOY calculations, dynamic Top N, DIVIDE for safe ratios)
- Power Query and M language (data type transformations, date column creation)
- Financial services domain knowledge (charge-offs, product hierarchy, member demographics)
- Executive dashboard design (diverging bars, KPI layering, bookmark toggle UX)
- Data storytelling (each visual answers a distinct business question, no repetition)

---

## Author

**Sai Sreeja**
Data Analyst | SQL | Python | Power BI | Snowflake | Databricks | dbt
[LinkedIn](https://linkedin.com/in/) | [GitHub](https://github.com/SaiSreeja17)

Domain expertise in financial services analytics with hands-on experience building production dashboards, datamart SQL pipelines, dbt transformations, and Azure Data Factory workflows in a credit union environment.