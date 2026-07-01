# Bright Coffee Shop Sales Analysis 2026

---

## Introduction

Bright Coffee Shop has appointed a new CEO whose mission is to grow revenue and improve product performance. As a Junior Data Analyst, I was tasked with analyzing historical transactional sales data and delivering actionable insights to support the CEO's decision-making.

---

## Objectives

1. Identify which products generate the most revenue
2. Determine what time of day the store performs best
3. Analyze sales trends across products and time intervals
4. **Deliver recommendations for improving sales performance** *(primary objective — objectives 1–3 provide the evidence base for this)*

---

## Approach & Pipeline

This project follows an **ELT (Extract → Load → Transform)** pattern:

| Stage | What happened |
|---|---|
| **Extract** | Source dataset received in Excel format, converted to CSV |
| **Load** | Raw CSV uploaded into Databricks as-is — no pre-processing applied |
| **Transform** | Data cleaned and reshaped using SQL queries inside Databricks |
| **Analyze** | Transformed results exported to Google Sheets for pivot tables and charts |
| **Present** | Key insights and recommendations delivered via PowerPoint to the CEO |


---

## SQL Transformations (Databricks)

All transformations were performed using SQL inside the Databricks SQL Editor against the raw loaded table.

Key transformations:
- Cast `unit_price` from string to decimal (handling comma-formatted values e.g. `'3,1'` → `3.1`)
- Compute `total_amount = unit_price * transaction_qty`
- Create `transaction_time_bucket` to group transactions into 30-minute intervals
- Group and aggregate by `product_type`, `product_category`, and `time_bucket`

---

## Key Insights Delivered

- Revenue ranking by product type and category (top and bottom contributors)
- Peak and lowest-revenue time intervals across the trading day
- Cross-analysis of which products drive revenue during which time windows
- Volume vs. revenue mismatches (high-volume/low-revenue vs. low-volume/high-revenue products)
- Revenue concentration — whether a small number of products account for most sales

---

## Recommendations

| Finding | Recommendation |
|---|---|
| Slow time slots identified | Run targeted marketing campaigns during low-revenue periods |
| Top-selling products identified | Increase stock allocation for best performers |
| Underperforming products identified | Promote or reconsider low-revenue, low-volume items |

---

## Next Steps

- Automate daily sales reporting
- Track and compare sales performance across multiple store locations
- Implement loyalty programs aligned to peak customer time slots

---

## Tools Used

| Category | Tool |
|---|---|
| Project planning | Miro |
| Data processing | Databricks (SQL Editor) |
| Data analysis | Google Sheets (pivot tables & charts) |
| Presentation | Microsoft PowerPoint |
| Version control | GitHub |

---

## Submission Checklist

- [x] XMind plan / architecture diagram
- [x] Processed dataset with pivot tables & charts (Google Sheets / Excel)
- [x] PowerPoint presentation
- [x] SQL file with all queries
