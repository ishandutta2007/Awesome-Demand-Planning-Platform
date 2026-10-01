# Awesome-Demand-Planning-Platform

# Top Demand Planning Platforms Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Demand Forecasting, Inventory Optimization, S&OP & Supply Chain Planning*
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Demand Planning**. These tools help supply chain teams forecast demand, optimize inventory levels, and align sales and operations planning (S&OP).

**Examples** include Anaplan, RELEX Solutions, Blue Yonder, o9 Solutions, ToolsGroup, Kinaxis, River Logic, FuturMaster, Gains Systems, Logility, Netstock, and Lokad (the category leaders).

**Open-source emphasis**: Demand planning has a **focused open-source ecosystem**. **planr** is the most mature open-source R package for demand planning, providing DRP (Distribution Requirement Planning), projected inventories, coverage calculations, and constrained demand functions . **Advanced Demand Forecasting and Inventory Optimization** provides a complete Python-based system with multiple forecasting models (SES, Holt's, Holt-Winters), EOQ, safety stock, and a Streamlit dashboard . This section documents these focused solutions honestly—the open-source ecosystem remains significantly behind commercial platforms in ML sophistication and enterprise integration.

Contributions welcome! Open an Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Anaplan](https://www.anaplan.com/)**  
  Cloud-based planning platform for connected planning across finance, supply chain, and sales. Uses in-memory OLAP architecture for rapid model recalculation and multi-dimensional planning. **Note**: Exclusively cloud-based; no on-premises deployment option .

- **[RELEX Solutions](https://www.relexsolutions.com/)**  
  Unified supply chain and retail planning platform. Provides demand forecasting, merchandise planning, supply chain optimization, and operations planning for retailers and consumer brands .

- **[Blue Yonder](https://blueyonder.com/)**  
  AI-powered supply chain orchestration platform. Provides demand planning, inventory optimization, S&OP, and logistics management with patented algorithms covering every sales pattern from slow-moving to highly seasonal .

- **[o9 Solutions](https://o9solutions.com/)**  
  AI-powered integrated business planning platform. Provides real-time data for supply chain decisions across demand, supply, inventory, and S&OP .

- **[ToolsGroup](https://www.toolsgroup.com/)**  
  Supply chain planning and optimization software. Provides demand forecasting, operations planning, demand sensing, and data unification. Known for probabilistic forecasting and Monte Carlo simulation for safety stock optimization .

- **[Kinaxis](https://www.kinaxis.com/)**  
  AI-powered supply chain orchestration platform for end-to-end planning. Provides demand, supply, inventory, S&OP, and logistics management with rapid response capabilities .

- **[Netstock](https://www.netstock.com/)**  
  Cloud-based inventory and demand planning solution that integrates with ERPs. Provides AI-powered demand forecasting, inventory optimization, and insights to avoid stockouts while reducing tied-up capital. **Note**: Certified on Microsoft AppSource, integrates with Dynamics 365 Business Central and other ERPs .

- **[Lokad](https://www.lokad.com/)**  
  Quantitative supply chain optimization platform. Provides demand forecasting and inventory optimization with a focus on ROI-driven probabilistic forecasting and parts optimization .

## Open-Source GitHub Projects

### Demand Planning & Inventory Optimization Frameworks

- **[planr](https://github.com/nikonguyen/planr)**  
  **The most mature open-source R package for demand and supply planning.** Provides comprehensive **DRP (Distribution Requirement Planning)** functionality. **Key features**: `drp()` function calculates Replenishment Plans with projected inventories and coverages; `inv_to_cov()` converts projected inventories to projected coverage in periods; `const_dmd()` calculates constrained demand based on projected inventory availability; `proj_git()` projects Goods In Transit with ETA/ETD tracking . **Input requirements**: Just 5 key features—a DFU (item × location), Period (weekly/monthly buckets), Demand (quantity planned to be consumed), Opening Inventory (units at horizon start), and Supply Plan . **Frozen/Free Horizon** parameter supports production plan consideration. **Installation**: `install.packages("planr")`. **Best for**: Supply chain analysts and data scientists needing a lightweight, code-based DRP engine.

- **[Advanced Demand Forecasting and Inventory Optimization](https://github.com/Malay19/Advanced-Demand-Forecasting-and-Inventory-Optimization-Using-Machine-Learning)**  
  **Complete end-to-end Python solution for demand forecasting and inventory optimization.** **Key features**: Multiple forecasting models—**Simple Exponential Smoothing (SES)**, **Holt's Linear Trend**, and **Holt-Winters Seasonal**—with automatic model selection per SKU based on accuracy metrics (MAPE, RMSE); **Inventory optimization** calculates EOQ, Safety Stock, and Reorder Points considering demand and lead time variability; **KPI reporting** for Inventory Turnover, Fill Rate, Days of Supply, and SKU Risk Levels; **Interactive Streamlit dashboard** with forecasting charts, inventory optimization views, order recommendations, and simulation tools . **Tech stack**: Python, Pandas, NumPy, Statsmodels, Plotly, Streamlit. **Outputs**: CSV files for inventory results, demand forecasts, model metrics, and KPI summaries. **Best for**: Python developers and data scientists wanting a complete demand planning toolkit.

### Machine Learning Forecasting Approaches

- **[Prophet (Meta)](https://github.com/facebook/prophet)**  
  Open-source forecasting tool from Meta. Handles seasonality, holidays, and missing data robustly. **Best for**: Business time-series forecasting with interpretable results. Works well for campaign metrics with strong weekly/monthly seasonality .

- **[Statsmodels SARIMA](https://github.com/statsmodels/statsmodels)**  
  Statistical forecasting with Seasonal ARIMA models. **Best for**: Regular seasonal patterns where simpler models outperform complex ones. Email open rates show stable weekly patterns (Tuesday morning opens 23% higher than Friday afternoon) where SARIMA performs well .

- **[XGBoost](https://github.com/dmlc/xgboost)**  
  Gradient boosting for demand forecasting with external features. **Best for**: Forecasts correlating with fuel prices, model releases, competitor pricing, weather, and marketing spend. **Ensemble approach**: Averaging Prophet, SARIMA, and XGBoost predictions with weights based on holdout performance often outperforms any single model .

### Additional Strong Open-Source Options

- **DRP & Supply Planning**: **planr** (R package, DRP, projected inventories, constrained demand) .
- **Demand Forecasting**: **Advanced Demand Forecasting** (Python, SES/Holt-Winters, EOQ, Streamlit dashboard) .
- **Time Series Models**: **Prophet** (Meta, seasonality handling), **Statsmodels SARIMA** (statistical forecasting), **XGBoost** (external features, ensemble) .
- **ERP Foundations**: **Odoo** (open-source ERP with inventory and manufacturing modules adaptable for demand planning) .

**Frameworks for building custom systems**: Combine **planr** for DRP and replenishment planning, **Advanced Demand Forecasting** for ML-based forecasting with EOQ and safety stock, **Prophet** or **XGBoost** for time-series forecasting with external features, and **Odoo** for ERP integration. Add **PostgreSQL** for persistence and **Docker** for deployment.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Demand planning platforms handle sensitive supply chain and financial data; ensure proper access controls and compliance with data protection regulations.
- **Open-source reality**: The open-source ecosystem for demand planning is **focused but limited compared to commercial platforms**. **planr** provides a mature R-based DRP engine with projected inventories and constrained demand . **Advanced Demand Forecasting** offers a complete Python toolkit with multiple forecasting models and inventory optimization . However, **commercial platforms** (Anaplan, RELEX, Blue Yonder, o9 Solutions, Kinaxis) provide **enterprise-grade ML sophistication, real-time data integration, multi-echelon optimization, and integrated S&OP workflows** that open-source alternatives cannot match without significant development. The open-source path is most viable for **specific DRP calculations, forecasting model experimentation, or organizations with strong data science capacity** seeking lightweight alternatives.

---

**Made for supply chain analysts, demand planners, inventory managers, and data scientists.**
Let's make demand planning more open, transparent, and data-driven.
