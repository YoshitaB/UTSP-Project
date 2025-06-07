# UTSP-Project
This repository contains an implementation of the Unsupervised Travelling Salesman Problem (UTSP) framework, which solves the Travelling Salesman Problem (TSP) using unsupervised learning and Graph Neural Networks (GNNs). The project reimplements a baseline model using Graph Convolutional Networks (GCN) and introduces a modified model using Graph Attention Networks (GAT). It includes scripts for generating TSP instances, training models, evaluating performance, and visualizing results for TSP sizes n=20, 50, 100, 200, and 500. The codebase is designed to run in Google Colab with data and results stored in Google Drive.

Features
- Baseline Model: A GCN-based UTSP model using GCNConv layers to predict edge probabilities.
- Modified Model: A GAT-based model using GATConv layers with attention mechanisms for improved edge predictions.
- TSP Instance Generation: Generates random TSP instances for multiple sizes with coordinates and distance matrices.
- Training and Evaluation: Scripts to train models and evaluate tour lengths, with 2-opt local search optimisation.
- Visualisations: Tour plots, training loss curves, and a comparison chart of average tour lengths.
- Report: A LaTeX report template summarising implementation, experiments, and results.

  UTSP-Assignment/
├── models/
│   ├── baseline_utsp.py      # Baseline GCN-based UTSP model
│   ├── modified_utsp.py      # Modified GAT-based UTSP model
├── scripts/
│   ├── generate_tsp.py       # Generates TSP instances
│   ├── train_baseline.py     # Trains baseline or modified model
│   ├── evaluate.py           # Evaluates models and generates visuals
│   ├── local_search.py       # Implements 2-opt and tour construction
├── data/
│   ├── tsp_{size}_coords_{i}.npy  # TSP coordinates (n=20, 50, 100, 200, 500; i=0..9)
│   ├── tsp_{size}_dist_{i}.npy    # Distance matrices
├── results/
│   ├── baseline_tour_{size}.png   # Tour visualizations for baseline model
│   ├── modified_tour_{size}.png   # Tour visualizations for modified model
│   ├── training_loss_{model}_{size}.png  # Training loss plots
│   ├── length_comparison.png      # Bar chart comparing tour lengths
│   ├── {model}_utsp_{size}.pth    # Trained model weights
├── report/
│   ├── experimental_report.tex    # LaTeX report template
│   ├── experimental_report.pdf    # Compiled report (if generated)
├── README.md
