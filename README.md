# UAE Real Estate Rental Market — BI Portfolio Project

## Project Overview

An end-to-end Business Intelligence project analyzing **73,742 UAE property rental listings** across all seven emirates. The goal was to uncover pricing patterns, market distribution, and value opportunities across Dubai, Abu Dhabi, Sharjah, and the Northern Emirates.

**Tools used:** SQL · Microsoft Excel · Power BI  
**Dataset:** UAE rental listings covering all 8 emirates  
**Records:** 73,724 listings · 8 emirates · 9 property types

---

## Business Questions Answered

### SQL Analysis

| # | Question | Technique |
|---|----------|-----------|
| Q1 | What unique cities are covered? | SELECT DISTINCT |
| Q2 | What property types are available? | SELECT DISTINCT |
| Q3 | Find furnished apartments in Dubai under 80K AED | Filtering & Sorting |
| Q4 | Find large villas (4BR+, 3,000+ sqft) across all emirates | Filtering & Sorting |
| Q5 | Show properties listed in the last 30 days | Date filtering |
| Q6 | Calculate market-wide KPIs (avg rent, min, max, avg area) | Aggregation + Outlier detection |
| Q7 | Rank each emirate by listing volume and average rent | GROUP BY |
| Q8 | Compare rental costs across property types in 2024 | GROUP BY + Date filter |
| Q9 | Furnishing mix (furnished vs unfurnished) by city | GROUP BY |
| Q10 | Value score rating based on rent per sqft thresholds | CASE / Conditional logic |
| Q11 | Bedroom category segmentation (Studio → Family) | CASE / Conditional logic |
| Q12 | Top locations in Dubai by average rent (10+ listings) | Subquery + HAVING |
| Q13 | Cities where average rent exceeds the national average | Correlated subquery |

### Key Findings
- **Dubai dominates** the market with ~50% of all listings (29,366 properties)
- **Dubai median rent (140K AED)** is nearly 4× Sharjah's median (37K AED)
- **Furnished units command a significant rent premium** across all emirates
- An outlier property at **55M AED** was skewing the national average — identified, investigated, and filtered
- **Abu Dhabi** is the second-largest market at 28.6% of listings, with a median rent of 90K AED

---

## Excel Workbook Structure

| Sheet | Purpose |
|-------|---------|
| `Cleaning` | Main working dataset: cleaned data with added ID column, Short Address normalization, and derived columns |
| `Lookup Table` | XLOOKUP reference table — looks up Property Type, Rent Amount, City, and Rent Category by ID |
| `Sparklines` | Property listing growth by emirate (Jan–Apr 2024) with inline sparkline charts |
| `Conditional Formatting` | Market volume and rank by emirate with color-coded star ranking |
| `Apartment Counts Chart` | PivotTable showing Dubai apartment listing counts by month (Jan–Apr 2024) |
| `Rent Comparison` | PivotTable comparing median vs average rent by emirate across all 8 cities |

### Data Cleaning Steps Performed
- Added sequential ID column for record identification
- Normalized full address to short city-level format (`Short Address`)
- Engineered `Rent_per_sqft` and `Rent_category` (Low / Medium / High) derived columns
- Verified zero nulls across all critical fields


---

## Power BI Dashboard

The Power BI report (`Project.pbix`) includes interactive visuals covering:
- Rent distribution by emirate and property type
- Furnished vs unfurnished rent comparison
- Listing volume trends over time
- Geographic distribution of listings across the UAE

---

## Files in This Repository
```
UAE-Real-Estate-BI-Portfolio/
├── README.md
├── SQL/
│   └── UAE_Rental_Analysis.sql
├── Excel/
│   └── dubai_properties_v1.xlsx
└── PowerBI/
    └── Project.pbix
```

---

## About Me

Information Systems student specializing in Business Intelligence. Interested in BI analyst roles across the Gulf region.

Connect with me on [  https://www.linkedin.com/in/mohammad-mohammad-0547283b1/  ](LinkedIn) ← paste your LinkedIn URL here
