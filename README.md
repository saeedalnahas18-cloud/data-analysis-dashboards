# Data Analysis Dashboards

Two Excel dashboard projects built from provided course data files. Every number on the dashboard sheets is a live Excel formula — no hard-coded values.

## 1. Online Store — Sales & Customer Dashboards

Source data: 1,001 orders across January–March, 233 products, 1,000 customers (UAE, Egypt, Saudi Arabia).

- Net sales: **20,734,230.54** (gross 21,036,227.94 minus 301,997.40 in member discounts; members get 2%)
- By branch: Saudi Arabia 10,345,068.66 (329 orders, 49.9%), UAE 5,873,173.60 (340 orders, 28.3%), Egypt 4,515,988.28 (332 orders, 21.8%)
- By product line: Health and beauty 320 orders (32.0%), Sports and travel 189 (18.9%), Fashion accessories 171 (17.1%), Electronic accessories 165 (16.5%), Home and lifestyle 156 (15.6%)
- Membership: Member 709 (70.8%), Normal 292 (29.2%)
- Payment: Cash 584 (58.3%), Credit card 291 (29.1%), Ewallet 126 (12.6%)
- Rating: Satisfied 503 (50.2%), Very Satisfied 406 (40.6%), Not Satisfied 65 (6.5%), Full Satisfied 27 (2.7%)
- Net by month: Jan 7,282,854.47; Feb 7,422,918.89; Mar 6,028,457.17

Sheets: README, Products (233), Customers (1,000), Data (1,001 rows, live formulas), Dashboard1_Sales, Dashboard2_Customers.

## 2. Pharma Sales 2019–2020 — Sales & Staff Dashboards

Source data: 230 rows (115 per year), 8 products, 12 sales reps across 3 supervisors.

- 2019 total: **1,043,124**; 2020 total: **1,171,833**; grand total: **2,214,957** (variance +128,709)
- By channel (both years): Pharmacies 980,180; WholeSale 789,178; Hospitals 243,463; Clinics 202,136
- Top supervisor both years: Eman Shaker (2019: 454,359, 43.6%; 2020: 524,844, 44.8%)
- Top reps 2019: Ahmed Ashour 307,518; Aya Mounir 210,120; Ali Mohamed Ali 107,595. Top reps 2020: Aya Mounir 207,237; Atef AbdelHamed 202,933; Ahmed Ashour 201,198
- Total units both years: 127,531

Sheets: README, Data (230 rows, live formulas), Products (8), Supervisors (12), Dashboard1_Sales (year selector All / 2019 / 2020), Dashboard2_Staff.

## Data notes

- Payment code WA (March only, 44 orders) is not defined in the source spec; it is treated as Ewallet because March uses abbreviated payment codes (CA / CSH / WA) while January and February use full words.
- Duplicate invoice ID 687-15-1097 is kept as two distinct orders (January qty 12, Cash; March qty 2, CSH; same customer and product).
- In the pharma data, Total_Price is authoritative; it differs from UNITS x price by rounding only (max |difference| 0.50). A Check column in Data makes this visible.
- The raw pharma file's sheet named "2019" actually holds both years.

## Verification

Both workbooks were verified by LibreOffice headless recalculation: 41/41 checks passed (online store), 141 checks passed across all three year-selector states (pharma).

Screenshots of all four dashboards are in `images/`.

Note: these are course projects built from the provided data files, not real company results.
