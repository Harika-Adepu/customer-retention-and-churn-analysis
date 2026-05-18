# Customer Retention & Churn Analysis

An end-to-end data science and business intelligence project that evaluates customer behavior, maps out customer lifecycle patterns, and diagnoses retention drops using descriptive analytics. This project translates raw operational data into high-impact, actionable business strategies designed to reduce customer churn and maximize lifetime value (CLV)

`CustomerRetentionAndChurnAnalysis.ipynb` - Complete, verified Jupyter Notebook containing data preprocessing, advanced feature engineering, behavioral analytics, and demographic risk visualizations. 

* **Dataset:** [Kaggle Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

---

📌 What It Is

This repository houses a comprehensive customer retention diagnostic pipeline. Rather than applying generic predictive algorithms blindly, this pipeline addresses a core corporate question: *"Why are customers leaving the platform, and which segments are most vulnerable?"* Raw CRM and billing datasets often mask behavioral insights behind unformatted text fields, incorrect data types, and implicit structural anomalies. This project focuses heavily on **Strategic Feature Engineering**—such as building automated billing flags, ecosystem service attachment counters, and duration-based lifestyle cohorts—to extract concrete, job-ready business intelligence.

### Tech Stack & Libraries Used:
* **Language:** Python
* **Data Manipulation:** `Pandas`, `NumPy`
* **Data Preprocessing:** `scikit-learn` (`StandardScaler`)
* **Data Visualization:** `Seaborn`, `Matplotlib` (Custom stylized axes using `PercentFormatter`)

---

🛠️ What It Does

1. **Anomalous Text & Data Cleaning:** Uncovers and resolves hidden text whitespace issues (`" "`) within billing fields that standard `isnull()` checks miss. Casts continuous values to correct float types and purges empty newly created data frames cleanly to prevent calculation crashes.
2. **Behavioral Feature Engineering:** Translates raw attributes into strategic operational indicators:
   * `TenureGroup`: Segments continuous client lifecycles into distinct duration groups (`short-term`, `mid-term`, `long-term`).
   * `IsAutomatic`: Groups payment string indicators into binary automatic vs. manual billing classifications.
   * `NumberOfServices`: Aggregates the sum of attached add-on products to create an operational proxy for consumer platform involvement.
3. **Faceted Demographic Diagnostics:** Leverages cross-cutting trellis plots to multi-facet age matrices (`SeniorCitizen`) directly against `gender` properties, exposing non-obvious churn concentrations across customer profiles.
4. **Ecosystem & Billing Friction Quantification:** Evaluates payment convenience frameworks and platform interlocking indices to construct clear statistical barriers that protect margins against subscription cancellations.

---

## 📊 Customer Lifecycles & Cohorts Identified

Based on the engineered subscription milestones, the processed customer base breaks down cleanly into the following operational performance categories:

| Lifecycle Cohort | Tenure Horizon | Active Base Count | Customer Attrition Count | Base Churn Rate | Customer Retention Rate | Brief Operational Description |
| **Short-Term** | 0 – 12 Months | 2,175 | 1,037 | **47.68%** | 52.32% | Extreme vulnerability phase; nearly half of new accounts cancel within year one. |
| **Mid-Term** | 12 – 48 Months | 2,618 | 619 | **23.64%** | 76.36% | Transitional phase; attrition rates drop by half as platform familiarity builds. |
| **Long-Term** | 48 – 72 Months | 2,239 | 213 | **9.51%** | 90.49% | Established loyal core; highly secure segment with massive system attachment. |

* **Overall Company Metrics:** Total Base Analyzed: **7,032 accounts** | Baseline Company Churn: **26.58%** | Base Retention: **73.42%**

---

## 🚀 Business Benefits & Actionable Strategies

By deploying the insights discovered within this analytical pipeline, startup founders, product managers, and retention teams can transition from defensive discounting to proactive, high-ROI stabilization frameworks:

* **Optimize the Early Onboarding Window (Short-Term Cohort):** Because data proves attrition is heavily front-loaded in the first 12 months, companies should launch automated usage check-ins, product feature walkthroughs, and success milestone emails during weeks 2 to 4 to quickly drive time-to-value.
* **Remove Renewal Friction (Billing Automation):** Customers on manual invoicing (checks/electronic checks) churn at more than double the rate (**34.74%**) of automatic autopay lines (**16.00%**). By running limited-time promos (e.g., *"Save \$5 next month by switching to autopay"*), you remove recurring monthly decision points where consumers question platform value.
* **Drive Ecosystem Interlocking (Service Attachment):** Accounts utilizing 0 add-on services suffer an extreme churn rate exceeding **40%**. Once a customer connects 3 or more services (Online Backup, Tech Support, Security lines), their churn probability drops to nearly zero. Bundling minor technical add-ons into baseline contracts creates powerful functional switching costs.
* **Target Demographic Vulnerabilities (Senior Portals):** Trellis mapping reveals that Senior Citizen status is a primary churn catalyst, pushing cancellation rates past **~40%** completely independent of gender. Simplifying digital statements, enlarging UI typography, and keeping dedicated human telephone support options open will actively safeguard this retirement-age market share.
