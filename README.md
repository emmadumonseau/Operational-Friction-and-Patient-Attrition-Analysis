# Operational Friction & Patient Attrition Analysis

## Executive Summary
Patient drop-off directly impacts clinical outcomes and organizational financial stability. This project investigates the structural and operational drivers of patient loss across a multi-specialty health system. By synthesizing clinical satisfaction scores, appointment attendance history, insurance models, and patient travel distance, this interactive Tableau dashboard identifies **$451,052 in total revenue at risk** across **705 high-risk patients**, establishing a benchmark system-wide **Patient Attrition Rate of 68.4%**.

---

## Business Questions Addressed
This analysis was structured to answer four core questions for health system leadership:

1. **Baseline & Specialty Disparities:** What is our current baseline attrition rate, and which clinical specialties significantly exceed this threshold?
2. **Operational Bottlenecks:** How do appointment friction (missed visits) and patient satisfaction interact to drive patient churn?
3. **Insurance Vulnerability:** Does patient attrition correlate with specific insurance types or reimbursement structures?
4. **Geographic Barrier Impact:** How does travel distance affect patient adherence and total financial leakage?

---

## Key Findings

### 1. High-Risk Clinical Specialties
* **Top Attrition Specialties:** **Neurology (70.3%)** and **Family Medicine (70.2%)** lead all departments in patient loss, exceeding the **68.4% system baseline**.
* **Primary Care Impact:** High attrition in foundational care entry points like Family Medicine and General Practice (69.5%) creates downstream leakage across secondary care pipelines.
* **Low-Attrition Outliers:** **Orthopedics (64.0%)** and **Cardiology (65.2%)** show higher retention, indicating strong patient adherence in procedure-driven care.

### 2. Operational Friction (Missed Visits + Satisfaction)
* **The High-Risk Compound Effect:** The highest volume of severe friction occurs among patients with **4–5 missed appointments** and **Low Satisfaction scores (1.0–2.4)**.
* **Early Friction Warning:** Even within **High Satisfaction (3.6–5.0)** groups, patients with **1–2 missed appointments** show steady drop-off, indicating that operational inconvenience (scheduling, wait times) can impact adherence before patient satisfaction scores visibly drop.

### 3. Payer Exposure
* **Medicaid Attrition Peak:** **Medicaid patients demonstrate the highest attrition rate at 70.5%**, closely followed by **Private Insurance (69.4%)**.
* **Government/Medicare Adherence:** **Medicare (66.7%)** and **Self-Pay (67.1%)** cohorts perform better than baseline retention rates, highlighting distinct behavioral patterns between commercial and government-sponsored coverage.

### 4. Distance & Financial Exposure
* **The 25+ Mile Risk Cliff:** Patients traveling **25+ miles** experience the highest attrition rate (**72.3%**) and represent the largest single dollar concentration (**$238,852 in Revenue at Risk**).
* **Proximity Retention:** Local patients (**0–10 miles**) retain significantly better (**64.5% attrition**, **$74,005 at risk**), confirming physical distance as a primary barrier to continuous care.

---

## Strategic Recommendations & Action Plan

### 1. Address Geographic Friction (25+ Mile Cohort)
* **Telehealth & Remote Monitoring Integration:** Implement hybrid telehealth options for routine follow-ups in high-volume, long-distance specialties (e.g., Neurology consultation).
* **Transportation & Regional Hubs:** Partner with non-emergency medical transportation (NEMT) services to reduce patient drive times.

### 2. Implement Automated Missed Visit Intervention Protocols
* **Trigger-Based Outreach:** Establish automated care navigation outreach after **2 missed appointments**, rather than waiting for formal discharge or complete attrition.
* **Flexible Re-Scheduling Systems:** Offer digital portal self-scheduling and SMS reminder adjustments for high-risk groups to lower scheduling barriers.

### 3. Targeted Specialty Retention Strategies
* **Family Medicine & Primary Care Stabilization:** Investigate primary care appointment wait times and clinic workflows to identify why patient drop-off occurs early in care navigation.
* **Payer Navigation Support:** Provide dedicated financial counseling and navigation support for Medicaid patients to prevent coverage gaps.

---

## Dashboard Architecture & Stack
* **Analytics & Data Modeling:** Python (Pandas), SQL
* **Visualization & Business Intelligence:** Tableau Desktop / Tableau Public
* **Key Visual Elements:**
  * **Top KPI Scorecards:** Active Patients, Attrition Rate, Total Revenue at Risk.
  * **Specialty & Payer Horizontal Bars:** Sorted volume distribution with system-wide reference baseline line (`68.4%`).
  * **Operational Friction Matrix:** Heatmap comparing satisfaction tiers against missed visit counts.
  * **Dual-Axis Revenue & Distance Exposure:** Combination Bar Chart (`SUM(Revenue at Risk)`) & Trendline (`AVG(Attrition Rate)`).
