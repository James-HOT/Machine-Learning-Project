# Shoe Brand Classification Project

English | 繁體中文

---

## English

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

---

## 繁體中文

### 專案簡介

此 repository 是一個鞋子品牌分類（Shoe Brand Classification）的機器學習專案。
主要流程寫在 Jupyter Notebook，訓練完成的模型以 H5 檔案提供。

- Notebook：`Shoe_brand_Classification_Project.ipynb`
- 訓練模型：`best_model.h5`

### Git LFS 重要說明

此專案的主要檔案使用 Git LFS 儲存。
如果你剛 clone 後看到檔案非常小，代表你拿到的是 LFS pointer，而不是實際內容。

請執行以下指令下載實際檔案：

```bash
git lfs install
git lfs pull
```

### 專案結構

```text
Machine-Learning-Project/
├── Shoe_brand_Classification_Project.ipynb   # 訓練與實驗 notebook
├── best_model.h5                             # 已訓練模型
└── README.md                                 # 專案說明文件
```

### 環境需求

目前 repo 內尚未提供 `requirements.txt` 或 `environment.yml`。
依照一般 `.ipynb` + `.h5` 的影像分類流程，建議準備以下環境：

- Python 3.9+（建議）
- Jupyter Notebook 或 JupyterLab
- TensorFlow / Keras
- NumPy
- Matplotlib
- scikit-learn
- Pillow

若執行 notebook 時出現 import 錯誤，再補裝缺少套件即可。

### 安裝與設定

1. 下載專案：

   ```bash
   git clone <your-repo-url>
   cd Machine-Learning-Project
   ```

2. 透過 Git LFS 拉取大型檔案：

   ```bash
   git lfs install
   git lfs pull
   ```

3. 建立並啟用虛擬環境（建議）：

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

4. 安裝套件（範例）：

   ```bash
   pip install jupyter tensorflow numpy matplotlib scikit-learn pillow
   ```

### 執行方式

1. 啟動 Jupyter：

   ```bash
   jupyter notebook
   ```

2. 開啟 `Shoe_brand_Classification_Project.ipynb`。
3. 由上到下依序執行 cell。
4. 若 notebook 含訓練流程，請先確認資料集路徑在你的環境中正確。
5. 若 notebook 需載入 `best_model.h5`，請確認檔案已成功透過 Git LFS 拉下來。

### 模型載入範例

```python
from tensorflow.keras.models import load_model

model = load_model("best_model.h5")
print("Model loaded successfully.")
```

### 常見問題

- **載入 `best_model.h5` 時出現 `OSError`**
  - 多半是尚未拉到實體檔案，請執行 `git lfs pull`。
- **Notebook 看起來很小、內容不完整**
  - 很可能仍是 LFS pointer，請執行 `git lfs pull`。
- **出現 `ModuleNotFoundError`**
  - 代表缺少套件，請在目前啟用的 Python 環境安裝對應套件。
- **訓練時 kernel 當掉**
  - 可先降低 batch size、影像尺寸，或改用更高記憶體/GPU 的環境。

### 後續可強化方向

- 新增 `requirements.txt` 或 `environment.yml`，提升可重現性。
- 新增獨立推論腳本（例如 `predict.py`）。
- 補上資料集目錄規範（train/validation/test 結構）。
- 在文件中補充模型評估指標與混淆矩陣。
