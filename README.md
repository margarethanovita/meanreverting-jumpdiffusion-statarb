# Mean-reverting with Jump-diffusion Stocks Stat-Arb Strategy

This repository contains my experiment with a **market-neutral statistical arbitrage strategy** applied to selected stock pairs from the Indonesia Stock Exchange.

The strategy is inspired by and adapted from the framework proposed in:

> Endres, S., & Stübinger, J. (2017). *Optimal Trading Strategies for Lévy-driven Ornstein–Uhlenbeck Processes*. FAU Discussion Papers in Economics, No. 17/2017.  
> [Link to paper](https://hdl.handle.net/10419/169117)

---

## 🔍 Overview

This project implements a **pairs trading strategy** based on the **Lévy-driven Ornstein–Uhlenbeck (OU) process**, allowing the spread between two co-integrated stocks to exhibit **mean-reversion with jumps** and **fat-tailed behavior** — characteristics often found in financial time series.

### Main Objectives:
- Model the spread of each pair using a Lévy-driven OU process.
- Estimate parameters such as:
  - Mean-reversion speed (θ)
  - Volatility (σ)
  - Jump intensity (λ)
  - Exponential parameter (η)
- Optimize entry and exit thresholds by maximizing **expected return per unit time**.

---

## ⚙️ Model Features

- **Mean-Reverting Spread:**  
  Log-price spread is modeled as:  
  dXₜ = θ(μ - Xₜ)dt + dLₜ  
  where Lₜ is a Lévy process incorporating Brownian motion and Poisson process.

- **Jump Component:**  
  Jumps follow a **double exponential distribution**, capturing both large upward and downward movements in price spread.

- **Closed-Form Optimization:**  
  The expected first-passage time is derived in closed form, allowing **direct optimization** of trade thresholds.

- **Market Neutral:**  
  Strategy enters **long-short positions** simultaneously to minimize systematic market risk exposure.

---

## 📚 Reference

Endres, S., & Stübinger, J. (2017). *Optimal Trading Strategies for Lévy-driven Ornstein–Uhlenbeck Processes*. FAU Discussion Papers in Economics, No. 17/2017. Friedrich-Alexander-Universität Erlangen–Nürnberg.  
👉 [Available here](https://hdl.handle.net/10419/169117)

---

## 🛠️ Tools & Dependencies

- Python
- Optimization library
- Data source: Yahoo Finance

---

## 📝 Notes

This project is for academic and educational purposes only. Returns and performance measures are not financial advice.

