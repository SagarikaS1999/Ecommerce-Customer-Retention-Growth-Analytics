# Data Analytics Case Study
## CohortIQ: Retention, CLV, and Churn Modeling in E-commerce

This repository contains my solutions to a SQL-based analytics case study for a **Data Growth Analyst** role. The case simulates a real-world data analysis task using an e-commerce dataset to uncover insights around customer retention, revenue health, lifetime value, and churn risk.

The work was done in **Google Colab** using **pandasql**, **pandas**, and Python data visualization libraries like **matplotlib** and **seaborn**. All code, reasoning, and charts are included for review and discussion.

---
## 💻 Tech Stack Used

| Tool/Library   | Purpose                                           |
|----------------|---------------------------------------------------|
| **Python**     | General scripting and data handling               |
| **pandas**     | Data manipulation and preprocessing               |
| **pandasql**   | SQL-style querying on pandas DataFrames           |
| **matplotlib** | Visualization of retention curves and segments    |
| **seaborn**    | Advanced data visualization and plotting styles   |
| **Google Colab** | Development and execution environment          |

---
## 🧠 Business Impact

This project mimics how a Data Analyst would support a **growth team**, **marketing team**, and **customer success** by delivering actionable insights such as:
- Real retention patterns beyond surface-level metrics
- Data-driven CAC benchmarks by segment
- Diagnosis of healthy vs. unsustainable growth
- Proactive churn intervention strategy

---

## 🧠 Case Questions & Deliverables

### 📈 1. Cohort Retention Analysis

- Built a monthly **cohort table** showing user retention over 12 months.
- Conducted **resurrection analysis** to track users returning after 2+ months of inactivity.
- Created **quality retention** metrics by filtering low-value customers (total spend < $50).

**Deliverables:**
- Retention matrix table
- Resurrection rate table
- Comparison of standard vs. quality retention

### 💰 2. Customer Lifetime Value (CLV) & Acquisition Efficiency

- Segmented users by first-90-day behavior: single/repeat purchasers, high/low value.
- Calculated predicted CLV using:
  - Average Order Value
  - Monthly purchase frequency
  - Estimated lifespan
- Recommended **maximum Customer Acquisition Cost (CAC)** using a 3:1 LTV:CAC ratio.
- Validated model with actual CLV of customers with 12+ months of data.

**Deliverables:**
- Segment-wise CLV estimates and CAC thresholds

### 📊 3. Growth Decomposition & Revenue Health

- Decomposed monthly revenue growth into:
  - New customer revenue
  - Existing customer expansion
  - Customer churn impact
- Computed **Net Revenue Retention (NRR)** by cohort
- Identified whether growth was driven by acquisition or expansion

**Deliverables:**
- Growth waterfall analysis
- NRR tables

### ⚠️ 4. Customer Risk Scoring & Churn Prevention

- Built a **customer risk scoring system** using RFM + engagement:
  - Recency of purchase
  - Purchase frequency trend
  - Spending trend
  - Category diversity
- Identified **at-risk high-value customers**
- Ranked top 50 customers by churn risk × value

**Deliverables:**
- Risk score methodology and distribution
- Prioritized customer retention table
- Recommended timing for retention intervention

---
## 📊 Dataset Overview

The dataset used is an e-commerce orders table with the following schema:

| Column         | Description                           |
|----------------|---------------------------------------|
| `invoice_id`   | Unique identifier for each transaction |
| `line_item_id` | Unique identifier for each item line   |
| `user_id`      | Customer identifier                    |
| `item_id`      | Product identifier                     |
| `item_name`    | Product name                           |
| `item_category`| Product category                       |
| `price`        | Price of the item (USD)                |
| `created_at`   | Timestamp of order creation            |
| `paid_at`      | Timestamp of payment completion        |


