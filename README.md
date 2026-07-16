# Multi-Domain Nuclear Digital Twin Security

[![PyTorch](https://img.shields.io/badge/PyTorch-2.12.0%2Bcpu-EE4C2C.svg)](https://pytorch.org/) 
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Author:** Dr. Mehtab Alam, Akshya Chamoli, Ashraf Ali, Abdullah Alourani

## Abstract
The increasing adoption of Digital Twin (DT) architectures in nuclear power systems has accelerated the convergence of Operational Technology (OT) and Information Technology (IT), exposing critical cyber-physical infrastructure to sophisticated zero-day attacks that cannot be reliably detected using conventional signature-based Intrusion Detection Systems. Addressing the heterogeneous characteristics of physical process telemetry and industrial network traffic remains a major challenge for developing practical anomaly detection frameworks. This research proposes a unified unsupervised deep learning and threat modeling framework that integrates domain-aware preprocessing, temporal anomaly detection, adaptive thresholding, and STRIDE-based threat attribution into a single cyber-physical security architecture for nuclear DT. The framework combines a Long Short-Term Memory Autoencoder (LSTM-AE) with domain-specific normalization strategies, applying Min-Max scaling to bounded physical telemetry and Robust scaling to highly variable network traffic while preserving the statistical characteristics of each operational domain. A dynamic 99.5th-percentile anomaly threshold is employed to reduce false-positive alarms that could lead to unnecessary operational interventions in safety-critical environments. To improve the interpretability of unsupervised anomaly detection, the framework incorporates a deterministic feature-level attribution mechanism that maps localized reconstruction errors to the STRIDE threat taxonomy, providing human-readable cyber-physical threat intelligence for system operators. The proposed framework is validated across three publicly available industrial control system datasets acting as nuclear-relevant industrial proxies for complementary operational domains: HAI (primary power generation), SWaT (secondary cooling processes), and WUSTL-IIoT (edge network monitoring). Experimental evaluation demonstrates robust anomaly detection performance, achieving ROC-AUC scores of 0.944, 0.948, and 0.985, respectively. The results demonstrate that integrating domain-aware preprocessing, unsupervised anomaly detection, adaptive thresholding, and STRIDE-based threat attribution provides an effective and interpretable framework for enhancing cyber-physical security in DT -enabled nuclear environments.

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
   `git clone https://github.com/mahiealam/Multi-Domain-Nuclear-DT-Security.git`
2. Install dependencies: Python 3.10+ and PyTorch 2.12.0.
3. Run `Pipeline.ipynb` via Jupyter to execute the dual-scaler preprocessing and train the LSTM-Autoencoder.
