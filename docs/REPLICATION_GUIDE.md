# Replication Guide
## 1. Requirements

- Google Colab
- Python 3.9+
- No external datasets required
## 2. Environment Setup

Open a new Google Colab notebook and install dependencies:

```bash
!pip install torch torchvision numpy matplotlib

---

### **3. Running the Code**

```markdown
## 3. Running the Code

1. Upload or clone the repository into Colab.
2. Run the notebook cells in order:
   - Data generation
   - Model definition
   - Training loop
   - Evaluation and visualization
3. Training typically completes within a few minutes on CPU.
## 4. Outputs

After execution, the following outputs are generated:

- Trained model weights:
  - `outputs/density_matrix_model.pt`
- Sample reconstructed density matrices:
  - `outputs/rho_pred_samples.npy`
- Printed metrics:
  - Mean Fidelity
  - Mean Trace Distance
  - Inference Latency
## 5. Reproducibility Notes

- Random seeds can be fixed for exact reproducibility.
- All data is synthetically generated.
- The same Colab notebook can be rerun to reproduce results.
