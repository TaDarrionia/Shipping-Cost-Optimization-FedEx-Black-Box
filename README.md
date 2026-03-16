# Shipping Cost Optimization & Logistics Analytics Engine
This project builds a data-driven logistics analytics and optimization engine designed to analyze and reduce shipping costs across a multi-store fulfillment network. The pipeline integrates order data, carrier shipping records, geographic location data, and dimensional shipment characteristics to quantify the drivers of shipping cost and simulate optimal fulfillment strategies.

The workflow constructs a multi-phase analytical framework that progresses from empirical baseline analysis to predictive modeling and ultimately to an origin optimization simulation capable of identifying the most cost-efficient fulfillment store for each order.
The system was built to support carrier negotiation strategy, operational efficiency improvements, SKU packaging optimization, and fulfillment network planning.

# Key Objectives

The project answers several operational and strategic logistics questions:

• **Shipping Cost Drivers:** What factors most influence parcel shipping cost?

• **Distance Impact:** How do zone distance and service level affect shipping spend?

• **DIM Exposure:** Which stores generate the highest dimensional shipping charges?

• **SKU Cost Risk:** Which products disproportionately drive logistics cost?

• **Fulfillment Optimization:** What is the optimal origin store for each order?

• **Network Savings:** How much shipping cost reduction is possible through smarter routing?


# Analytical Pipeline
The analysis is implemented as an 8-phase pipeline:

**Phase 1 — Empirical Shipping Cost Foundation**  
Builds the unified logistics dataset by merging multiple operational data sources.

**Data sources include:**

	• Order fulfillment data
	• Carrier parcel invoices
	• Internal shipping charge records
	• Store location coordinates
	• U.S. ZIP code geolocation data

**Key outputs:**

	• Shipment-level master dataset
	• Revenue attribution by order
	• Weight, dimensional, and pricing zone features
	• Shipping cost to revenue ratios
	• Margin proxy calculations

**Phase 2 — Descriptive Baseline Analysis**  
Establishes a pre-negotiation shipping cost baseline.


**Key metrics generated:**

	• Total shipping spend
	• Shipping cost per order and per shipment
	• Shipping cost as a percentage of revenue
	• Service-level mix analysis
	• Zone distribution analysis
	• Store-level shipping performance

This phase provides the baseline operational benchmark used for later optimization and negotiation analysis.


**Phase 3 — Store-Specific Zone Cost Gradients**  
Analyzes how shipping cost increases with zone distance for each fulfillment store.

**Outputs include:**

	• Store × Zone shipping cost tables
	• Incremental $ cost per zone increase
	• Cost per pound analysis
	• Zone cost heatmap matrices

This reveals which stores experience steeper cost escalation with distance.


**Phase 4 — Dimensional Shipping Economics**  
Examines the impact of dimensional weight charges on shipping cost.

**Key analyses:**

	• DIM rate by store
	• DIM rate by SKU
	• DIM premium by weight band
	• Volume breakpoint analysis
	• Marginal shipping cost per cubic centimeter
	• Weight reporting compliance metrics

This phase identifies packaging inefficiencies and dimensional cost exposure.


**Phase 5 — Feature Importance Model**  
Builds a predictive shipping cost model using linear regression.

**Features analyzed:**

	• Shipment weight
	• Pricing zone
	• Distance
	• DIM flag
	• Service type
	• Fulfillment store

**Model outputs include:**

	• Feature coefficients ($ impact per driver)
	• Percent contribution of cost drivers
	• Model performance metrics (R² and MAE)

This model quantifies the economic impact of each shipping cost driver.


**Phase 6 — SKU Shipping Risk Dashboard**  
Evaluates shipping risk at the product level.

**Metrics generated:**

	• DIM rate per SKU
	• Shipping cost as % of revenue
	• Average weight and volume
	• Shipping zone exposure

**SKUs are classified into:**

	• High Risk
	• Medium Risk
	• Low Risk

This analysis identifies products that create disproportionate logistics costs.


**Phase 7 — Store Performance Scorecard**  
Measures fulfillment efficiency across stores.

**Metrics include:**

	• DIM rate
	• Shipping cost vs revenue
	• Weight and volume reporting variance
	• SKU complexity handled

A composite performance score ranks stores by operational efficiency.


**Phase 8 — Origin Optimization Engine**  
The final phase simulates the optimal fulfillment origin for each order.

**For each order, the engine:**

	1. Calculates distance from every store
	2. Estimates shipping zone from distance
	3. Applies model-derived shipping cost drivers
	4. Adjusts cost for dimensional penalties
	5. Simulates shipping cost from each possible origin

**Outputs include:**

	• Predicted shipping cost for every store–order combination
	• Optimal origin store per order
	• Estimated cost savings versus actual fulfillment

This phase enables network-level fulfillment optimization.

# Technologies Used

**Python ecosystem tools:**

	• pandas – data manipulation and transformation
	• numpy – numerical computation
	• scikit-learn – regression modeling
	• xlsxwriter – automated Excel reporting
	• math / haversine calculations – geospatial distance modeling

# Data Inputs

**The pipeline integrates multiple operational datasets:**

	• Order fulfillment records
	• Carrier parcel invoice data
	• Internal shipping tracking data
	• Store location coordinates
	• U.S. ZIP code latitude/longitude reference data

All input files are provided as Excel datasets.

# Output Deliverables

**The script automatically generates analytical reports including:**

	• Shipping cost baseline analysis
	• Store-level logistics performance dashboards
	• SKU shipping risk tables
	• Dimensional shipping impact analysis
	• Feature importance modeling outputs
	• Fulfillment origin optimization simulation

All outputs are exported as Excel workbooks for executive analysis and visualization.

# Use Cases

**This project can support:**

	• Carrier rate negotiations
	• Fulfillment network design
	• Store shipping performance management
	• Packaging optimization initiatives
	• SKU logistics profitability analysis
	• Strategic logistics cost reduction

# Future Enhancements

**Potential improvements include:**

	• Machine learning models (Random Forest / Gradient Boosting)
	• Real carrier zone mapping integration
	• Monte Carlo logistics simulations
	• Dynamic routing optimization
	• Interactive dashboards (Power BI / Tableau)
• API integration with fulfillment systems
