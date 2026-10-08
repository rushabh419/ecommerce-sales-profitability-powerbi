### 1. Project Title
* Title: E-Commerce Sales & Profitability Analytics Dashboard
* Repository Name: ecommerce-sales-profitability-powerbi

### 2. Short Description
* An end-to-end e-commerce business intelligence project built in Microsoft Power BI analyzing multi-category retail sales, customer spending, and regional profitability.
* Transforms raw transactional and fulfillment records into an interactive executive dashboard featuring custom KPI scorecards, conditional profit-loss formatting, and multi-level dynamic slicers.

### 3. Purpose
* Monitor Financial Performance: Track gross revenue, net profit margins, total unit sales, and Average Order Value (AOV) across fiscal quarters.
* Identify Profit Leaks vs. Profit Drivers: Pinpoint loss-making months and product lines versus top-performing categories using dynamic visual thresholds.
* Segment Product & Payment Mix: Break down sales shares across Clothing, Electronics, and Furniture while analyzing customer preferred payment modes (COD, UPI, Credit Card, EMI).
* Understand Regional & Customer Concentration: Isolate top-grossing states and high-spending VIP customers to direct marketing spend and inventory placement.
* Demonstrate Full-Lifecycle BI Execution: Showcase relational data modeling (1-to-Many joins), Power Query ETL, DAX calculated columns, and dashboard UI styling.

### 4. Tech Stack
* Business Intelligence & Visualization: Microsoft Power BI Desktop
* Data Transformation & ETL: Power Query
* Data Modeling & Analytics: DAX (Data Analysis Expressions) / Calculated Columns
* Data Storage / Source: CSV Flat Files

### 5. Example Walkthrough
* Use Case: Diagnosing quarterly profitability trends and regional revenue drivers.
* Action: Select "Q1" in the quarter tile slicer and choose "Maharashtra" from the state drop-down filter.
* Observed Insight: Clothing represents over 60% of order volume with steady positive margins, whereas specific furniture sub-categories incur periodic losses; Cash on Delivery (COD) and UPI remain the dominant payment channels.
* Conclusion: Highlights the need to renegotiate vendor procurement costs on underperforming sub-categories while running retargeting campaigns for high-spending customers in key urban states.

### 6. Data Source
* Dataset: E-Commerce Retail Store Dataset (2 relational tables)
* Format: .csv (Orders & Details)
* Key Attributes:
  * Orders Table:
    * Order ID: Unique transaction identifier
    * Order Date: Transaction timestamp (modeled into date hierarchies)
    * CustomerName: Customer full name
    * State: State of purchase (e.g., Maharashtra, Delhi, Uttar Pradesh)
    * City: City of delivery (e.g., Pune, Mumbai, Indore, Delhi)
  * Details Table:
    * Order ID: Relational foreign key linking to Orders
    * Amount: Transaction sales value
    * Profit: Net profit or loss recorded on the line item
    * Quantity: Units ordered
    * Category: Primary merchandise sector (Clothing, Electronics, Furniture)
    * Sub-Category: Granular classification (e.g., Sarees, Printers, Bookcases)
    * PaymentMode: Checkout method (COD, UPI, Credit Card, Debit Card, EMI)

### 7. Features & Highlights
* Relational Star-Schema Modeling: Configured one-to-many relationship linking `Orders[Order ID]` to `Details[Order ID]` for seamless cross-table filtering.
* Executive KPI Cards: Real-time metric cards showing Total Revenue (Sum of Amount), Net Profit, Total Quantity Sold, and Average Order Value (AOV).
* Conditional Monthly Profit-Loss Column Chart: Clustered column visual applying rule-based conditional formatting (blue for profitable months, orange/red for net loss months).
* Top N Sub-Categories Bar Chart: Ranked visual utilizing Power BI Top N visual filtering to highlight the 5 most profitable sub-categories.
* Category & Payment Mode Donut Charts: Proportional share visuals mapping order volume percentages by merchandise category and payment method.
* Geographic & Customer Leaderboards: Horizontal bar charts detailing top revenue-generating states and top high-value individual customers.
* Dynamic Interactive Slicers: Interactive tile slicer for quarterly periods (Q1, Q2, Q3, Q4) and a searchable drop-down slicer for state-level drill-downs.

### 8. Business Impact & Insights
* Dominant Product Sector: Clothing drives the vast majority of volume (>60%), serving as the store's primary customer acquisition engine, while Electronics commands higher ticket sizes.
* Regional Revenue Concentration: Top states (Maharashtra, Delhi, Uttar Pradesh) generate disproportionate shares of overall turnover, justifying localized warehouse hubs to reduce shipping lead times.
* Payment Channel Optimization: Heavy reliance on COD and UPI indicates an Indian digital commerce profile; offering small prepaid incentives on UPI could cut COD return-to-origin (RTO) friction.
* Strategic Recommendations:
  * Implement loyalty tiers and personalized discount codes for top customers to boost repeat purchases.
  * Adjust minimum order thresholds to lift the Average Order Value (AOV) on low-margin sub-categories.
 
  * ### 9.	Screenshots / Demos
Show what the dashboard looks like.
Example: ![Dashboard Preview](https://github.com/rushabh419/ecommerce-sales-profitability-powerbi/blob/main/Ecommerce_Sales_Dashbord_1.png)
