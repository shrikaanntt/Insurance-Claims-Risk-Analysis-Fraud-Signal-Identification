# Insurance Claims Risk Analysis & Fraud Signal Identification

##  Project Overview

Insurance claims management is a critical operational function where inaccurate risk assessment can lead to financial losses, operational inefficiencies, and increased fraud exposure. This project focuses on analyzing real-world insurance claims data to identify **behavioral, temporal, and financial risk signals** that can help insurers prioritize claim reviews and improve decision-making.

Rather than directly labeling claims as fraudulent, the objective is to surface **risk indicators** that increase the likelihood of claim misuse, enabling smarter triaging and more efficient allocation of investigation resources.

---

##  Business Objectives

* Identify claim patterns associated with elevated risk
* Understand how claim timing, severity, and behavior impact risk exposure
* Support **risk-based claim triage** instead of blanket investigations
* Provide actionable insights aligned with real insurance workflows

---

##  Dataset Description

* **Source:** Open-source insurance claims dataset
* **Granularity:** Claim-level data (one row per claim)
* **Key Data Categories:**

  * Policy & customer attributes
  * Incident and claim context
  * Financial claim components
  * Vehicle information
  * Outcome indicator (`fraud_reported`, used only for validation)

---

##  Tools & Technologies

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Jupyter Notebook**

---

##  Project Methodology

### 1️. Data Audit & Understanding

* Reviewed dataset structure, data types, and column relevance
* Classified features into policy, incident, financial, and behavioral groups
* Identified junk and non-informative columns

### 2️. Data Cleaning & Validation

* Removed irrelevant columns
* Converted date fields into proper datetime formats
* Assessed missing values from a **business perspective**
* Validated financial consistency:

  * Ensured `total_claim_amount = injury + property + vehicle claims`

### 3️. Feature Engineering

Created meaningful risk signals, including:

* **Authority involvement flags**
* **Police report availability indicators**
* **Days since policy binding**
* **High-severity claim flags (top decile)**
* **Vehicle age at time of incident**

These features were engineered to reflect **real insurer risk assessment logic**.

### 4️. Exploratory Data Analysis

* Analyzed claim severity across:

  * Policy tenure
  * Vehicle age
  * Authority involvement
* Visualized patterns using bar charts to highlight:

  * Early-policy high-risk claims
  * High-severity claims without authority involvement
  * Vehicle age vs claim amount trends

### 5️. Business Insights & Recommendations

Key findings were translated into **actionable business insights**, focusing on:

* Early-policy claim monitoring
* Risk-based investigation prioritization
* Operational efficiency through selective manual review
* Feedback loops for underwriting and pricing teams

---

##  Key Insights

* Claims filed shortly after policy binding exhibit higher average claim amounts
* High-severity claims without authority or police involvement carry elevated risk
* Older vehicles combined with high claim amounts warrant closer scrutiny
* Risk is best identified through **feature combinations**, not single indicators

---

##  Business Recommendations

* Implement stricter review rules for early-policy claims
* Use severity and behavioral flags to prioritize investigations
* Allow low-risk claims to flow through automation
* Continuously refine underwriting rules using claim behavior feedback

---

##  Limitations

* Dataset does not include historical claim behavior per customer
* External factors such as repair invoices and adjuster notes are unavailable
* Fraud label is not used as a predictive variable, only for reference

---

##  Project Outcome

This project demonstrates an end-to-end analytics workflow that mirrors real insurance operations — from data auditing and feature engineering to business-driven insights and recommendations. It showcases how analytics can be embedded into claims workflows to reduce leakage, improve efficiency, and support informed decision-making.

---

##  How to Run

1. Clone the repository
2. Open the Jupyter Notebook
3. Run cells sequentially to reproduce the analysis

---

##  Author

**Shrikant Sharma**
*Analytics & Insurance Risk Analysis*
