# 📊 E-Commerce Dales Analysis Using PowerBI

## 📌Project Summary
A polished, interactive Power BI dashboard that transforms raw e-commerce transactions into clear business intelligence. The dashboard surfaces high-value KPIs, uncovers regional and seasonal patterns, and highlights product and customer segments that drive revenue and profit.

---

## 🎯Highlights
- **Deliverable**: Single Power BI report file `ECommerce_Sales.pbix` with all visuals, queries, and DAX measures.
- **Primary Objectives**: Monitor sales performance, identify growth opportunities, enable operational and strategic decisions.
- **Audience**: Data analysts, product managers, marketing teams, business stakeholders.

---

## 🚀Dashboard Features
- **Executive Summary**  
  - **Total Quantity**, **Total Profit**, **Average Sales Value (ASV)** and trend sparkline.
- **Geography**  
  - Top states by sales and profit; interactive state slicer.
- **Time Series**  
  - Monthly profit and revenue trends with quarter selection buttons for quick comparisons.
- **Product Performance**  
  - Profit by product and top-selling SKUs; category-level donut chart for share of sales.
- **Customer Insights**  
  - Top customers by revenue; cohort-ready metrics for retention analysis.
- **Payments and Channel Metrics**  
  - Payment method distribution; quick view of conversion levers.
- **Interactivity**  
  - Slicers by Date, State, Category, Payment Method, and dynamic drill-through pages.

## 🟰Key DAX Samples
- **Total Profit**
  ```DAX
  Total Profit = SUMX(Sales, Sales[Quantity] * (Sales[UnitPrice] - Sales[Cost]))
  ```
- **Average Sales Value**
  ```DAX
  ASV = DIVIDE([Total Revenue], DISTINCTCOUNT(Sales[OrderID]))
  ```
- **Year to Date Profit**
  ```DAX
  YTD Profit = TOTALYTD([Total Profit], 'Date'[Date])
  ```
## 📈Inferences from the E-commerce Sales Dashboard

#### 💹Sales Performance Overview
- **High volume, low margin**: Total Quantity is large (458K) while Total Profit is relatively low (37K), indicating high sales volume but slim average profit per unit.  
- **ASV strength**: **ASV = 291.85** shows average order value is moderate; increasing ASV will more efficiently raise profit than only increasing quantity.

#### 🌍Geographic Insights
- **Concentration in few states**: California, New York, and Texas are the top drivers of sales and profit; performance is concentrated geographically.  
- **Opportunity in mid-performing states**: States ranked below the top three show room for growth via targeted campaigns and localized offers.

#### 💡Product and Category Insights
- **Category leaders**: Electronics (40%) and Fashion (25%) are the biggest revenue contributors; they should receive priority for inventory and promotions.  
- **Profit by product skew**: A small set of products delivers most profit; identify and protect these SKUs from stockouts and margin erosion.

#### 🧑‍🤝‍🧑Customer Insights
- **Top customers matter**: A handful of customers account for disproportionate revenue; build retention playbooks (personal offers, loyalty incentives) for them.  
- **Cohort and repeat-purchase potential**: Use top-customer behaviour to define high-LTV cohorts and tailor upsell flows.

#### 💳Payment and Conversion Insights
- **Payment mix**: Credit Card 45% and Debit Card 30% dominate payments; optimizing for card conversions and reducing fees can improve margins.  
- **Alternative payment gaps**: PayPal (15%) and Others (10%) are smaller but valuable — test incentives to shift customers toward lower-cost or higher-converting methods if appropriate.

#### ☁️Temporal and Seasonality Insights
- **Monthly profit patterns**: Clear monthly variation suggests peak months where marketing ROI is higher and low months where cost control or re-engagement is needed.  
- **Quarter-level strategy**: Quarter buttons reveal that some quarters outperform others; align promotions, inventory buys, and staffing to quarter-specific demand.

#### 💹Profitability and Cost-Control Insights
- **Margin pressure**: Low total profit relative to volume implies margin compression; audit COGS, discounts, and fulfillment costs to reclaim margin.  
- **ASV and cross-sell levers**: Bundles, threshold-based free shipping, and recommended add-ons are high-leverage tactics to lift ASV and margin.

#### 🎬Actionable Recommendations
1. **Prioritize Electronics and Fashion** for promotions, premium placements, and inventory safety stock.  
2. **Run targeted regional campaigns** in California, New York, and Texas; test pilots in 2–3 mid-tier states to expand reach.  
3. **Introduce ASV-focused tactics**: product bundles, minimum-free-shipping thresholds, and post-checkout cross-sell.  
4. **Optimize payment costs**: renegotiate gateway fees, promote higher-margin payment flows, A/B test payment page layouts.  
5. **Protect top-SKU availability**: set higher reorder points and faster replenishment for highest-profit products.  
6. **Build customer retention programs** for top customers and high-LTV cohorts (personalized offers, early access).  
7. **Implement forecasting and cadence planning**: use monthly profit trends to plan promotions, staffing, and inventory by quarter.  
8. **Measure and iterate**: add KPI cards for margin per category, cost per acquisition by channel, and repeat-purchase rate; run short experiments and track lift.


