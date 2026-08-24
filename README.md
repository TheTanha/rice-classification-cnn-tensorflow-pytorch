# 🍚 Rice Variety Classification – TensorFlow vs PyTorch

A comprehensive deep learning project to classify **5 varieties of rice** using custom CNN models built with both **TensorFlow/Keras** and **PyTorch**.  
This notebook compares performance, training speed, and accuracy of the two frameworks side‑by‑side on a dataset of 75,000 rice grain images.

---

## 📊 Dataset

- **Source**: [Rice Image Dataset](https://www.kaggle.com/datasets/muratkokludataset/rice-image-dataset) on Kaggle  
- **Classes**: Arborio, Basmati, Ipsala, Jasmine, Karacadag  
- **Total Images**: 75,000 (15,000 per class)  
- **Split**: 60% Train / 20% Validation / 20% Test  
- **Image Size**: 250×250 pixels (RGB)

> The dataset is automatically downloaded via `kagglehub` when the notebook runs.

---

## 🧠 Model Architecture

A lightweight CNN with **3 convolutional blocks**:

- Conv2D + BatchNorm + ReLU + MaxPooling (×3)  
- Global Average Pooling  
- Dense (128) + Dropout (0.4)  
- Output Dense (5) with Softmax  

Both TensorFlow and PyTorch implementations share **identical architecture** to ensure a fair comparison.

| Framework | Trainable Params |
|-----------|------------------|
| TensorFlow| 111,301          |
| PyTorch   | 110,853          |

---

## 🚀 How to Run

1. Open the notebook in **Google Colab** (GPU recommended).  
2. Execute cells sequentially – the dataset is downloaded automatically.  
3. Training takes ~2 hours (PyTorch) to ~7 hours (TensorFlow) on a T4 GPU.  
4. All outputs (models, plots, metrics) are saved to `/content/rice_classification/`.

---

## 📈 Results

| Metric                   | TensorFlow | PyTorch |
|--------------------------|------------|---------|
| **Test Accuracy**        | 97.21%     | **99.39%** |
| Precision (weighted)     | 97.48%     | 99.39%   |
| Recall (weighted)        | 97.21%     | 99.39%   |
| F1 Score (weighted)      | 97.25%     | 99.39%   |
| Training Time (seconds)  | 6977.5     | **1546.7** |
| Best Val Accuracy        | 97.09%     | **99.45%** |

> PyTorch achieves higher accuracy in **~4.5× less time** on the same hardware.

---

## 📁 Project Structure

After running the notebook, the following artifacts are saved:
