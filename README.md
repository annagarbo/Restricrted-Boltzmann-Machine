# Restricted Boltzmann Machine

This repository contains a group project developed during the course  
**Laboratory of Computational Physics** at the **University of Padova (UNIPD)**  
in the academic year **2022–2023**.

The project focuses on the implementation, training, and performance analysis of a **Restricted Boltzmann Machine (RBM)**, with particular attention to how different modeling and optimization choices affect learning dynamics and convergence.

---

## Project overview

The main goal of this work is to study the learning behavior of a Restricted Boltzmann Machine trained on **structured synthetic data**, specifically **one-hot encoded patterns** representing simplified protein polarity states.

The RBM is trained to reproduce the underlying structure of the data distribution, and its performance is evaluated under different conditions, including:

- **Binary [0,1] vs bipolar [-1,1] data representations**
- **Different optimization strategies**, including:
  - Vanilla gradient descent
  - RMSProp optimizer
- **Contrastive Divergence (CD)** with varying number of steps
- **Backward Contrastive Divergence (BCD)** to preserve one-hot encoding constraints
- **Different numbers of hidden units** to analyze model capacity and overfitting

The project combines theoretical understanding, numerical implementation, and statistical analysis to assess convergence, stability, and interpretability of the learned model.

---

## Methods and analysis

The RBM learning process is analyzed using two main performance indicators:

- **Log-Likelihood**, used to monitor how well the model fits the training data
- **Energy gradient**, measuring the difference between the energy of the data distribution and the model distribution

A well-trained RBM is expected to show:
- Saturation of the log-likelihood
- Energy gradient converging toward zero

The study compares learning behavior across different configurations and highlights how **binary representations** generally lead to **faster and more stable convergence** compared to bipolar ones, in agreement with the theoretical design of RBMs.

A detailed description of the methodology, results, and discussion can be found in the accompanying report.

---

## Repository structure

The repository is organized as follows:
```
Restricted-Boltzmann-Machine/
│
├── DATA/ # Training datasets (binary / bipolar representations)
├── DATA_b/ # Alternative or processed datasets
├── E2/ # Additional experiments and analysis
│
├── gen_23_RBM-input.ipynb # Data generation and preprocessing
├── RBM_23_FINAL_BN3.ipynb # Final RBM implementation (binary representation)
├── RBM_23_FINAL_BP2.ipynb # Final RBM implementation (bipolar, 2 hidden units)
├── RBM_23_FINAL_BP6.ipynb # Final RBM implementation (bipolar, 6 hidden units)
│
├── group2306_assignment.pdf # Project report with full theoretical and numerical analysis
├── group2306_excercise2.ipynb
├── PESI CASUALI.png # Visualization of randomly initialized weights
│
└── README.md
```

---

## Report

The file  
**`group2306_assignment.pdf`**  
contains the full project report, including:

- Theoretical background on RBMs
- Description of the learning algorithms
- Performance comparison between different configurations
- Weight matrix visualizations
- Discussion of convergence, noise, and overfitting effects

---

## Notes

This project was developed in an academic context and is intended as an exploratory and educational study of unsupervised learning using energy-based models.  
The emphasis is on **physical intuition**, **statistical analysis**, and **model behavior**, rather than production-level optimization.

---

## Authors

Group project developed by:

- Edoardo Renato Bucalo  
- Camilla Forza  
- Anna Garbo  
- Federico Ruffini
