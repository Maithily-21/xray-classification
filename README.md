# 🩻 X-ray Image Classification (Pneumonia Detection)

This project uses **Transfer Learning (VGG16)** to classify **Chest X-rays** into **Normal** vs **Pneumonia**.  
The model was trained on the [Kaggle Chest X-ray Pneumonia Dataset](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia).  

---

## 📂 Repository Structure
xray-classification/
│── model/ # Folder containing trained model (.h5)
│ └── pre_trained_model_2.h5
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
