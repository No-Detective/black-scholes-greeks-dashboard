# 📈 Black-Scholes Option Pricer & Greeks Dashboard

This project implements a **Black-Scholes option pricing engine** from scratch and provides an interactive dashboard to visualize the **Greeks** of an option using historical stock data.

---

## 🔧 Features

* 📊 Pulls historical stock price data using `yfinance`
* 🧮 Calculates 20-day rolling volatility as an input to the pricing model
* 💰 Implements the **Black-Scholes** formula for European call and put options
* ⚙️ Computes **option Greeks** using finite difference methods:

  * Delta
  * Gamma
  * Theta
  * Vega
* 🧠 Includes interactive dashboard widgets to adjust parameters in real time

---

## 📌 Technologies Used

* `Python`
* `Jupyter Notebook`
* `pandas`, `numpy`, `scipy`
* `yfinance`
* `ipywidgets` for dashboard interactivity
* `matplotlib` for visualization

---

## 📈 Methodology

1. **Download Historical Prices:**

   * Stock data fetched from Yahoo Finance
   * Only `Close` prices used to estimate volatility

2. **Estimate Volatility:**

   * 20-day log return rolling standard deviation
   * Annualized using √252

3. **Black-Scholes Pricer:**

   * Built from scratch (not using `scipy.stats` pricing shortcuts)
   * Handles both calls and puts

4. **Greeks Calculation:**

   * Approximated using **finite difference bumps** in inputs
   * Change each variable ±0.01 to compute sensitivities

5. **Interactive Dashboard:**

   * Dropdowns and sliders to simulate different market conditions
   * Live calculations shown for each Greek

---

## 🧠 Learning Goals

* Deep understanding of how Black-Scholes works
* Hands-on calculation of option prices and Greeks
* Practice with financial data pipelines and interactivity

---

## 🧮 Future Enhancements

* Real-time pricing with minute-level data
* Add implied volatility visualization
* Integrate American option logic (e.g., binomial tree)
* Portfolio-level dashboard with multiple strikes
