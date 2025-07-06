# Algorithmic-Trading-Assignment
Formulate and apply trading rules using one or more of the techniques: Genetic Algorithms, Genetic Programming, Neural Networks, Particle Swarm Optimisation, or Differential Evolution. 

# Overview
- Developed a trading algorithm to predict and execute trades on Google's (GOOG) stock.
- Used Recursive Feature Elimination (RFE), Neural Networks, and Genetic Algorithm (GA) to enhance stock price prediction and trading strategy optimisation.
# Trading strategy
- RFE used to select several technical indicators by removing less relevant ones.
- Trained a neural network trained to take the selected technical indicators over a lookback window of 10 days as input and predict the next-day stock price.
- Evolved a trading strategy using GA on the buy/sell/stop-loss thresholds 
# Performance on training data
- Used MAPE (relative error) and MDA (directional accuracy) to evaluate the price predictive accuracy of the neural network
- Achieved 0.78% MAPE error and 75.88% MDA on training data.
- Used annualised return and annualised Sharpe ratio (risk-adjusted return) to evaluate effectiveness of trading strategy.
- Achieved 48.10% annualised return and 1.58 annualised Sharpe ratio on training data.
# Performance on unseen data (backtesting)
- Backtesting results were successful.
- Achieved 3.50% MAPE error and 79.08% MDA on test data.
- Achieved 38.98% annualised return and 1.71 annualised Sharpe ratio on test data.
- Achieved better performance when compared against 4 other baseline approaches (random trading, buy-and-hold, suboptimal trading strategies, etc.)
# Other observations
- Observed unusually low stock trading activity at periods where the stock price exceeded $150. Traced this back to the neural network's drop in accuracy when predicting prices above $150.
- Concluded that this is due to unseen stock prices in the training data, as Google's highest stock price in the training data was $150.71 on 18 Nov 2021. However, Google's stock price rose above $150 a share in April 2024, the neural network was unable to predict the future stock prices as accurately.
- Noted that future improvement could use daily stock price change (%) as a percentage instead of stock price itself.
