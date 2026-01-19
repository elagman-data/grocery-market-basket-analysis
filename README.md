# Grocery Market Basket Analysis (Exploratory Apriori)
**Industry:** Retail | Customer Analytics | Data Mining

---

## Executive Summary
This project performs an **exploratory market basket analysis** on grocery transaction data
using the **Apriori algorithm**. The objective is to identify frequently co-purchased items
and examine how different parameter configurations (support, confidence, lift, and rule length)
affect the quantity, strength, and interpretability of association rules.

Rather than optimizing for a single “best” model, the analysis emphasizes **experimentation
and sensitivity analysis**, reflecting real-world data mining workflows where parameter
tuning is essential for balancing discovery and business usability.

---

## Business Context
Market basket analysis is commonly used in retail and e-commerce to support:
- Cross-selling and product recommendation strategies
- Product bundling and promotion design
- Store layout and merchandising decisions
- Targeted offers and campaign planning

The resulting association rules help answer questions such as:
> *If a customer buys item A, how likely are they to also buy item B?*

---

## Dataset Overview
The analysis uses a **publicly available grocery transactions dataset** containing:
- Customer identifiers
- Transaction dates
- Purchased item descriptions

A transaction basket is defined as the set of unique items purchased by the same customer
on the same date.

*Note: The raw dataset is not included in this repository due to size and licensing considerations.*

---

## Methodology
The analysis follows an exploratory data mining approach:

### 1. Data Preparation
- Cleaned item descriptions and transaction dates
- Grouped purchases into transaction baskets

### 2. Exploratory Analysis
- Examined item frequencies and transaction characteristics
- Visualized purchasing patterns

### 3. Association Rule Mining
- Applied the **Apriori algorithm**
- Evaluated rules using:
  - **Support:** frequency of itemsets
  - **Confidence:** likelihood of co-purchase
  - **Lift:** strength of association beyond chance

### 4. Parameter Experimentation
- Tested multiple configurations of support, confidence, lift, and rule length
- Compared trade-offs between rule coverage and actionability

---

## Why the Code Shows Multiple Experiments
The Python script intentionally includes **multiple Apriori runs** with different parameter
settings. This reflects real-world data mining practice, where:
- There is no single “correct” threshold
- Analysts must balance coverage versus interpretability
- Patterns that remain stable across configurations are often more valuable

The code documents how insights change as assumptions and thresholds vary.

---

## Key Observations
- Lower support thresholds increase the number of discovered rules but introduce more noise.
- Higher lift thresholds reduce rule volume while improving interpretability and strength.
- Some item associations remain stable across configurations, indicating robust purchasing behavior.
- Parameter selection depends on the intended business objective
  (broad discovery vs actionable recommendations).

---

## Tools & Techniques
- **Python**
- **Pandas:** data preparation and manipulation
- **Apriori Algorithm**
- **Association Rule Metrics:** support, confidence, lift

---

## Next Steps
- Validate rule stability across different time periods
- Focus on high-lift, high-confidence rules for potential deployment
- Extend analysis to customer segmentation or time-based trends
- Integrate association rules into recommendation or promotion systems

---

*Note: This project emphasizes exploratory analysis. The code intentionally documents
experimentation and parameter tuning to reflect realistic data mining workflows rather
than a single optimized solution.*
