# **GOPALS: Geospatial Optimization and Portfolio Allocation using Landscape Segmentation**
*A novel portfolio optimization framework for robust portfolio allocation.*

<img src="/Indian_Markets/GOPALS_img.png" width="50%">

## **Research Papers**

This repository supports ongoing research on portfolio optimization and market simulations based on GOPALS. Below are published papers based on the GOPALS framework:

1. **Robust Portfolio Optimization using GOPALS: Geospatial Optimization and Portfolio Allocation using Landscape Segmentation**  
   - *Authors:* Jatin Patni, Ritabrata Bhattacharyya
   - *Published on:* [SSRN](https://ssrn.com/abstract=5057384)  
   - *Abstract:* Portfolio Optimization is an important area of research in Financial Investments. The traditional mean-variance framework for portfolio optimization is very sensitive to the estimation errors in the expectations of returns and covariances, and leads to suboptimal port folios. Even after using techniques such as shrinkage methods, robust optimization, and resampling methods, we are unable to address these limitations comprehensively. 
This study introduces GOPALS: Geospatial Optimization and Portfolio Allocation using Landscape Segmentation, a simulation-based portfolio optimization framework designed to overcome these limitations and improve the robustness of the portfolio optimization process. 
GOPALS methodology relies on simulating market scenarios and identifying ”stable regions” in the high-dimensional portfolio weight space (i.e. regions where portfolio allocations consistently perform favorably across varying market conditions) using clustering methods. By restricting the choice of portfolio allocations from such stable regions, the portfolio performance can be shown to be consistently favorable and robust to estimation errors.
GOPALS is applied to a handpicked universe of Indian Equity Mutual Funds, with practical constraints-such as long-only positions and concentration limits-in order to reflect real-world constraints of investing. The robustness of GOPALS is shown via backtests per formed over multiple historical regimes.
GOPALS offers a resilient approach to portfolio construction, hence it has considerable promise, not only in academic research, but also in the real world of financial investments. It offers investors and portfolio managers a new tool for navigating uncertain markets across different asset classes and global investment universes.

---

## **Overview**

This repository supports ongoing research on **GOPALS (Geospatial Optimization and Portfolio Allocation using Landscape Segmentation)**, a portfolio optimization framework that identifies **stable regions in portfolio weight space**, offering consistent performance across diverse market conditions.

This repository provides the source code, data sets and results for the paper **"GOPALS: Geospatial Optimization and Portfolio Allocation using Landscape Segmentation."** GOPALS introduces a robust portfolio optimization framework that identifies **stable regions in portfolio weight space**, offering consistent performance across various market scenarios.

The framework combines advanced optimization techniques, Monte Carlo simulations, and machine learning (e.g., clustering, t-SNE) to construct portfolios that are resilient to estimation errors in future returns and risks.

The GOPALS framework is designed to adapt to various asset classes and markets. While the current implementation focuses on Indian Equity Mutual Funds, future extensions will cover:
- **Indian Stock Markets**
- **US ETF Markets**
- **Global Asset Classes (e.g., Bonds, Commodities, Real Estate)**

---


## **Current Features**

- Portfolio optimization using Monte Carlo market simulations and clustering.
- Identification of stable regions in portfolio weight space using clustering and t-SNE.
- Backtesting across historical market regimes (2020–2023).
- Comparison with traditional MVO, equal-weighted strategies and benchmark market strategies.
- Metrics reported: Sharpe Ratio, Sortino Ratio, Max Drawdown, Annual Return, and Volatility.

---


## **Getting Started**

### **Step 1: Data Processing and EDA:**
- **Notebook:** [Step 1 - Data Processing and EDA.ipynb](https://github.com/JatinPatni/GOPALS/blob/master/Indian_Markets/Equity_Mutual_Funds_v1/notebooks/Step%201.2%20-%20Data%20Processing%20and%20EDA.ipynb)
- **Description:** Selection of Market and Universe. This code is used to select the universe of mutual funds, look at the heatmap of correlations and apply hierarchical clustering to choose one mutual fund for
each of the 25 clusters to reduce the universe to 25 mutual funds.

<img src="/Indian_Markets/Equity_Mutual_Funds_v1/results/figures/all_mfs.png" width="50%">
<img src="/Indian_Markets/Equity_Mutual_Funds_v1/results/figures/hierarchical_clustering_results.png" width="50%">
<img src="/Indian_Markets/Equity_Mutual_Funds_v1/results/figures/hist_dist1.png" width="50%">

### **Step 2: Generate Market Scenarios:**
- **Notebook:** [Step 2 - Generate Market Scenarios-Monte Carlo.ipynb](https://github.com/JatinPatni/GOPALS/blob/master/Indian_Markets/Equity_Mutual_Funds_v1/notebooks/Step%202.2%20-%20Generate%20Market%20Scenarios%20-%20Simulations.ipynb)
- **Description:** In this code we generate historical as well as futuristic market scenarios by randomly introducing noise to historical risk, return and correlation measurements.

### **Step 3: Generating Portfolio Runs:**
- **Notebook:** [Step 3 - Generate_Portfolio_runs_Monte_Carlo_Scenarios.ipynb](https://github.com/JatinPatni/GOPALS/blob/master/Indian_Markets/Equity_Mutual_Funds_v1/notebooks/Step%203.2%20-%20Generate_Portfolio_runs_Monte_Carlo_Scenarios.ipynb)
- **Description:** In this step, we generate multiple portfolio allocations and record the performance of these portfolio allocations across the market scenarios that we generated in the previous step

### **Step 4: Identifying Stable Regions:**
- **Notebook:** [Step 4 - Identify Stable Regions-percen0.95_MCsim.ipynb](https://github.com/JatinPatni/GOPALS/blob/master/Indian_Markets/Equity_Mutual_Funds_v1/notebooks/Step%204%20-%20Identify%20Stable%20Regions-percen0.95%20Monte%20Carlo%20simulation%20runs.ipynb)
- **Description:** In this step, we filter out portfolios which perform favourably and visualise clusters in high dimensional space using t-SNE algorithm

<img src="/Indian_Markets/Equity_Mutual_Funds_v1/results/figures/tsne.png" width="50%">

### **Step 5: Backtest GOPALS Strategy:**
- **Notebook:** [Step 5 - Generate GOPALS portfolio weights Strategy_2.3-MCSim.ipynb](https://github.com/JatinPatni/GOPALS/blob/master/Indian_Markets/Equity_Mutual_Funds_v1/notebooks/Step%205%20-%20Generate%20GOPALS%20portfolio%20weights%20Strategy_2.3-MCSim-latest.ipynb)
- **Description:** Here we generate GOPALS based portfolio allocations and record the performance over various backtesting regimes.

### **Step 6: Generate Mean Variance Optimization Results:**
- **Notebook:** [Step 6 - Generate MVO portfolio weights.ipynb](https://github.com/JatinPatni/GOPALS/blob/master/Indian_Markets/Equity_Mutual_Funds_v1/notebooks/Step%206%20-%20Generate%20MVO%20portfolio%20weights.ipynb)
- **Description:** We use this code to generate MVO portfolios using the cvxpy library and coding the constraints to the objective function.

### **Step 7:  Generate PnL Time Series from Portfolio Weights:**
- **Notebook:** [Step 7 - Generate PnL time series from portfolio wts.ipynb](https://github.com/JatinPatni/GOPALS/blob/master/Indian_Markets/Equity_Mutual_Funds_v1/notebooks/Step%207%20-%20Generate%20PnL%20time%20series%20from%20portfolio%20wts.ipynb)
- **Description:** Utility functions to generate PnL from Portfolio Weights

### **Step 8: Generate Portfolio Performance Metrics:**
- **Notebook:** [Step 8 - Generate portfolio performance metrics given portfolio returns.ipynb](https://github.com/JatinPatni/GOPALS/blob/master/Indian_Markets/Equity_Mutual_Funds_v1/notebooks/Step%208%20-%20Generate%20strategy%20performance%20metrics%20given%20strategy%20returns%20timeseries.ipynb)
- **Description:** Utility functions to generate performance metrics.


## **Contact Me**

I’m open to collaborations, suggestions, and feedback related to this project or similar research initiatives. Feel free to reach out through any of the following channels:

- **GitHub Issues:** [Create a new issue here](https://github.com/JatinPatni/GOPALS/issues)
- **Email:** [jatinpatni@gmail.com](mailto:jatinpatni@gmail.com)
- **LinkedIn:** [Your LinkedIn Profile](https://www.linkedin.com/in/jatinpatni/)

---

