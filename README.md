# crypto-pridction
📊 Attention-LSTM Multivariate Time Series Forecasting

This project implements a complete deep learning forecasting pipeline using a custom Attention-enhanced LSTM model for multivariate time series prediction. The goal is to demonstrate how attention mechanisms can improve forecasting performance by highlighting the most influential time steps in the input sequence.

✅ Project Overview

This project builds and evaluates a forecasting system that:

1. Generates a Multivariate Time Series Dataset

5 features

2200+ daily observations

Includes trend, seasonality, noise, and cross-feature dependencies

Target variable is a weighted composite of all features

Dataset is standardized and validated with ADF stationarity tests

2. Implements a Custom Attention Layer (TensorFlow/Keras)

A fully custom Keras Attention Layer is built from scratch:

Learns attention weights over LSTM hidden states

Outputs both:
✓ Context vector
✓ Attention scores

Easily integrates into LSTM architecture

3. Builds Two Forecasting Models

Attention-LSTM Model (LSTM → Attention → Dense layers → Multi-step output)

Baseline LSTM Model (standard stacked LSTM + Dense output)

Both models predict the next 24 time steps (multi-step forecasting).

4. Rolling Window Cross-Validation

The project applies time-series aware CV:

Expanding/rolling windows

Multiple folds

RMSE tracked for each fold

5. Backtesting & Metrics

Models are evaluated on a held-out test set using:

RMSE

MAE

MAPE
Results are compared between:

Attention-LSTM

Baseline LSTM

6. Attention Weight Visualization

The project extracts and visualizes:

Attention scores for example test inputs

Average attention distribution

Insight into which time steps influence predictions most

7. Automatic Report Generation

A final Markdown report (report.md) is generated containing:

Dataset description

Preprocessing summary

Model architectures

CV results

Test performance

Attention interpretations

File list with outputs

📁 Project Output Includes

dataset.csv – synthetic multivariate dataset

metrics_test.csv – RMSE/MAE/MAPE comparison

cv_metrics.csv – cross-validation RMSE

example_attention_scores.csv

forecast_example_*.png

attention_example_*.png

avg_attention.png

report.md – consolidated project report

🧠 Key Learnings

How to build a complete forecasting pipeline

How to engineer a multivariate synthetic dataset with realistic temporal patterns

How to implement a fully custom Attention Layer in Keras

How attention improves interpretability in deep learning models

How to evaluate multi-step forecasting models with proper metrics

How to perform rolling-window cross-validation for time series

🚀 Technologies Used

Python

TensorFlow / Keras

Pandas & NumPy

Scikit-Learn

Statsmodels

Matplotlib

Google Colab

📝 Ideal Use Cases

Time series forecasting research

Model interpretability using attention

Educational deep learning projects

Comparing LSTM vs Attention-LSTM architectures

Multi-step prediction tasks

If you want, I can also generate:

➤ Full README.md (with badges, installation guide, usage examples)
➤ A project banner image
➤ A diagram of your Attention-LSTM architecture

Just ask: “Generate full README.md” or “Create repo banner”.
