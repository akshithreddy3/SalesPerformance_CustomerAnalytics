# Sales Performance & Customer Analytics — SuperStore

**Author:** Akshith Reddy  

## Overview
This project presents a complete **end-to-end data analytics workflow** using a SuperStore sales dataset.  
It demonstrates the process of cleaning, analyzing, and deriving insights from retail sales data, following the **CRISP-DM methodology**.

## Dataset
- **File:** `SuperStore_Sales.csv`  
- **Rows:** ~9,800  
- **Columns:** Order ID, Order Date, Ship Date, Ship Mode, Customer ID, Customer Name, Segment, Country, City, State, Postal Code, Region, Product ID, Category, Sub-Category, Product Name, Sales  
- **Date Range:** 2015-01-03 → 2018-12-30  

## Methodology (CRISP-DM)
1. **Business Understanding** — identify key objectives (sales growth, category performance, shipping efficiency, customer retention).  
2. **Data Understanding** — audit schema, nulls, duplicates; validate date parsing.  
3. **Data Preparation** — parse dates, engineer time features, calculate shipping lead times.  
4. **Modeling / Analysis**  
   - **Exploratory Analysis**: Trends (monthly/YoY), mix (category, region, segment).  
   - **Customer Analytics**: RFM segmentation, monthly cohort retention.  
   - **Operational Analytics**: SLA analysis of shipping lead times.  
   - **Associations**: Market-basket analysis with lift.  
   - **ABC Classification**: Pareto analysis of products.  
   - **Forecasting**: Naive & seasonal-naive monthly forecasts.  
   - **Outlier Detection**: High AOV orders.  
5. **Evaluation** — summarize KPIs, validate patterns against expectations.  
6. **Deployment / Recommendations** — translate findings into business actions.

## Key Insights
- **Sales Growth:** $2.26M total; YoY growth +30.6% in 2017, +20.3% in 2018.  
- **Mix Leaders:** Technology is the largest category (~$827K). Phones & Chairs are the top sub-categories.  
- **Regional Split:** West and East dominate sales; Central and South lag.  
- **Customer Value:** 793 unique customers, segmented into **VIP, Loyal, Regular, At-Risk** via RFM.  
- **Retention:** Cohorts show steady drop-off after first month; opportunities for retention campaigns.  
- **Shipping:** Average ship lead time ~4 days; 90% of orders delivered ≤6 days.  
- **Cross-Sell:** Market-basket lift reveals strong product associations for bundle offers.  
- **Products:** Top 20% of products drive ~80% of sales (ABC classification).  
- **Forecasting:** Simple seasonal-naive models capture annual trends.  
- **Outliers:** Few very large orders detected (3σ rule).

## Deliverables
- 📓 **Notebook**: [SalesPerformance_and_CustomerAnalytics.ipynb](./SalesPerformance_and_CustomerAnalytics.ipynb)  
- 📊 Exportable tables for KPIs, cohorts, RFM, ABC, etc.  
- 📈 Visuals: trends, mix, shipping lead times, RFM distributions, retention heatmap, Pareto chart, forecasts.

## Recommendations
- Scale winning categories & regions (Technology, Phones, West/East).  
- Improve retention for **At-Risk** customers; reward **VIP/Loyal** segments.  
- Optimize shipping SLAs in slower modes/regions.  
- Use cross-sell bundles suggested by basket analysis.  
- Protect & grow **A-class** products, rationalize **C-class** items.  
- Upgrade forecasting to ARIMA/Prophet for higher accuracy if required.

---

### How to Run
1. Clone this repo  
2. Place `SuperStore_Sales.csv` in the project folder  
3. Open and run `SalesPerformance_and_CustomerAnalytics.ipynb` in Jupyter/VS Code  
4. (Optional) Uncomment export functions in Appendix to save CSV outputs  

---

💡 This project showcases a **complete data analytics pipeline**: from cleaning and exploration through advanced customer, operational, and product analytics, to business-ready recommendations.
