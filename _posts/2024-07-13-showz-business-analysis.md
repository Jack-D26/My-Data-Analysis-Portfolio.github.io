---
layout: post
title: "User-Behaviour & Marketing-ROI Analysis for Showz Ticket Platform"
date: 2024-07-14
excerpt: "Daily traffic patterns, funnel timing, cohort revenue and ROMI by acquisition channel for an online ticket marketplace."
---

## 🎯 Objective

The analytics team at **Showz** wanted to understand:

1. How visitors use the platform day-to-day.
2. When they convert from first visit to first purchase.
3. How much revenue each signup cohort generates over time.
4. Whether marketing spend is paying for itself (CAC vs LTV, ROMI).

---

## ⚙️ How I did it

- **Data sources**

  - 2 years of web-server logs (visits & sessions).
  - Order database (dates, order values).
  - Monthly marketing-spend file.

- **Pre-processing**

  - Removed bots, duplicates, timezone noise.
  - Joined visits ↔ orders ↔ spend; created visitor and order cohorts.

- **Key analyses**
  1. **Traffic & engagement** – daily / weekly / monthly unique users, session length, returning-user share.
  2. **Funnel timing** – distribution of “first visit → first order” lag.
  3. **Cohort LTV curves** – revenue month 0 → month 12 per signup cohort.
  4. **CAC vs LTV & ROMI** – channel-level payback calculation.

### Cohort Revenue over 12 Months

![Cohort LTV]({{ site.baseurl }}/assets/projects/showz_analysis/cohort_ltv.png)

---

## 🔍 Insights & Findings

- **~908 daily unique users**, **~23 k monthly** – healthy, steady growth.

### Daily Traffic Trend

![Daily Unique Users]({{ site.baseurl }}/assets/projects/showz_analysis/daily_unique_users.png)

- **~26 % of daily traffic is returning users**, showing engagement.
- **Average session ≈ 10 min** → users browse events before buying.
- **Conversion rate ≈ 17 %**; 70 % of first orders happen within 30 days of first visit.
- Mobile traffic lags in conversion vs desktop → UX opportunity.
- **Channel 1 has the best ROMI (0 .85)**, **Channels 3, 4, 5, 10 are negative**.

### ROMI by Acquisition Channel

![ROMI by Channel]({{ site.baseurl }}/assets/projects/showz_analysis/romi_by_channel.png)

- Cohort curves flatten after month 4 → if CAC > LTV by then, channel is unprofitable.
- Overall marketing spend > revenue → current mix runs at a net loss (ROI = –0 .23).

---

## 💡 Conclusions & Recommendations

| Action                                        | Impact                              | Effort |
| --------------------------------------------- | ----------------------------------- | ------ |
| Reduce / renegotiate **Channels 3, 4, 5, 10** | Eliminate negative-ROI spend        | Low    |
| Scale **Channel 1**                           | Highest revenue; breaks even < 3 mo | Medium |
| Improve **mobile checkout flow**              | Capture untapped mobile demand      | High   |
| Launch **first-30-days retention programme**  | Most LTV accrues early              | Medium |

---

## 🛠️ Tools & Technologies

- Python (Pandas • NumPy • SciPy • Seaborn • Matplotlib)
- Jupyter Notebook
- Cohort & funnel analysis, CAC/LTV modelling
- Mann-Whitney U for significance checks
- Custom KPI dashboards
