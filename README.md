# Retail Profitability Model

SKU Contribution Margin & Price Elasticity Scenario Analysis  
*(FP&A / Revenue Analytics Project)*

---

## Overview

This project demonstrates a lightweight FP&A-style model used to evaluate **SKU-level profitability** and support **pricing decisions** through contribution margin analysis and elasticity-based scenarios.

It is designed to be simple, interpretable, and extensible — similar to internal tools used by finance and revenue analytics teams.

---

## Model Overview

### Contribution Margin

For each SKU:

- **Revenue** = Price × Units  
- **Gross Profit** = (Price − Unit Cost) × Units  
- **Contribution Margin (%)** = (Price − Unit Cost) / Price  

---

### Price Elasticity Scenario

Demand response is estimated using:

- **%ΔQ = Elasticity × %ΔP**

For a given price change:

- **New Price** = Price × (1 + %ΔP)  
- **New Units** = Units × (1 + %ΔQ)  

Revenue and profit are recomputed under each scenario.

---

## Outputs

### SKU-Level Profitability
- Revenue  
- Gross profit  
- Contribution margin (%)

### Scenario Comparison Summary
- Total revenue  
- Total profit  
- Total units  
- Delta vs. baseline  

---

## Assumptions & Notes

- Elasticity is assigned at the **category level** for simplicity (a common approach in early-stage FP&A analysis).
- The model prioritizes clarity and interpretability over statistical complexity.
- Designed to be easily extended with historical data or dashboards.

---

## Project Structure

```text
retail-profitability-model/
├── data/
│   └── sample_sales.csv
├── notebooks/
│   └── 01_profitability_model.ipynb
├── README.md
└── requirements.txt
