# 🇮🇳 India Market Research - GOPALS Project

This folder contains market-specific research focused on **India's financial markets**, including large-cap stocks, equity mutual funds, and debt mutual funds. The research applies the **GOPALS: Geospatial Optimization and Portfolio Allocation using Landscape Segmentation** methodology, targeting robust portfolio construction through portfolio weight space segmentation and market simulations.

---

## **Table of Contents**
1. [Overview](#overview)
2. [Folder Structure](#folder-structure)
3. [Research Scope](#research-scope)
4. [How to Run](#how-to-run)
5. [Results](#results)
6. [Contributing](#contributing)
7. [License](#license)
8. [Contact](#contact)

---

## **Overview**
The **Indian Market Research** focuses on creating robust investment portfolios using historical simulations, Monte Carlo scenario generation, and portfolio optimization techniques. We apply the GOPALS framework to various Indian asset classes and compare portfolios against market indices such as **NIFTY 50** and **BSESN**.

---

## **Folder Structure**


---

## **Research Scope**
We conduct research in the following asset classes within the Indian financial market:

1. **Large Cap Stocks:**  
   - Focused on Indian blue-chip stocks like **NIFTY 50**, **BSESN**, and **top large-cap mutual funds**.  
   - **Goal:** Create optimized portfolios with minimal risk-return estimation error.

2. **Equity Mutual Funds:**  
   - Includes diversified equity mutual funds with historical **NAV** data.  
   - **Goal:** Backtest equity mutual funds using the GOPALS methodology.

3. **Debt Mutual Funds:**  
   - Focuses on Indian government and corporate debt mutual funds.  
   - **Goal:** Create stable, low-volatility portfolios under fixed-income constraints.

---

## **How to Run**
Follow these steps to execute the research process:

### **1. Clone the Repository**
```bash
git clone https://github.com/JatinPatni/GOPALS.git
cd GOPALS/india

jupyter notebook notebooks/01_data_preprocessing.ipynb

results/
├── portfolio_metrics.csv         # Portfolio performance metrics
├── sharpe_ratio_chart.png        # Sharpe ratio comparison
├── efficient_frontier.png        # Portfolio allocation visualization


Contact
Author: Jatin Patni
Email: jatinpatni@gmail.com
LinkedIn: [Your LinkedIn Profile](https://www.linkedin.com/in/jatinpatni/)
