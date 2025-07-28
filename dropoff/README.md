
# Customer Volume Drop-Off & Recovery Analytics

**Project Type**: Growth & Retention Analysis  
**Dataset**: Simulated transactional data – 18,000 weekly deposits across 3,000 unique users  
**Core Focus**: Detecting and quantifying behavioral drop-offs in user deposit activity  
**Tech Stack**: Python (Pandas, NumPy), Jupyter, CSV, GitHub Pages  
**Key Themes**: Operational analytics · Recovery logic · Cohort tracking · Product risk signal  

---

## 🚀 Objective

Identify customers who exhibit **volume drop-offs** in deposit activity, define the **severity** of these drops, and track if and when they **recover**. This kind of insight supports:

- Early detection of **potential churn**
- Quantification of **impact zones** in user experience
- Input for product, risk, and marketing teams to **reactivate key segments**

---

## 🧠 Business Context

In fintech and neobank environments like Revolut, customer inactivity is often a **silent churn** — not visible until it's too late. Instead of waiting for account dormancy, this project focuses on detecting **micro-drop-offs**: weekly-level volume declines that signal something is broken — in UX, pricing, trust, or timing.

This approach helps teams:

- Triage operational issues (e.g., failed auth flows)
- Spot strategic risks (e.g., high-value users silently dropping)
- Feed automated lifecycle campaigns and experimentation

---

## 🧪 Analytical Process

### 1. **Weekly Cohort Structuring**
- Grouped transactions by `uid` and `week`
- Engineered features:
  - `weekly_volume_usd`
  - `weekly_tx_count`
  - `avg_txn_value`

### 2. **Drop-Off Logic**
- Defined drop-off as a **>70% decline** from a user’s previous week
- Created a binary `dropoff_flag`
- Computed `drop_severity`: relative % change in deposit behavior
- Isolated `first_drop_week` to track when each user dropped

### 3. **Recovery Logic**
- Marked a user as recovered if they regained >=80% of their previous volume after a drop
- Added `recovered` boolean and `ever_dropped` tracking
- Built weekly summaries to observe recovery behavior over time

---

## 📈 Engineered Metrics

| Feature              | Description |
|----------------------|-------------|
| `weekly_volume_usd`  | User-level volume per week |
| `dropoff_flag`       | Boolean for a drop-off event |
| `drop_severity`      | Magnitude of drop relative to prior activity |
| `ever_dropped`       | Tracks if a user has ever dropped before a given week |
| `recovered`          | Flags if a user bounced back post-drop |
| `recovery_rate`      | Recovered users / Dropped users (weekly or cumulative) |

---

## 🔍 Project Insights

- **67.4% drop-off rate** occurred during the week of **22 July 2024** — likely a breaking point in the flow or user friction
- **96.4% recovery rate** overall — most users returned after their drop, often within 1–2 weeks
- **-83.9% avg. drop severity** — dropped users saw a major decline in value, not just count
- Drop-offs were concentrated among high-volume users — suggesting risk in upper funnel UX or fees

---

## 💼 Strategic Takeaways

- Weekly volume drops act as **early churn predictors**
- Recovery detection should be embedded in product analytics frameworks
- Risk teams could monitor drop severity + failed deposit ratio as live indicators
- Growth and lifecycle teams should prioritize users with `ever_dropped = True` but `not recovered`

---

## 📁 Repository Structure

```
dropoff-detection/
├── data/
│   └── weekly_user_volume_summary.csv
├── notebooks/
│   └── dropoff_analysis.ipynb
├── README.md
└── recovery_logic.md
```

---

## 📊 Future Directions

- **Segment recovery by channel** (e.g., manual vs. automated deposits)
- **Build anomaly detection logic** to identify systemic vs. user-level drops
- Extend into **predictive churn modeling** with logistic regression or tree-based classifiers
- Automate via **Streamlit** or embed into a **Looker dashboard** for ongoing ops monitoring

---

> Created by **Pelumi Okunola** | Data Analyst & MSc AI + Data Science  
> 📍 [GitHub Portfolio](https://qkpesko.github.io/data_projects/)
