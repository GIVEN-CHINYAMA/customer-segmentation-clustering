markdown# 🛒 Customer Segmentation Using K-Means Clustering and RFM Analysis
### *An End-to-End Unsupervised Machine Learning Project*

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/GIVEN-CHINYAMA/customer-segmentation-clustering/blob/main/customer_segmentation_clustering.ipynb)
[![View on nbviewer](https://img.shields.io/badge/View-nbviewer-orange?style=flat&logo=jupyter)](https://nbviewer.org/github/GIVEN-CHINYAMA/customer-segmentation-clustering/blob/main/customer_segmentation_clustering.ipynb)
[![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat&logo=python&logoColor=white)](https://python.org)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-F7931E?style=flat&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Plotly](https://img.shields.io/badge/Plotly-Interactive_Charts-3D4DB7?style=flat&logo=plotly)](https://plotly.com)
[![Status](https://img.shields.io/badge/Status-Complete-2ecc71?style=flat)](https://github.com/GIVEN-CHINYAMA/customer-segmentation-clustering)

**Author:** Given Chinyama
**Institution:** Kwame Nkrumah University
**Date:** May 2026
**GitHub:** [github.com/GIVEN-CHINYAMA](https://github.com/GIVEN-CHINYAMA)

---

## 👆 Click "Open in Colab" Above to View the Full Notebook

> GitHub cannot render large notebooks with embedded visualisations. Click the **Open in Colab** badge above to view the complete project with all code, outputs, and interactive charts — no setup required.

---

## 📊 Results Summary

### Clustering Performance

| Metric | Value |
|---|---|
| **Algorithm** | K-Means++ |
| **Optimal K** | Selected via Elbow Method + Silhouette Score |
| **Silhouette Score** | Computed and validated per cluster |
| **Features Used** | Recency · Frequency · Monetary · Avg Order Value |
| **Preprocessing** | Log Transformation + StandardScaler |
| **Dimensionality Reduction** | PCA (2D + 3D projections) |

---

## 🗓️ Customer Segment Profiles (RFM — K-Means Output)

| Segment | Recency | Frequency | Monetary | Business Action |
|---|---|---|---|---|
| 💎 Champions | Very Low | Very High | Very High | Reward & retain at all costs |
| 🌟 Loyal Customers | Low | High | High | Upsell premium products |
| 🚀 Potential Loyalists | Low | Medium | Medium | Nurture with loyalty programme |
| ⚠️ At-Risk Customers | High | High | High | Win-back campaign urgently |
| 😴 Hibernating | Very High | Low | Low | Low-cost reactivation attempt |
| ❌ Lost Customers | Very High | Very Low | Very Low | Final re-engagement or write off |

> 🏆 **Champions and Loyal Customers** typically generate the majority of revenue despite being a minority of the customer base — confirming the **Pareto Principle (80/20 rule)** in retail data.

---

## 📁 Project Overview

Understanding *who your customers are* is one of the most valuable things a business can do. Customer segmentation — dividing a customer base into distinct groups based on purchasing behaviour — enables businesses to personalise marketing, improve retention, and maximise revenue.

This project builds an **end-to-end, production-grade unsupervised machine learning pipeline** that engineers RFM features from raw transactional data, applies K-Means clustering to discover natural customer groups, and delivers actionable business profiles for each segment.

### Why This Project Stands Out

Unlike most clustering tutorials that use iris or toy datasets, this project works with **541,909 real transactions** from a UK-based online retailer sourced from the UCI Machine Learning Repository. This makes it a genuine industry-relevant project applicable to any e-commerce, retail, or financial services business.

---

## 🔍 Problem Statement

> *"Which customers are our most valuable, which are at risk of leaving, and how do we treat each group differently to maximise lifetime value?"*

Retail and e-commerce businesses need a data-driven customer intelligence system that can:
- **Identify high-value customers** worth retaining at premium cost
- **Detect at-risk customers** before they churn permanently
- **Find dormant customers** who can be reactivated cheaply
- **Guide marketing teams** with segment-specific targeting strategies
- **Replace guesswork** with evidence-based customer intelligence

---

## 📦 Dataset

| Property | Details |
|---|---|
| **Source** | UCI Machine Learning Repository — Online Retail Dataset |
| **Records** | 541,909 transactions |
| **Coverage** | December 2010 to December 2011 |
| **Business** | UK-based online retailer (gift and homewares) |
| **Variables** | InvoiceNo · StockCode · Description · Quantity · InvoiceDate · UnitPrice · CustomerID · Country |
| **Customers** | ~4,300 unique customers after cleaning |
| **Countries** | 38 countries (UK = ~92% of transactions) |

### RFM Features Engineered

| Feature | Definition | Business Meaning |
|---|---|---|
| **Recency** | Days since last purchase | How recently did the customer buy? |
| **Frequency** | Number of unique invoices | How often do they buy? |
| **Monetary** | Total revenue generated (£) | How much do they spend? |
| **Avg Order Value** | Monetary ÷ Frequency | What is their typical basket size? |

---

## 🗂️ Project Stages

| Stage | Description |
|---|---|
| Stage 1 | Environment setup — library installation and imports |
| Stage 2 | Data collection — UCI Online Retail Dataset (541,909 transactions) |
| Stage 3 | Data overview and quality check — shape, dtypes, missing values |
| Stage 4 | Data cleaning — cancellations, nulls, negative quantities, outliers |
| Stage 5 | RFM feature engineering — Recency, Frequency, Monetary, Avg Order Value |
| Stage 6 | RFM exploratory data analysis — distributions, correlations, pairplots |
| Stage 7 | Feature scaling — log transformation + StandardScaler |
| Stage 8 | Optimal K selection — Elbow Method + Silhouette Score (K=2 to 11) |
| Stage 9 | K-Means clustering — K-Means++ with n_init=20 |
| Stage 10 | Cluster analysis — radar charts, box plots, RFM profiling |
| Stage 11 | Business segment labelling — Champions, Loyal, At-Risk, etc. |
| Stage 12 | PCA visualisation — 2D and 3D projections |
| Stage 13 | Interactive visualisations — Plotly 3D scatter, treemap, bar charts |
| Stage 14 | Business intelligence report — revenue by segment + recommendations |

---

## 🛠️ Technologies Used

| Tool | Purpose |
|---|---|
| Python 3.10+ | Core language |
| Scikit-learn | K-Means clustering, PCA, Silhouette Score |
| Pandas / NumPy | Data manipulation and RFM engineering |
| Matplotlib / Seaborn | Static visualisations (12+ charts) |
| Plotly | Interactive 3D scatter, treemap, bar charts |
| Google Colab | Cloud execution platform |

---

## 💡 Key Findings

- **Champions and Loyal Customers** generate the majority of total revenue despite being a minority of the customer base — the Pareto Principle holds strongly in this dataset
- **At-Risk customers** show high historical frequency but increasing recency — a targeted win-back campaign can recover significant revenue before they churn permanently
- **New Customers** have low frequency by definition — onboarding campaigns in the first 30 days dramatically improve long-term retention rates
- **Hibernating and Lost** segments should receive low-cost reactivation attempts only — high-spend campaigns on these groups produce poor ROI
- **Log transformation** was essential — raw RFM distributions were severely right-skewed, and clustering on untransformed data produced poor, unbalanced segments
- **K-Means++** initialisation with n_init=20 produced significantly more stable and reproducible clusters than random initialisation
- **PCA 2D projection** captured the majority of variance and clearly separated the Champion segment from low-value segments visually

---

## 📸 Visualisations

The notebook generates **15 publication-quality charts**:

| # | Chart | Description |
|---|---|---|
| 1 | RFM Distributions | Histograms for all 4 RFM features |
| 2 | RFM Box Plots | Outlier detection per feature |
| 3 | RFM Pairplot | Scatter plots for all feature pairs |
| 4 | Correlation Heatmap | RFM feature correlation matrix |
| 5 | Log Transform | Before vs after transformation (8 panels) |
| 6 | Elbow Method | Inertia vs K (K=2 to 11) |
| 7 | Silhouette Scores | Score vs K with best K highlighted |
| 8 | Cluster Sizes | Bar chart of customers per segment |
| 9 | Radar Charts | RFM normalised profile per cluster |
| 10 | RFM Box by Cluster | Recency, Frequency, Monetary per segment |
| 11 | PCA 2D Scatter | All customers projected to 2D |
| 12 | PCA 3D Scatter | All customers projected to 3D |
| 13 | Plotly 3D Interactive | Interactive RFM space exploration |
| 14 | Revenue Treemap | Segment area = revenue contribution |
| 15 | Silhouette Plot | Per-sample silhouette coefficients |

---

## 💼 Business Insights & Marketing Recommendations

### Segment Strategy

| Segment | Strategy | Channel | Budget Priority |
|---|---|---|---|
| 💎 Champions | VIP programme, early access, referral incentives | Email · WhatsApp · Personal | 🔴 Highest |
| 🌟 Loyal Customers | Loyalty points, upsell premium lines | Email · App push | 🔴 High |
| 🚀 Potential Loyalists | Second-purchase discount, onboarding flow | Email · SMS | 🟡 Medium |
| ⚠️ At-Risk | Personalised win-back offer within 30 days | Email · Retargeting ads | 🔴 High |
| 😴 Hibernating | Low-cost re-engagement — seasonal promotion | Email only | 🟢 Low |
| ❌ Lost | Final reactivation email then suppress | Email only | 🟢 Minimal |

### Actionable Recommendations

1. **Protect Champions first** — assign a dedicated account manager or VIP tier; losing one Champion costs more than acquiring ten new customers
2. **Launch a 30-day At-Risk alert** — automatically flag customers whose recency crosses a threshold and trigger a personalised win-back sequence
3. **Differentiate onboarding** — new customers who make a second purchase within 30 days have significantly higher lifetime value; automate a second-purchase incentive
4. **Build a monthly scoring pipeline** — re-run RFM and K-Means every month so segment labels stay current as customer behaviour evolves
5. **A/B test campaigns per segment** — never send the same message to Champions and Lost customers; measure uplift vs control group for each segment independently
6. **Integrate with CRM** — push segment labels directly into Salesforce, HubSpot, or Mailchimp for automated campaign triggering

---

## 🚀 How to Run

### Option 1 — Google Colab (Recommended)

Click the **Open in Colab** badge at the top of this page. All dependencies install automatically in Cell 3. No local setup required. Total runtime: approximately **3–5 minutes**.

### Option 2 — Run Locally

```bash
git clone https://github.com/GIVEN-CHINYAMA/customer-segmentation-clustering.git
cd customer-segmentation-clustering
pip install pandas numpy matplotlib seaborn scikit-learn plotly openpyxl jupyter
jupyter notebook customer_segmentation_clustering.ipynb
```

---

## 📌 Repository Structure
customer-segmentation-clustering/
│
├── customer_segmentation_clustering.ipynb   ← Complete end-to-end notebook
├── README.md                                ← This file
├── .gitignore                               ← Python gitignore
└── LICENSE                                  ← MIT License

---

## 🚀 Future Work

- [ ] Add **CLV (Customer Lifetime Value)** as a 4th clustering feature
- [ ] Try **DBSCAN** for density-based clustering — handles non-spherical shapes
- [ ] Try **Gaussian Mixture Models** for soft/probabilistic cluster assignment
- [ ] Build a **Streamlit dashboard** — live RFM scoring for new transaction uploads
- [ ] **Deploy as a monthly pipeline** with automated email alerts per segment
- [ ] **Integrate with real CRM** — push labels to Salesforce or HubSpot via API
- [ ] Add **cohort analysis** — track how segments evolve month over month
- [ ] Apply to **Zambian retail/mobile money data** for a locally relevant extension

---

## 👤 Author

**Given Chinyama**
🎓 Kwame Nkrumah University
🌍 Lusaka, Zambia
🐙 [github.com/GIVEN-CHINYAMA](https://github.com/GIVEN-CHINYAMA)

---

## 📄 License

This project is licensed under the **MIT License** — free to use, adapt, and build on with attribution.

---

## ⭐ Show Your Support

If you found this project useful or learned something from it, please consider giving it a **⭐ star** on GitHub. It helps others discover the project and means a lot!

---

Given Chinyama, 2026*
