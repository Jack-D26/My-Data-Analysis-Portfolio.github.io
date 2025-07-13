---
layout: post
title: "Hypothesis Prioritisation & A/B-Test Evaluation for an Online Retailer"
date: 2024-07-13
excerpt: "Using ICE/RICE scoring and a production A/B test to decide which growth ideas deserve investment and whether a new checkout flow beats the current one."
---

## 🎯 Objective

The e-commerce team had two immediate questions:

1. **Which growth hypotheses should we tackle first?**
2. **Does our new checkout flow (Group B) outperform the current one (Group A)?**

My goal was to apply data-driven frameworks to prioritise ideas, run a proper A/B test, and interpret the results with statistical rigour.

---

## ⚙️ How I did it

### 1 — Hypothesis Prioritisation

- Gathered eleven marketing / product ideas.
- Scored each using **ICE** (Impact × Confidence ÷ Effort) and **RICE** (Reach × Impact × Confidence ÷ Effort).
- Sorted by RICE to build an execution roadmap; the _email-subscription banner_ ranked top.

### 2 — A/B-Test Analysis

- **Data prep:** merged orders + visits; removed duplicates & nulls; labelled by test group.
- Built cumulative graphs for **revenue**, **orders**, **ARPU**, and **conversion rate**.
- Detected a revenue spike on Aug 17-18 driven by a handful of \$1 000+ orders in **Group B**.
- Applied **Mann-Whitney U-test** with Bonferroni correction across key metrics.

---

## 🔍 Insights & Findings

- **Group B’s cumulative revenue > Group A**, but significance vanished after removing extreme orders.

### Cumulative Revenue – Test vs Control

![Cumulative Revenue]({{ site.baseurl }}/assets/projects/busines_decisions/cumulative_revenue.png)

- **Average Order Value** stayed higher in Group B throughout, suggesting larger baskets, yet variance was high.

### Relationship Between Average Basket Price and Orders

![Scatter: Mean Prices]({{ site.baseurl }}/assets/projects/busines_decisions/scatter_mean_prices.png)

- **Conversion rate differences were not statistically significant** at the 5 % level.

### Conversion Rate Over Time

![Conversion Rate]({{ site.baseurl }}/assets/projects/busines_decisions/conversion_rate.png)

- The RICE matrix highlighted three high-ROI ideas worth immediate rollout (subscription banner, geo-targeted flash sale, simplified product page).

---

## 💡 Conclusions & Recommendations

| Decision                                       | Rationale                                                                          |
| ---------------------------------------------- | ---------------------------------------------------------------------------------- |
| **Do not ship the new checkout flow yet.**     | Uplift driven by very few high-ticket purchases; needs longer run or segmentation. |
| **Investigate high-value orders** on Aug 17-18 | Verify they’re legitimate; if anomaly, rerun test without them.                    |
| **Implement top-ranked RICE ideas**            | Low effort, high reach; expected to lift revenue ~5 % quarter-over-quarter.        |

---

## 🛠️ Tools & Technologies

- Python (Pandas, NumPy, SciPy, Seaborn, Plotly)
- Jupyter Notebook
- **ICE / RICE frameworks** for prioritisation
- **Mann-Whitney U-test** & multiple-comparison correction
- Cumulative KPI visualisation
