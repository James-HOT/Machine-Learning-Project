# Shoe Brand Classification Project

### Overview

This repository contains a machine learning project for shoe brand classification.
The main workflow is implemented in a Jupyter Notebook, and the trained model is provided as an H5 file.

- Notebook: `Shoe_brand_Classification_Project.ipynb`
- Trained model: `best_model.h5`

### Important Note About Git LFS

Both major files in this repository are stored using Git LFS.
If you just cloned this repository and see very small file sizes, you are likely seeing LFS pointer files instead of real content.

Run the following commands to download actual files:

```bash
git lfs install
git lfs pull
```

### Project Structure

```text
Machine-Learning-Project/
├── Shoe_brand_Classification_Project.ipynb   # Training / experimentation notebook
├── best_model.h5                             # Saved trained model
└── README.md                                 # Project documentation
```

### Requirements

There is currently no dedicated dependency file (`requirements.txt` or `environment.yml`) in this repository.
Based on common workflows for `.ipynb` + `.h5` classification projects, use a Python environment that includes:

- Python 3.9+ (recommended)
- Jupyter Notebook or JupyterLab
- TensorFlow / Keras
- NumPy
- Matplotlib
- scikit-learn
- Pillow

If imports fail when running the notebook, install missing packages as needed.

### Setup

1. Clone the repository:

   ```bash
   git clone <your-repo-url>
   cd Machine-Learning-Project
   ```

2. Download large files via Git LFS:

   ```bash
   git lfs install
   git lfs pull
   ```

3. Create and activate a virtual environment (recommended):

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

4. Install dependencies (example):

   ```bash
   pip install jupyter tensorflow numpy matplotlib scikit-learn pillow
   ```

### How To Run

1. Start Jupyter:

   ```bash
   jupyter notebook
   ```

2. Open `Shoe_brand_Classification_Project.ipynb`.
3. Run notebook cells from top to bottom.
4. If the notebook includes training steps, ensure dataset paths are valid on your machine.
5. If the notebook loads `best_model.h5`, confirm the file exists and is fully pulled by Git LFS.

### Using the Trained Model (Example)

```python
from tensorflow.keras.models import load_model

model = load_model("best_model.h5")
print("Model loaded successfully.")
```

### Troubleshooting

- **`OSError` when loading `best_model.h5`**
  - The file may still be an LFS pointer. Run `git lfs pull`.
- **Notebook appears tiny / unreadable JSON missing**
  - The notebook may still be an LFS pointer. Run `git lfs pull`.
- **`ModuleNotFoundError`**
  - Install missing packages in your active Python environment.
- **Kernel crashes during training**
  - Reduce batch size, reduce image size, or run on a machine with more memory/GPU.

### Future Improvements

- Add `requirements.txt` (or `environment.yml`) for reproducible setup.
- Add a dedicated inference script (for example, `predict.py`).
- Add dataset organization notes (train/validation/test folder format).
- Add model evaluation metrics and confusion matrix in documentation.

