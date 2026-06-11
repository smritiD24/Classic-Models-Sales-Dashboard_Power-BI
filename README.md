# 📊 Classic Models Sales Dashboard — Power BI

> A sales performance dashboard built on the Classic Models dataset, covering orders, products, customers, and payments across 2003–2005.
![DB](https://github.com/smritiD24/Classic-Models-Sales-Dashboard_Power-BI/blob/main/Dashboard_Classic%20Models.png)
---

## 📁 Repository Structure

```
classic-models-powerbi/
│
├── dashboard_screenshot.png       # Dashboard preview image
├── ClassicModels_Dashboard.pbix   # Power BI file (main deliverable)
├── data/
│   ├── customers.csv
│   ├── employees.csv
│   ├── offices.csv
│   ├── order_details.csv
│   ├── orders.csv
│   ├── payments.csv
│   ├── productlines.csv
│   └── products.csv
├── insights/
│   └── key_findings.md            # Written business insights (this section below)
├── README.md
└── data_model.png                 # Screenshot of the star schema / data model in Power BI
```

---

## 🗃️ Dataset Overview

The Classic Models dataset simulates a wholesale distributor of die-cast car replicas. It contains 8 relational tables:

| Table | Rows | Description |
|---|---|---|
| orders | 326 | Order header with dates and status |
| order_details | 2,996 | Line items with quantity and price |
| products | 110 | Product catalog with buy price and MSRP |
| customers | 122 | Customer details and credit limits |
| employees | 23 | Sales reps and management hierarchy |
| offices | 7 | Office locations worldwide |
| payments | 273 | Customer payment records |
| productlines | 7 | Product category descriptions |

---

## 📌 Dashboard Visuals

| Visual | Description |
|---|---|
| **KPI Cards** | Total Sales ($9.6M), Profit Margin % (39.84%), Profit ($3.83M), Top Product |
| **Bar Chart** | Quantity Ordered by Year (2003–2005) |
| **Pie Chart** | Sales share by Product Line |
| **Treemap** | Quantity Ordered by Product Line |
| **Map** | Customer count by country |
| **Bar Charts** | Top 5 and Bottom 5 Selling Products |
| **Slicers** | Filter by Year, City, Sales Rep, Product Line |
| **KPI Gauge** | 2004 monthly sales goal tracker |

---

## 🔍 Key Business Insights

### 💰 Revenue & Profitability

- **Total revenue across all years: $9.6M** with a healthy overall profit margin of **39.84%**, generating **$3.83M in absolute profit**.
- Profit margin consistency across product lines suggests disciplined pricing relative to buy price — the business is not discounting heavily to drive volume.

### 📅 Year-over-Year Trends

| Year | Revenue | Orders | Units Sold | Avg Order Value |
|---|---|---|---|---|
| 2003 | $3.32M | 111 | 36,439 | ~$29,886 |
| 2004 | $4.52M | 151 | 49,487 | ~$29,907 |
| 2005 | $1.77M | 64 | 19,590 | ~$27,671 |

- **2004 was the peak year**, with 36% revenue growth over 2003 — driven by a 36% increase in number of orders and a 36% jump in units ordered.
- **2005 appears to decline sharply (-60.8%)**, but this is misleading — the dataset only covers orders up to mid-2005, so 2005 is an incomplete year. This is important context: the business was likely still on a growth trajectory.
- Average order value remained stable at ~$29K across 2003–2004, suggesting the growth was driven by **customer acquisition and repeat orders**, not price inflation.

### 🏎️ Product Line Performance

| Product Line | Sales | Profit | Sales Share |
|---|---|---|---|
| Classic Cars | $3.85M | $1.53M | 40.1% |
| Vintage Cars | $1.80M | $0.74M | 18.7% |
| Motorcycles | $1.12M | $0.47M | 11.7% |
| Trucks & Buses | $1.02M | $0.40M | 10.7% |
| Planes | $0.95M | $0.37M | 9.9% |
| Ships | $0.66M | $0.26M | 6.9% |
| Trains | $0.19M | $0.07M | 2.0% |

- **Classic Cars dominates at 40% of total sales** — it is the undisputed anchor of the business. Any disruption (supply issue, trend shift) in this category would severely impact revenue.
- **Vintage Cars at 18.7%** is a strong second, making Cars (classic + vintage combined) nearly **59% of all revenue**.
- **Trains is the weakest category** — $188K in sales, $65K profit, and only 2% of revenue. This line may warrant a discontinuation review or a focused promotional campaign.
- Motorcycles, Trucks, and Planes are mid-tier lines with fairly similar sales volumes, suggesting an opportunity to differentiate one of them through targeted marketing.

### 🏆 Top & Bottom Products

**Top 5 by Revenue:**
1. 1992 Ferrari 360 Spider red — $276,840
2. 2001 Ferrari Enzo — $190,756
3. 1952 Alpine Renault 1300 — $190,018
4. 2003 Harley-Davidson Eagle Drag Bike — $170,686
5. 1968 Ford Mustang — $161,531

**Bottom 5 by Revenue:**
1. 1939 Chevrolet Deluxe Coupe — $28,053
2. 1936 Mercedes Benz 500k Roadster — $29,763
3. 1982 Lamborghini Diablo — $30,973
4. 1958 Chevy Corvette Limited Edition — $31,628
5. 1982 Ducati 996 R — $33,269

- Ferrari products occupy two of the top three spots — brand recognition clearly drives premium sales.
- The bottom 5 are all in the $28K–$33K range, suggesting consistently low demand rather than outlier failures.
- The gap between top ($276K) and bottom ($28K) products is nearly **10x** — indicating a long-tail product distribution. A 80/20 analysis would likely reveal that ~20% of products drive 80% of revenue.

### 🌍 Customer Geography

- **USA leads with 36 customers** — nearly 30% of all customer accounts.
- **Germany (13) and France (12)** are the top European markets.
- **Australia (5) and UK (5)** are smaller but present.
- Opportunity: Europe collectively (Germany + France + UK + others) likely rivals or surpasses the US in customer count — a regional breakdown of revenue by territory would be a valuable next analysis.

### 📆 Monthly Seasonality (2004)

| Month | Sales ($K) |
|---|---|
| Jan | 292 |
| Feb | 290 |
| Mar | 218 |
| Apr | 188 |
| May | 248 |
| Jun | 343 |
| Jul | 326 |
| Aug | 419 |
| Sep | 284 |
| Oct | 500 |
| **Nov** | **979** |
| Dec | 429 |

- **November 2004 was by far the biggest month at $979K** — nearly 22% of all 2004 revenue came from a single month. This is likely driven by holiday pre-ordering from retail clients.
- **Q4 (Oct–Dec) accounted for roughly $1.91M**, or about 42% of 2004 annual revenue. The business is **highly seasonal and Q4-dependent**.
- March–April is the softest period, dipping to $188K–$218K. This suggests a potential opportunity for off-season promotions.

### 💳 Payments & Credit

- 273 payments on record from 122 customers — meaning not every customer has paid (some orders may be pending or on credit terms).
- The dataset includes a `creditLimit` column per customer — this could be leveraged to identify high-credit-limit customers who are under-purchasing relative to their limit (a sales outreach opportunity).

---

## 🛠️ Tools Used

- **Power BI Desktop** — data modeling, DAX measures, visualizations
- **CSV files** — raw data source (no SQL server required)
- Dataset inspired by the MySQL Sample Database (Classic Models)

---

## 📚 Reference

Dashboard layout and visual concepts inspired by a guided Power BI tutorial on YouTube. Data analysis, insights, and visual customization (color palette, chart arrangement, titles) performed independently.

---

## 🚀 What to Add to Make This Repository Stand Out

- [ ] `data_model.png` — screenshot of your Power BI data model (star schema showing table relationships)
- [ ] `dax_measures.md` — document your custom DAX formulas (Profit Margin %, YoY Growth, etc.)
- [ ] `data_cleaning_notes.md` — note any transformations done in Power Query
- [ ] A LinkedIn post screenshot if you shared this project publicly
- [ ] `insights/key_findings.md` — paste the business insights section above as a separate file

---

*Dataset: Classic Models (open-source sample database) | Tool: Power BI Desktop*
