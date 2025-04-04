

# 🚗 Analyzing Insurance Auto Claims

## 📘 Overview  
This repository presents the code, analysis, and documentation for a data science project titled **"Analyzing Insurance Auto Claims"**. The project explores a dataset of **6,249 auto insurance claims** from a company operating in the **southwest and western United States**. The main goal is to address declining profitability by generating **actionable insights** related to pricing strategies, customer segments, and policy improvements.

---

## 🎯 Project Objectives  

This project investigates the following key questions:

1. **📈 Customer Lifetime Value (CLV)**  
   How does CLV vary across different auto policy types?

2. **💼 Employment & Income**  
   How do employment status and income influence policy preferences?

3. **🚙 Vehicle Impact on Claims**  
   What is the relationship between vehicle class/size and claim amounts?

4. **💸 Premium Pricing Analysis**  
   How do vehicle attributes affect monthly premiums?

5. **🔁 Policy-Premium Interplay**  
   How do vehicle size, class, and channel affect pricing dynamics?

---

## 📂 Dataset  

- **Source**: [`claims_df.rds`](https://gmubusinessanalytics.netlify.app/data/claims_df.rds)  
- **Size**: 6,249 insurance claims  
- **Key Variables**:
  | Variable | Description | Data Type |
  |----------|-------------|-----------|
  | `customer_id` | Unique customer identifier | Character |
  | `policy` | Auto policy type (e.g., Personal, Corporate) | Factor |
  | `vehicle_class` | Vehicle type (e.g., Sedan, Luxury SUV) | Factor |
  | `vehicle_size` | Vehicle size (Small, Medium, Large) | Factor |
  | `monthly_premium` | Monthly insurance premium (USD) | Numeric |
  | `current_claim_amount` | Current claim amount (USD) | Numeric |
  | `total_claims_amount` | Historical total claim amount (USD) | Numeric |
  | `customer_lifetime_value` | Revenue minus total claim costs (USD) | Numeric |

(See notebook for full list.)

---

## 🧪 Methodology  

- **Language & Tools**: R (v4.2.1+), `tidyverse`, `ggplot2`, `RColorBrewer`  
- **Data Loading**:
  ```r
  library(tidyverse)
  claims_df <- readRDS(url("https://gmubusinessanalytics.netlify.app/data/claims_df.rds"))
  ```

- **Analysis Includes**:
  - Summary statistics and grouped averages
  - Faceted scatter plots and bar charts
  - Key visual: CLV vs. policy type & claims vs. vehicle class

---

## 📊 Key Findings  

- **🏆 CLV & Policy**:  
  Personal auto policies yield the **highest CLV** across all policy types.

- **👔 Employment & Income**:  
  Employed individuals have **higher income levels**, particularly under personal policies.

- **🚘 Claim Risks**:  
  **Luxury SUVs and large vehicles** are tied to higher current and total claim amounts.

- **💰 Premium Insights**:  
  Monthly premiums are **higher for luxury SUVs**, especially via **branch sales** channels.

---

## ✅ Recommendations  

1. **Focus on Personal Auto Policies**  
   Maximize marketing and retention where CLV is highest.

2. **Target Employed Individuals**  
   Capitalize on income potential for upselling or policy upgrades.

3. **Tighten Risk Controls**  
   Consider higher premiums or enhanced underwriting for **large vehicles** and **luxury SUVs**.

4. **Leverage Branch Sales Channels**  
   Optimize pricing through channels where premiums perform better (e.g., branches).

---

## 📁 Repository Structure  

```
/insurance-auto-claims-analysis
├── /scripts                  # R scripts for EDA and visualizations
│   └── analysis.R
├── /visualizations           # Output plots (e.g., FIG.1 - FIG.6)
├── /docs                     # Supporting docs
│   └── executive_summary.md  # Executive summary of insights
├── README.md                 # Project overview
```

---

## ⚙️ Installation  

1. **Clone the repo**  
   ```bash
   git clone https://github.com/<your-username>/insurance-auto-claims-analysis.git
   cd insurance-auto-claims-analysis
   ```

2. **Install R and dependencies**  
   Ensure R ≥ 4.2.1 is installed, then:
   ```r
   install.packages(c("tidyverse", "RColorBrewer"))
   ```

---

## 🚀 Usage  

- Run the main script:
  ```r
  source("scripts/analysis.R")
  ```
- View visual insights in `/visualizations`
- Read the detailed narrative in `/docs/executive_summary.md`

---

## ⚠️ Limitations  

- **Geographic Restriction**: Data limited to southwest and western U.S.
- **EDA Focus**: Relationships are **correlational**, not causal
- **Missing External Factors**: Variables like seasonality or macroeconomics not included

---

## 🔮 Future Scope  

- Use **predictive modeling** (e.g., regression, clustering) to forecast claims or premiums  
- **Expand the dataset** to other regions or timeframes  
- Include external data like **economic indicators** or **seasonal effects** to improve insight depth

---
