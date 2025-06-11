# 🧠 Brain Tumor Detection Using MRI Scans

This project uses deep learning to classify brain MRI scans into four categories — **glioma**, **meningioma**, **pituitary tumor**, and **no tumor**. We compare a baseline neural network, a custom CNN, and a ResNet18-based transfer learning model. The custom CNN achieved the highest accuracy of **97.3%**.

---

## 📂 Dataset

- Combined dataset of **7,023 MRI images** from:
  - Nanfang and Tianjin Medical University Hospitals (2005–2010)
  - Kaggle repository:  
    [Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)

---

## 🧹 Data Preprocessing

- Resized to **224×224×3**
- Normalized pixel values
- Applied data augmentation:
  - Random rotations (±15°)
  - Horizontal flips
  - Width/height shifts
  - Random zoom

- Dataset Split:
  - 70% Training
  - 15% Validation
  - 15% Testing

---

## 🧠 Models

### 🔹 Baseline Neural Network (NN)
- Fully connected layers
- Accuracy: ~77%

### 🔹 Custom Convolutional Neural Network (CNN)
- 2 convolutional blocks → flatten → dense layers
- Batch normalization and dropout included
- Accuracy: **97.3%**

### 🔹 ResNet18 (Transfer Learning)
- Pretrained on ImageNet
- Final layers fine-tuned
- Accuracy: ~89%

---

## 📊 Performance Comparison

| Model       | Accuracy | Precision | Recall | F1 Score |
|-------------|----------|-----------|--------|----------|
| CNN         | 97.3%    | High      | High   | High     |
| ResNet18    | ~89%     | Moderate  | High   | Strong   |
| Baseline NN | ~77%     | Lower     | Lower  | Lower    |

---

## 📸 Visualization

- Prediction outputs are visualized alongside MRI images
- Each image displays predicted label and confidence score
- CNN showed highest confidence in glioma classification

---

## 🧠 Insights

- Custom CNN outperforms both the baseline and pretrained model  
- Augmentation and dropout layers significantly improve generalization  
- Glioma classification showed the highest model confidence  

---

## 👨‍💻 Contributors

- Rohith Adhitya Chinnannan Rajkumar  
- Rutvik Shah  
- Uma Maheshwari Deivasigamani  

---

## 📜 License

This work is for academic use only. MRI data is publicly available for research purposes.
