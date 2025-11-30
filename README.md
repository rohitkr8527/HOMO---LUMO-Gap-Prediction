# HOMO–LUMO Gap Prediction Using Graph Neural Networks and Δ-Learning

This project implements a pipeline for predicting the HOMO–LUMO energy gap of molecules using Graph Neural Networks (GNNs) and Δ-learning. The workflow includes data preparation, graph construction, model training, and evaluation.

## Features

* Molecular structure processing using RDKit
* Graph representation for PyTorch Geometric
* Two modelling approaches: standard GNN and Δ-learning
* Configurable dataset size and property selection
* Evaluation using MAE and prediction plots

## Project Structure

```
Model.ipynb        # Main notebook containing full workflow
(Generated plots)  # Stored in the working directory
```

## Installation

Clone the repository:

```bash
git clone <repo_url>
cd <repo_name>
```

Install dependencies inside the notebook or locally:

```python
!pip install rdkit -q
!pip install torch_geometric -q
!pip install e3nn -q
```

Requirements:

* Python 3.8+
* PyTorch
* RDKit
* PyTorch Geometric
* e3nn

## Dataset Configuration

Modify dataset settings in the notebook:

```python
data_size = 10000      # Number of molecules
USE_QM = False         # Toggle quantum mechanical targets
```

You can replace the sample dataset with your own molecular data.

## Model Description

### Standard GNN

Uses graph message passing with atom and bond features constructed using RDKit and PyTorch Geometric.

### Δ-Learning Model

Learns a correction term over a baseline method (e.g., GFN2) to improve prediction accuracy.

## Evaluation

The notebook generates:

* Predictions vs. true values
* MAE metrics
* Learning curves

All plots are saved automatically.

## Running the Notebook

1. Open the notebook in Jupyter or Google Colab.
2. Run cells sequentially from installation to evaluation.
3. Review the generated plots and metrics.

## Future Improvements

* Hyperparameter tuning
* Support for additional molecular properties
* Larger datasets

## Contributing

Contributions are welcome. Fork the repository and open a pull request.
