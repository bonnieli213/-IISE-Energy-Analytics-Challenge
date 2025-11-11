# ⚡ IISE Data Analytics Competition — Energy Load Forecasting

### 🏫 Team: CMUGridElfs | Carnegie Mellon University
Our team participated in the **2025 IISE–PG&E Data Analytics Challenge**, forecasting **hourly electricity demand** for a California region using **two years of historical data** on load, temperature, and solar irradiance (GHI).  
Accurate long-term load forecasting supports **grid reliability**, **renewable energy integration**, and **strategic infrastructure planning**.


## 🔍 Approach
We developed a **bi-level ensemble model** that combines the strengths of statistical and machine-learning techniques:

1. **Level 1 – Temporal Modeling:**  
   Fit a general **time-series model** (e.g., ARIMA or Prophet) to capture long-term trends and seasonal patterns in electricity demand.  

2. **Level 2 – Residual Modeling:**  
   Train an **XGBoost model** on the **residuals** from the first model to capture nonlinear effects from external factors like **temperature** and **GHI**.  

Building on this concept, we created a **Tri-Resolution Boosting Framework**, which decomposes the forecasting task into **monthly**, **weekly**, and **hourly** components.  
Each level specializes in patterns at its respective time scale, and the results are combined for a final, highly accurate prediction.


## 🚀 Results
- The **Tri-Resolution Boosting Model** achieved the **lowest validation MSE (43.04)** among all tested methods.  
- It **outperformed Prophet, RNN, and standalone XGBoost**, demonstrating both **high accuracy** and **computational efficiency**.  
- The results highlight how integrating **statistical models** with **machine-learning approaches** can significantly improve long-term, high-resolution load forecasting.


## 🧰 Tech Stack

**Python**, **XGBoost**, **Prophet**, **ARIMA**, **RNN**, **Google Colab**, **pandas**, **NumPy**, **scikit-learn**


