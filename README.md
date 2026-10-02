# Congrats Congrats Money Money

> An end-to-end quantitative trading research pipeline implementing market data processing, feature engineering, machine learning-based return prediction, portfolio construction, and modular backtesting on 10 years of historical market data.

---

## Overview

This project implements a complete quantitative trading workflow, starting from raw historical market data and ending with portfolio performance evaluation. The pipeline processes large-scale financial time-series data, engineers predictive features, trains multiple machine learning models, generates systematic trading signals, and evaluates investment strategies using a configurable backtesting framework.

The project was developed as part of a quantitative trading coursework assignment and focuses on building a realistic research pipeline rather than a single trading strategy.

---

## Features

- End-to-end market data preprocessing pipeline
- Large-scale financial time-series processing
- Feature engineering using technical indicators and rolling statistics
- Machine learning-based return prediction
- Ensemble learning using multiple regression models
- Portfolio construction and signal generation
- Modular backtesting engine
- Transaction cost modelling
- Performance benchmarking
- Statistical arbitrage analysis
- Performance visualization and analytics

---

## Dataset

| Metric | Value |
|--------|------:|
| Assets | 100 |
| Historical Period | Apr 2016 – Jan 2026 |
| Trading Days | 2,429 |
| Raw Market Records | 251,100 |
| Processed Records | 244,583 |

---

## Project Pipeline

```text
Raw Market Data
        │
        ▼
Data Cleaning & Preprocessing
        │
        ▼
Feature Engineering
        │
        ▼
Machine Learning Models
        │
        ▼
Ensemble Prediction
        │
        ▼
Signal Generation
        │
        ▼
Portfolio Construction
        │
        ▼
Backtesting Engine
        │
        ▼
Performance Evaluation
        │
        ▼
Visualization & Analysis
```

---

## Feature Engineering

The pipeline generates predictive features from historical OHLCV data, including:

- Momentum (5, 10, 20 and 60 day)
- Rolling volatility
- Relative volume
- RSI (Relative Strength Index)
- Bollinger Bands
- ATR (Average True Range)
- Moving Average Distance
- Overnight Returns
- Intraday Returns
- High-Low Range
- Cross-sectional normalized features
- Rolling statistical features

Overall, the pipeline engineers **22 predictive features** used for return forecasting.

---

## Machine Learning Models

Multiple supervised learning models were implemented and evaluated for next-day return prediction.

Models include:

- Ridge Regression
- LightGBM
- CatBoost

The final prediction pipeline combines these models using a weighted ensemble to improve robustness and reduce model-specific bias.

---

## Portfolio Construction

Predicted returns are used to rank all assets daily and generate systematic trading signals.

The framework supports:

- Daily asset ranking
- Long-only portfolio construction
- Dynamic portfolio rebalancing
- Transaction cost adjustment
- Benchmark comparison

---

## Backtesting Framework

A modular backtesting engine was developed to simulate realistic trading conditions.

### Supported Features

- Configurable transaction costs
- Portfolio simulation
- Daily valuation
- Portfolio rebalancing
- Performance benchmarking
- Strategy visualization

Transaction costs were evaluated across multiple scenarios ranging from **0 to 30 basis points**.

---

## Performance

The final strategy was evaluated on approximately **10 years** of historical market data.

### Highlights

| Metric | Value |
|--------|------:|
| Initial Capital | $1,000,000 |
| Prediction Coverage | 89.7% |
| Strategy Return | 410.3% |
| Benchmark Return | 319.9% |
| Annualized Return | 16.8% |
| Sharpe Ratio | 0.847 |

The developed strategy consistently outperformed the benchmark during the evaluation period while accounting for transaction costs.

---

## Statistical Arbitrage Analysis

The project also explores statistical arbitrage techniques including:

- Lead-lag analysis
- Cross-correlation analysis
- Significance testing
- Pairwise asset relationship analysis

These experiments were performed across all 100 assets over the complete historical dataset.

---

## Technologies Used

### Programming Language

- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- LightGBM
- CatBoost

---

## Repository Structure

```text
.
├── data/
│   ├── raw/
│   └── cleaned_panel_data.csv
│
├── notebooks/
│
├── benchmark.py
├── build_all_notebooks.py
├── README.md
└── ...
```

---

## Future Improvements

Potential future extensions include:

- Hyperparameter optimization
- Advanced ensemble learning
- Deep learning based forecasting models
- Reinforcement learning for portfolio allocation
- Risk-aware portfolio optimization
- Live market data integration
- Paper trading deployment

---

## License

This repository was developed as part of a quantitative trading coursework project and is intended for educational and research purposes.
