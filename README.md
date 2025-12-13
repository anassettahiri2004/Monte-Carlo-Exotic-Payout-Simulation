# Monte Carlo and Reinforcement Learning Methods for Exotic and American Option Pricing

This project explores **advanced numerical methods for option pricing**, combining **Monte Carlo simulation** and **Deep Reinforcement Learning** to price **path-dependent exotic options** and **American options with early exercise features** under the Black–Scholes framework.

The repository is structured in two complementary parts:
1. Monte Carlo pricing of exotic options  
2. Reinforcement Learning (Deep Q-Learning) for American option pricing  

Together, these components illustrate modern computational approaches used in quantitative finance when closed-form pricing formulas are unavailable.

---

## 📌 Part I — Monte Carlo Simulation for Exotic Option Pricing

### Overview
In the first part, we implement a Monte Carlo simulation engine to price options whose payoff depends on the **entire path** of the underlying asset. The asset price is modeled under the **risk-neutral measure** using a Geometric Brownian Motion (GBM).

### Implemented Option Types
- **European Call Option** (benchmark)
- **Asian Arithmetic-Average Call Option**
- **Barrier Knock-Out Call Option**

### Methodology
- Simulate stock price paths using discretized GBM
- Compute option payoffs path-wise
- Estimate prices as discounted expected payoffs
- Analyze the effect of strike, volatility, and maturity
- Compare payout structures across option types

### Key Concepts
- Risk-neutral pricing
- Path-dependence
- Monte Carlo convergence
- Discounted expectation
- Sensitivity to model parameters

---

## 📌 Part II — Reinforcement Learning for American Option Pricing

### Overview
The second part formulates the pricing of an **American put option** as an **optimal stopping problem** and solves it using **Deep Q-Learning (DQN)** implemented in PyTorch.

Instead of relying on regression-based continuation value approximations, the model learns the optimal early exercise policy directly from simulated price paths.

### Reinforcement Learning Formulation
- **State:** normalized stock price and time index  
- **Actions:** exercise or continue  
- **Reward:** option payoff upon exercise  
- **Dynamics:** risk-neutral GBM transitions  
- **Discount factor:** derived from the risk-free rate  

### Implementation Details
- Custom RL environment for American options
- Deep Q-Network with experience replay
- Target network for training stability
- ε-greedy exploration strategy
- Bellman optimality enforcement via bootstrapped targets

### Outputs
- Estimated American option price via Monte Carlo evaluation
- Visualization of the learned **optimal exercise boundary**
- Validation against European option benchmarks

---

## 🛠️ Technologies Used
- **Python**
- **NumPy**
- **PyTorch**
- **Monte Carlo Simulation**
- **Reinforcement Learning (DQN)**
- **Stochastic Processes**
- **Optimal Stopping Theory**

---

## 📊 Results & Insights
- Monte Carlo methods naturally handle complex path-dependent payoffs
- Asian and barrier options exhibit lower prices than European counterparts due to payoff constraints
- Deep Q-Learning successfully learns the optimal early exercise strategy for American options
- The learned exercise boundary behaves consistently with financial theory
- American option prices dominate European prices as expected

---




