# 🩻 X-ray Image Classification (Pneumonia Detection)

This project uses **Transfer Learning (VGG16)** to classify **Chest X-rays** into **Normal** vs **Pneumonia**.  
The model was trained on the [Kaggle Chest X-ray Pneumonia Dataset](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia).  

---

## 📂 Repository Structure

xray-classification/

│── model/ # Folder containing trained model (.h5)

 └── pre_trained_model_2.h5
 
│── xray_model.ipynb # Notebook with training & evaluation

│── requirements.txt # Dependencies

│── README.md # Project documentation

---

## 📊 Dataset
- Source: [Chest X-ray Pneumonia Dataset on Kaggle](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)  
- Classes:  
  - **Normal** → Healthy lungs  
  - **Pneumonia** → Infected lungs  

---

## ⚙️ How to Run

### 1️⃣ Clone the repository
```bash
git clone https://github.com/Maithily-21/xray-classification.git
cd xray-classification

```
### 2️⃣ Install dependencies
```bash
pip install -r requirements.txt
```
### 3️⃣ Training
```bash
jupyter notebook xray_model.ipynb
```
### 4️⃣ Inference
```bash
from tensorflow.keras.models import load_model
import cv2, numpy as np

model = load_model("model/pre_trained_model_2.h5")

img = cv2.imread("sample_xray.jpg")
img = cv2.resize(img, (100, 100)) / 255.0
img = np.expand_dims(img, axis=0)

prediction = model.predict(img)
print("Pneumonia" if prediction[0][0] > 0.5 else "Normal")

```
### 📦 Model Weights

Trained model is stored in /model.

File size: ~70 MB (GitHub can’t preview, but it’s available in repo).

### 📈 Results

Base Model: VGG16 (pre-trained on ImageNet)

Accuracy: ~90% on validation set

