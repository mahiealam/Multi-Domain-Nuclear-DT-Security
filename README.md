# Multi-Domain Nuclear Digital Twin Security

[![PyTorch](https://img.shields.io/badge/PyTorch-2.12.0%2Bcpu-EE4C2C.svg)](https://pytorch.org/) 
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Author:** Dr. Mehtab Alam

## Abstract
[Insert your abstract here. Discuss the dual-scaler preprocessing, PyTorch LSTM-Autoencoder pipeline, and automated STRIDE threat mapping.]

## Repository Structure
* **`notebooks/Pipeline.ipynb`**: Contains the core logic, preprocessing, sequence windowing, and model training.
* **`Results/figures/`**: High-resolution performance plots and mapped threat visuals.
* **`Results/reports/research_summary_20260625_201722.md`**: Final evaluation metrics and research summary.
* **`Results/logs/full_pipeline_log_20260625_201722_reduced.txt`**: Reduced execution log demonstrating hardware metrics and pipeline flow.

## Datasets
This research evaluates the threat mapping pipeline across three multi-domain ICS datasets. Raw data is not tracked in this repository due to file size constraints. Please download the datasets from their original sources and place them in the `Datasets/` directory:
1. **[HAI (HIL-based Augmented ICS)](#)**: Evaluates baseline physical tampering and spoofing.
2. **[SWaT (Secure Water Treatment)](#)**: Merged normal/attack topologies.
3. **[WUSTL-IIoT](#)**: Targeted for network-layer threat simulations.

## Quick Start
1. Clone the repository:
   `git clone https://github.com/USERNAME/Multi-Domain-Nuclear-DT-Security.git`
2. Install dependencies: Python 3.10+ and PyTorch 2.12.0.
3. Run `Pipeline.ipynb` via Jupyter to execute the dual-scaler preprocessing and train the LSTM-Autoencoder.
