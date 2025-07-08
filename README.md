# Binary Classification on CIFAR-10 Using Transfer Learning and Custom CNNs

This project explores the performance of different convolutional neural network (CNN) architectures on a **binary classification task** derived from the CIFAR-10 dataset. The objective is to compare models trained from scratch with those leveraging **transfer learning**, specifically using a **pretrained ResNet18**.

---

## 📚 Overview

- **Task:** Binary image classification  
- **Dataset:** CIFAR-10  
- **Positive Class:** One selected CIFAR-10 class (e.g., airplane)  
- **Negative Class:** All other CIFAR-10 classes combined  
- **Image Size:** Resized from 32×32 to 224×224 to support ResNet18 input dimensions  
- **Training Strategy:** Early stopping based on validation performance

---

## 🧪 Models Compared

1. **Baseline CNN** – A simple custom convolutional architecture  
2. **Custom ResNet18** – ResNet18 architecture implemented and trained from scratch  
3. **Pretrained ResNet18** – PyTorch pretrained ResNet18 fine-tuned on the task

---

## 🔧 Experimental Setup

- Each model was trained on datasets of varying size:
  - 100, 1000, and 5000 samples per class (positive/negative)
- All models were trained using the same preprocessing, optimization settings, and early stopping

---

## 📊 Results (Best Test Accuracy)

| Samples per Class | Baseline CNN | Custom ResNet18 | Pretrained ResNet18 |
|-------------------|--------------|------------------|----------------------|
| 100               | 75.85%       | 77.15%           | **98.10%**           |
| 1000              | 82.70%       | 90.25%           | **97.20%**           |
| 5000              | 89.80%       | 94.85%           | **98.05%**           |

---

## ✅ Key Findings

- The **pretrained ResNet18** showed superior performance across all dataset sizes, especially in low-data regimes.
- The **custom ResNet18** demonstrated strong generalization with larger training sets.
- The **baseline CNN** was effective but limited in scalability and performance.
- Accuracy on 100 examples per class in training set.
  ![image](https://github.com/user-attachments/assets/1e55c602-22ba-4975-b7c6-229baf669940)
- Accuracy on 1000 examples per class in training set.
  ![image](https://github.com/user-attachments/assets/070dc347-bb3d-4c39-a08d-dcda23512ee1)
- Accuracy on 5000 examples per class in training set.
  ![image](https://github.com/user-attachments/assets/96ede89c-77a7-4cba-bc32-14dbdd8e456f)

- Top performing model analysis on the different datasets.
  ![image](https://github.com/user-attachments/assets/ea7d78e3-9140-42ae-a3b3-00fb49196c42)

## **The pretrained ResNet18 consistently outperforms the other models, especially when trained on fewer examples, highlighting the benefit of transfer learning in low-data regimes.**
---

## 🛠️ Tools & Frameworks

- [PyTorch](https://pytorch.org/)  
- [Torchvision](https://pytorch.org/vision/stable/index.html)  
- NumPy, Matplotlib (for analysis and visualization)  

---
