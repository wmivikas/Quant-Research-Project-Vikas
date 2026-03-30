# 📈 True Beacon Quant Research Project

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-black?logo=pandas)
![NumPy](https://img.shields.io/badge/Numpy-Scientific%20Computing-blue?logo=numpy)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Finance](https://img.shields.io/badge/Domain-Quant%20Finance-green)

---

## 🧠 Overview

This project implements a **pairs trading strategy** based on the **volatility spread** between:

* Nifty Index
* Bank Nifty Index

Built as part of the **True Beacon Quant Research Assignment**, the goal is to identify statistical arbitrage opportunities using **mean-reversion techniques**.

---

## 📊 Strategy Logic

### 🔹 Base Model — Z-Score

* Compute spread between Nifty IV & Bank Nifty IV
* Normalize using z-score
* Trade on deviation from mean

👉 Core idea: **Mean Reversion**

---

### 🔹 Improved Model — Moving Average (MA)

* Smooth spread using moving average
* Generate signals from trend + deviation

👉 Core idea: **Noise reduction + trend capture**

---

## 📁 Project Structure

```bash
├── data.parquet              # IV dataset (Nifty & BankNifty)
├── trading_strategy.ipynb    # Core implementation
├── trading_strategy.xlsx    # Output results
├── requirements.txt         # Dependencies
├── Full_Data.png            # Full strategy visualization
├── One_day_data.png         # Single day strategy (2021-10-11)
```

---

## 📉 Results

### ⚠️ Base Model Performance

* P/L: **-26.78**
* Sharpe Ratio: **-0.06**
* Drawdown: **-26.78**

### ⚠️ MA Model Performance

* P/L: **-26.78**
* Sharpe Ratio: **-0.06**
* Drawdown: **-26.78**

📌 Insight: Strategy needs **better signal filtering / risk management**

---

## 📊 Visualizations

### 📅 One Day Strategy

![One Day Strategy](One_day_data.png)

### 📈 Full Data Strategy

![Full Data Strategy](Full_Data.png)

---

## ⚙️ Assumptions

* Missing values handled using Pandas
* Trading horizon: **30 minutes → 5 days**
* Mean-reversion holds in IV spread

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Matplotlib
* Jupyter Notebook

---

## 📌 Key Learnings

* Z-score alone is **not sufficient** for stable trading
* IV spreads are **noisy and regime-dependent**
* Strategy needs:

  * Better entry filters
  * Stop-loss logic
  * Volatility regime detection



---

## ⭐ If you found this useful

Give it a star ⭐ and feel free to fork!
