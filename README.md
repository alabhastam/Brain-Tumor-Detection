# 🧠 Brain MRI Images for Brain Tumor Detection

This project trains and evaluates deep learning models to detect the presence of brain tumors from MRI scans.  
We implemented both a **custom CNN model** and a **transfer learning approach** (EfficientNetB0), compared their performance, and explored strategies for improving generalization.

---

## 📂 Project Workflow
1. **Data Loading & Exploration**  
   - Load MRI images dataset.
   - Visualize sample images, check class distribution.

2. **Preprocessing & Augmentation**  
   - Resize and rescale images to `(224, 224)`.  
   - Data augmentation using `ImageDataGenerator`.  
   - Split into training, validation, and test sets.

3. **Modeling**  
   - **Model 1:** Custom CNN with Conv2D, MaxPooling, Dropout layers.  
   - **Model 2:** Transfer learning with EfficientNetB0 pretrained on ImageNet.

4. **Evaluation**  
   - Accuracy/loss curves.  
   - Confusion matrix and classification report.  
   - Analysis of discrepancies between training, validation, and test performance.

5. **Summary & Future Work**  
   - CNN achieved **~78% validation accuracy**.  
   - Transfer learning (EfficientNetB0) underperformed due to domain gap and limited dataset.  
   - Future improvements: MRI-specific preprocessing, deeper fine-tuning, and medical-pretrained models.

---

## 📊 Results Overview

| Model                   | Train Accuracy | Val Accuracy | Test Accuracy |
|-------------------------|---------------:|-------------:|--------------:|
| Custom CNN (from scratch) | 81.05%         | 78.00%       | ~74%          |
| EfficientNetB0 TL       | 61.36%         | 62.00%       | ~54%          |

---

## ⚙️ Requirements
- Python 3.8+
- TensorFlow / Keras
- NumPy, Pandas
- Matplotlib, Seaborn
- OpenCV (for optional MRI-specific preprocessing)

