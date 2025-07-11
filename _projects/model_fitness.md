---
layout: post
title: "Customer Churn Analysis and Strategic Segmentation for Model Fitness"
date: 2024-06-10
categories: proyectos
excerpt: "In this project, I analyzed customer churn patterns and created strategic customer segments for Model Fitness, a gym chain, to reduce attrition and boost retention."
---

## 🎯 Objective

Model Fitness, a gym chain, sought to understand why clients were leaving and how to retain them.  
The goal was to analyze churn behavior, identify patterns, and build strategic customer clusters to guide decision-making.

## ⚙️ How I did it

- Cleaned and prepared customer data including demographic and behavioral features.
- Performed **Exploratory Data Analysis (EDA)** to detect patterns in churned vs active clients.
- Engineered new features and visualized key indicators like tenure, gender, membership type, and activity level.
- Built a **K-Means clustering model** to segment clients into 4 groups based on behavior and risk of churn.
  ![Tenure vs Churn](assets/projects/model_fitness/clusters_kmeans.png)
- Generated actionable recommendations for each segment to support business strategy.

## 🔍 Insights & Findings

- The churn rate was around **27%**, with many cancellations occurring in the first 3 months of membership.
- Clients on **short-term contracts** churned at much higher rates than those with long-term memberships.
- **Lower engagement** (fewer visits and classes per week) was a strong churn predictor.
- The clustering model revealed four clear segments:
  1. **At-risk low-engagement** clients
  2. **Loyal high-engagement** members
  3. **Short-term opportunists**
  4. **Newcomers with potential**

📊 Recommended Screenshot: Scatter plot of clusters with churn proportion

## 💡 Conclusions & Recommendations

- Focus retention efforts on **new clients in their first 3 months** through onboarding programs and engagement tracking.
- Offer **incentives to low-engagement members** to increase visit frequency (e.g., loyalty points or class bundles).
- Encourage **longer contract sign-ups** via discounts or perks, as they correlate with better retention.
- Use cluster profiles to personalize communication and offers based on behavior patterns.

## 🛠️ Tools & Technologies

- Python (Pandas, Seaborn, Matplotlib, Scikit-learn)
- Jupyter Notebook
- K-Means Clustering
- EDA & Data Visualization
