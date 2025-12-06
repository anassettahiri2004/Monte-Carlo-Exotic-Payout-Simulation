# Monte-Carlo-Exotic-Payout-Simulation
This project explores the simulation of stock price dynamics using Geometric Brownian Motion, the core stochastic model in the Black–Scholes framework. By leveraging Gaussian random vectors and Monte-Carlo techniques, it provides an intuitive way to study uncertainty in financial markets and visualize how asset prices evolve over time.
# 📈 Geometric Brownian Motion — Stock Price Simulation

This project explores the simulation of stock price dynamics using Geometric Brownian Motion (GBM), the core stochastic model in the Black–Scholes framework. By leveraging Gaussian random vectors and Monte-Carlo techniques, it provides a reproducible and intuitive way to study uncertainty in financial markets and visualize how asset prices evolve over time.

---

## 🔍 Model

The stock price \( S_t \) follows the stochastic differential equation:

$$
dS_t = r S_t\, dt + \sigma S_t\, dW_t
$$

where:  
- $S_t$: stock price at time $t$  
- $r$: risk-free interest rate  
- $\sigma$: asset volatility  
- $W_t$: standard Brownian motion  

The closed-form solution used for simulation is:

$$
S_t = S_0 \exp\\left( \left( r - \frac{1}{2}\sigma^2 \right)t + \sigma \sqrt{t}\, Z \right)
$$

with $Z \sim \mathcal{N}(0,1)$.

---

## ✨ Project Features

- Generates Gaussian random vectors with reproducible seeds  
- Simulates multiple GBM asset price paths  
- Visualizes the evolution of stock prices over time  
- Clean and extensible Python code structure  

---

## 🛠 Tech Stack

| Component | Description |
|----------|-------------|
| Python | Core language |
| NumPy | Numerical computations |
| Matplotlib | Visualization of price paths |

---

## 🚀 Future Improvements

- Monte-Carlo pricing of European/Asian options  
- Calibration to historical market data  
- Multi-asset GBM and correlation structure  

---

## 📂 Usage

Example simulation command:

```bash
python main.py
