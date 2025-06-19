# bayesian-cancer-predictor-demo
Bayesian logistic regression for cancer prediction using spatial transcriptomics (Visium, Pyro)


# Bayesian Cancer Prediction with Spatial Transcriptomics

This project builds a Bayesian logistic regression model using [Pyro](https://pyro.ai/) to classify cancerous regions in a human breast tissue sample based on spatial transcriptomics data. The model leverages MCMC inference to provide both predictions and uncertainty estimates, and it maps results spatially using Scanpy.

---

## What This Does

- Loads real spatial gene expression data (10x Genomics Visium breast cancer slice)
- Simulates cancer labels for tissue regions
- Selects top 1000 highly variable genes
- Trains a Bayesian logistic regression model using Pyro + NUTS sampling
- Extracts posterior distributions over weights (gene importance)
- Computes predictive probabilities and confidence for each spatial spot
- Visualizes cancer predictions and uncertainty across the tissue map

---

## Why It Matters

This is a prototype of a probabilistic diagnostic tool that could guide cancer classification from gene expression patterns. By using Bayesian modeling, it not only predicts cancer probability but also quantifies how confident it is — offering interpretable and clinically relevant insights.

---

## Outputs

- Posterior distributions over gene weights
- Top cancer-associated genes with uncertainty
- Spatial heatmaps of predicted cancer probability
- Spatial maps of model uncertainty

---

## Tech Stack

- Python
- PyTorch + Pyro
- Scanpy + AnnData
- Matplotlib
