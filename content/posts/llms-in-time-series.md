---
title: "Large Language Models as Zero-Shot Time Series Forecasters"
date: 2026-03-07
---

The convergence of Natural Language Processing (NLP) and Time Series Forecasting is accelerating. Unprecedented recent research indicates that Large Language Models (LLMs)—trained entirely on text and code—can process numerical sequences and output highly competitive time series forecasts, completely zero-shot.

## How Can Text Models Predict Numbers?

Traditionally, time series data is processed through purpose-built architectures (ARIMA, CNNs, Transformers patched for continuous variables). 

However, studies show that by tokenizing raw numerical time series data (e.g., converting the sequence `[104.2, 106.5, 102.1]` into textual string representations) and prompting a pre-trained LLM like GPT-4 or LLaMA with instructions like *"Predict the next 5 values in this sequence"*, the models perform remarkably well on standard forecasting benchmarks.

### The Underlying Mechanism

Why does this work? Language models learn complex, hierarchical pattern matching algorithms during pre-training. They internalize concepts of trend, seasonality, and cyclic behavior simply because mathematical and structural patterns are encoded syntactically throughout the internet's text. They have implicitly learned the "grammar" of sequences.

## Two Paradigms of Time Series LLMs

1. **LLM as a Tool (Prompting)**: Formatting numerical data as a prompt. While fascinating, it is highly unoptimized. Tokenizing numbers character-by-character scales poorly for high-frequency trading or massive supply chain datasets.
2. **Foundation Models for Time Series**: The more practical approach. Models like TimeGPT (Nixtla) or Chronos (Amazon) adopt the Transformer architecture of LLMs but are pre-trained on billions of actual time series observations across finance, weather, and retail.

### The True Value: Explainability

Where standard LLMs will truly shine in forecasting is not in raw predictive power (where specialized models still win on efficiency), but in **synthesis**. 

By feeding an LLM the numerical outputs of a rigorous state-space model alongside unstructured text data (earnings call transcripts, news headlines), the system can generate a dense narrative report explaining *why* the forecast shifted, bridging the gap between quantitative algorithms and human executives.

*At Predictive Systems Lab, we integrate multimodal LLM orchestration layers to explain and interpret complex algorithmic forecasting outputs.*
