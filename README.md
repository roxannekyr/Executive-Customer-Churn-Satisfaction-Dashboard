# Customer Satisfaction & Churn Analytics Dashboard

> **An end-to-end analytics project** covering data modelling, churn detection, loyalty segmentation, cohort analysis, and interactive Power BI reporting — built on retail transaction data across multiple Greek cities.

## Project Overview

This project transforms raw customer transaction records into a **multi-layered analytical framework** designed to answer key business questions around customer retention, satisfaction, and loyalty. The output is an interactive Power BI dashboard backed by a purpose-built data model.

| Dimension | Detail |
|---|---|
| **Data Period** | Jan 2023 – Dec 2024 |
| **Transactions** | ~5,000+ records |
| **Geographies** | Athens, Thessaloniki, Patras & more |
| **Categories** | Beauty, Clothing, Food, Electronics, Household |
| **Channels** | Online & In-Store |

## Analytical Framework

The project was structured around five interconnected analytical layers:

1. Churn Detection Model
- Defined churn using a **recency-based threshold** (configurable: default 6 months / 180 days)
- Calculated churn rates segmented by sales channel (Online vs. In-Store)
- Built a dedicated `Churn_Spend Analysis` model to cross-reference spend behaviour with attrition

2. Loyalty Programme Analysis
- Extracted each customer's **current loyalty status** (most recent record, not transactional average)
- Tracked loyal members who subsequently churned — isolating the loyalty-churn overlap
- Calculated: Total Loyals → Loyal Members Churned → Loyal Churn Rate %

3. Cohort Analysis
- Grouped customers by **acquisition cohort (month/year)**
- Tracked churn rate per cohort over time
- Produced a **time-based heatmap** to identify at-risk cohorts
- Modelling-ready output table for Power BI integration

4. Satisfaction vs. Category vs. Churn
- Segmented customers into `Satisfied` / `Not Satisfied` / `Average Satisfied` buckets
- Cross-referenced satisfaction scores with **product category**, purchase method, loyalty status, and churn flag
- Built a composite key (`Bridge_Table`) to enable many-to-many relationships in the data model

5. Date & Time Intelligence
- Constructed a dedicated `Calendar` and `Time` dimension table
- Enabled YoY comparisons, monthly trend analysis, and cohort labelling

## Data Model Architecture

The model follows a **star schema** design principle.

A `Bridge_Table` was designed to handle **many-to-many cardinality** between purchase dimensions (method, location, category, year, loyalty flag), enabling clean filtering across the dashboard without data duplication.

> ⚠️ **Note on source data:** The raw and intermediate analytical workbooks are intentionally excluded from this repository to protect data privacy. The `.pbix` file contains the final, structured data model and all calculations needed to explore the analysis. If you would like to discuss the underlying methodology in detail, please feel free to [reach out](#contact).

---

## 📸 Power BI Dashboard Preview

> 💡 *Screenshots below — click the `.pbix` file to explore the full interactive experience.*

| <img width="1328" height="753" alt="image" src="https://github.com/user-attachments/assets/11c7b171-85b3-4eb1-95db-bc119a4b955a" />
| <img width="1283" height="737" alt="image" src="https://github.com/user-attachments/assets/47387fb2-52de-4d86-a107-1d1d7de2cfcb" />
| <img width="1330" height="751" alt="image" src="https://github.com/user-attachments/assets/dc9a1372-c130-499b-bc90-1743ac41be1f" />
| <img width="1330" height="489" alt="image" src="https://github.com/user-attachments/assets/521df4d4-62c9-4041-a0c1-fe0d6565619d" />
| <img width="1331" height="746" alt="image" src="https://github.com/user-attachments/assets/a2b9f5a1-2460-4651-8ae2-d05a5ef9b002" />


## Tools & Techniques

| Tool | Usage |
|---|---|
| **Power BI Desktop** | Dashboard design, DAX measures, interactive filtering |
| **Excel (Advanced)** | Data modelling, Power QUERY, power pivots etc|
| **Data Modelling** | Star schema design, bridge tables, many-to-many handling |
| **Statistical Methods** | Recency-based churn definition, cohort retention curves |

## Key Business Insights Surfaced

- 📉 Identified cohorts with **above-average churn rates** and mapped them to specific acquisition months
- 🛒 Online vs. In-Store channels showed **distinct churn profiles** — informing channel strategy
- 💳 A measurable share of **loyalty programme members still churned**, revealing loyalty ≠ retention
- ⭐ Customer satisfaction scores correlated differently with churn depending on **product category**

## Contact

Interested in the methodology, the data model design, or a walkthrough?

- 💼 [LinkedIn]: https://linkedin.com/in/roxani-kiritsi/

*Built with curiosity, structured thinking, and too many nested SUMIFS.*
