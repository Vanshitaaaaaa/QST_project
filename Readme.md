# Quantum State Tomography using Classical Shadows (Track 1)

This repository contains the implementation for **Assignment 2 – QCG × PaAC Open Project (Winter 2025–2026)**.  
The objective of this project is to **reconstruct a quantum density matrix from measurement data** using a machine learning model while strictly enforcing physical constraints.

The project follows **Track 1 (Classical Shadows)** and uses a **Transformer-based neural network** trained to output a physically valid density matrix via Cholesky decomposition.

---

## Project Objectives

- Reconstruct quantum density matrices from measurement data
- Enforce physical constraints:
  - Hermitian
  - Positive Semi-Definite (PSD)
  - Unit trace
- Evaluate reconstruction quality using:
  - Quantum Fidelity
  - Trace Distance
- Ensure full reproducibility and transparency

---

## Chosen Track

**Track 1 – Classical Shadows**

- Model: Transformer Encoder
- Output: Lower triangular matrix \( L \)
- Density matrix reconstruction:
  \[
  \rho = \frac{LL^\dagger}{\text{Tr}(LL^\dagger)}
  \]

This guarantees physical validity by construction.

---

## Repository Structure

---

##  Running the Project (Quick Start)

This project is designed to run entirely on **Google Colab**.

1. Open the provided Colab notebook
2. Install dependencies
3. Generate training and test data
4. Train the Transformer model
5. Evaluate reconstruction metrics

Detailed step-by-step instructions are provided in:

 `docs/REPLICATION_GUIDE.md`

---

##  Results and Required Metrics

###  Mean Fidelity and Trace Distance

The model was evaluated on a held-out test set.  
Each predicted density matrix was compared with the ground-truth state.

- **Mean Fidelity (Test Set):** `0.9175329337120056`
- **Mean Trace Distance (Test Set):** `0.21767027969658376`

> Higher fidelity and lower trace distance indicate better reconstruction quality.

---

### Inference Latency

Inference latency measures the time required to reconstruct **one density matrix**.

- Measured using Python timing utilities
- Includes forward pass and density matrix reconstruction
- Averaged across multiple samples

- **Average inference latency:** 0.0003309645652770996 seconds per sample`

---

###  Metrics Summary

| Metric | Value |
|------|------|
| Mean Fidelity | 0.9175329337120056 |
| Mean Trace Distance | `0.21767027969658376` |
| Inference Latency | `0.0005732245445251464` |

---

## Documentation

Detailed explanations are available in the `/docs` folder:

- **MODEL_WORKING.md**  
  Mathematical formulation, Transformer architecture, and constraint enforcement.

- **REPLICATION_GUIDE.md**  
  Step-by-step guide to reproduce all results on Google Colab.

---

## AI Usage Disclosure

AI tools were used responsibly during development.

Details including:
- Tools used
- Nature of assistance
- Verification steps

are documented in:

 `AI_USAGE.md`

---

##  Reproducibility & Verification

- All experiments can be reproduced using the provided code and instructions
- Random seeds are fixed where applicable
- Physical validity of outputs is guaranteed by model design

---

## License

This project is intended for **academic and educational purposes only** as part of the QCG × PaAC Open Project.


