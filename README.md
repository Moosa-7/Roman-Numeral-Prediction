# Roman Numeral Prediction (Handwritten Recognition)

## 📌 Project Overview
This project develops a deep learning system to **predict handwritten Roman numerals (I, V, X)** from images.  
It uses a **Custom CNN architecture** with augmentation and transfer learning techniques to overcome **data scarcity** and **handwriting variability**.  

Achieved **~98.5% accuracy** on the test set.

---

## 👥 Contributors
- Muhammad Moosa (2023469)  
- Hamza Mukhtar (2023682)  
- Riyan Durrani (2023611)  
- Arsalan Khalil (2023130)  

---

## 🎯 Objectives
- Build an **image upload → prediction pipeline**.  
- Apply **CNN and transfer learning** approaches.  
- Document methodology, experiments, and results.  

---

## 📊 Dataset
- **3 classes**: I (1), V (5), X (10)  
- **Split**: Train (70%), Validation (15%), Test (15%)  
- **Challenge**: Small dataset + handwriting variability  
- **Solution**: Augmentation (rotation, shear, rescale), class balancing  

---

## 🛠 Methodology

### 🔹 Preprocessing
- Training data: Augmented using `ImageDataGenerator` (rotation, shear, rescaling).  
- Validation/Test: Rescaled only.  

### 🔹 Model Architecture
Custom CNN with:
- Conv2D → Batch Normalization → MaxPooling  
- Dropout (0.5) for regularization  
- Dense(3) output layer for classification  

### 🔹 Training Strategy
- Optimizer: **Adam (lr=1e-4)**  
- Loss: **Categorical Crossentropy with Label Smoothing**  
- Epochs: **20**  
- Class weights applied to address imbalance  

---

## 📈 Results
- **Test Accuracy**: ~98.5%  
- **Precision/Recall**: >0.95 for all classes  
- **Confusion Matrix**: Minor misclassifications between "I" and "X"  

---

## 🚀 Prediction Demo
Workflow:
1. Upload handwritten Roman numeral image  
2. Preprocess → Resize (224x224), Normalize  
3. Model predicts class (I, V, X)  

---

## ⚡ Challenges & Solutions
- **Data Scarcity** → Augmentation (↑ training diversity)  
- **Overfitting** → Dropout + BatchNorm  
- **Class Imbalance** → Weighted loss  

---

## 📂 Repository Structure
