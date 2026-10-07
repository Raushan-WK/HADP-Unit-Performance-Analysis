# HADP Unit Performance Analysis: Optimizing Subsidy Allocation & Ground Impact

## Overview
How do you ensure state agricultural subsidies actively drive economic growth and rural jobs rather than getting locked up in underperforming projects?

This repository contains a data-driven evaluation of **86,674 beneficiary-led agricultural units** supported under Jammu & Kashmir's **Holistic Agriculture Development Programme (HADP)**. By combining data cleaning, percentile-based ranking, and portfolio segmentation, this analysis addresses a core policy challenge: **How can public capital be reallocated to maximize Agri-GSDP growth and employment without escalating total program costs?**

---

## The Problem & Analytical Challenge
Under HADP, government subsidies are linked to predefined benchmark unit costs and disbursed on a flat, back-ended basis once a unit is set up. Post-disbursement performance (profit, revenue, person-days of work) is tracked by field officers using the **Kisan Sathi Output Tracking App (OTA)**.

Evaluating 86k+ units revealed two critical operational bottlenecks:
1. **The Diagnostic Data Gap:** ~21% of the portfolio had missing or unverified tracking metrics. Specifically, **14,849 functional units (17.1%)** lacked completed output data in the app, representing **₹512.4M in unmonitored capital**.
2. **Capital Misallocation:** A disproportionate share of subsidy was absorbed by units yielding sub-par financial and employment returns.

---

## Methodology & Performance Framework
To reflect HADP's dual mandate—boosting economic growth while creating rural employment—I built a **Dual-Gating Eligibility Filter** and a **50/50 Composite Efficiency Index**.

### 1. Dual-Gating Eligibility Filters
Units were filtered through two quality gates before being ranked:
* **Functional Gate:** Unit status marked as "Unit Functional" (**88.0%** of the portfolio).
* **Output Completeness Gate:** Must have non-zero, verified Profit and Employment entries in the Kisan Sathi OTA app.

### 2. 50/50 Composite Efficiency Index
To evaluate units fairly against their peer activities ($n \ge 30$) without double-counting subsidy impact, I applied percentile ranking across both impact dimensions:

$$\text{Composite Efficiency Score} = 0.50 \times \text{Financial Efficiency Percentile} + 0.50 \times \text{Employment Efficiency Percentile}$$

Where:
* **Financial Efficiency** = $\frac{\text{Annual Profit (₹)}}{\text{Sanctioned Subsidy (₹)}}$
* **Employment Efficiency** = $\frac{\text{Annual Person-Days}}{\text{Sanctioned Subsidy (₹)}}$

---

## Key Findings & Portfolio Diagnostic

Segmenting the functional portfolio revealed clear structural patterns and sector trade-offs:

* **High-Performers (15.6% of portfolio):** Absorbed **₹587.7M (15.6%)** in subsidy while delivering top-tier financial ROI and robust job creation per rupee spent.
* **Mid-Performers (31.3% of portfolio):** Absorbed **₹1.45B (38.5%)** in subsidy, yielding steady baseline performance.
* **Low-Performers (15.6% of portfolio):** Consumed **₹1.22B (32.4%)** in subsidy—absorbing **2x the capital share of High-Performers** relative to their group size while delivering sub-par output.
* **Sector Nuances & Trade-Offs:**
  * **Income ROI Leaders:** *Farm Mechanization* and *Horticulture* generated the highest profit per subsidy rupee.
  * **Job Creation Leaders:** *Sericulture* and *Livestock* drove the highest person-days generated per unit of capital.

---

## Policy & Governance Recommendations

Rather than cutting funding, the policy goal is to reallocate resources effectively. Based on the diagnostic, I proposed four key interventions:

1. **Shift to a 2-Tranche Performance-Linked Subsidy Model:**
   * **Tranche 1 (70%):** Released upon physical setup verification and mandatory LMS training completion.
   * **Tranche 2 (30%):** Released 6–12 months post-establishment, contingent on verified output reporting in the Kisan Sathi app.
2. **Field Officer SLAs:** Enforce 60-day digital validation SLAs for field officers to resolve the 17.1% unverified unit gap (₹512.4M).
3. **Targeted Unit Support:** 
   * Deliver customized LMS retraining for **13,556 low-performing units**.
   * Conduct diagnostic field audits for **10,366 non-functional units** to determine recovery or sanction revoking.
4. **Dynamic Quota Reallocation:** Gradually shift future sanction quotas away from bottom-performing activity sectors toward high-composite ROI sectors.

---

## Project Artifacts
* `Raushan_Kumar_Excal_Output.xlsx`: Complete analytical model, including raw data processing, activity percentile calculations, and district/sector cross-tabulations.
* `Raushan_Kumar_Slides_Output.pdf`: Executive presentation detailing the performance framework, portfolio diagnostic, and policy roadmap.

---

## Tech Stack & Tools Used
* **Data Processing & Analytics:** Python (Pandas, NumPy), SQL, Excel (Percentile Ranking, Data Modeling, Power Query)
* **Visualization & Presentation:** Microsoft Excel, Google Slides
  
