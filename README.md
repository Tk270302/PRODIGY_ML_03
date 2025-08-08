# PRODIGY_ML_03
# 🐱🐶 Cats vs Dogs Classification using VGG16 Features + SVM

This is Task 3 of my virtual internship at **Prodigy InfoTech** under the Machine Learning track.  
In this project, I implemented an **SVM classifier** using **VGG16 pretrained CNN features** to classify images of cats and dogs.  
This approach significantly improves accuracy compared to using raw pixels, especially for small datasets.

---

## 🧠 Task Summary

- **Goal**: Classify images of cats and dogs into their respective categories.
- **Dataset**: Custom subset from Kaggle Dogs vs Cats dataset (70 images of cats and 70 images of dogs in both train and test sets).
- **Approach**:  
  - Extract deep features from images using **VGG16** pretrained on ImageNet (without the top classifier layer).  
  - Train a **Linear SVM** on these extracted features.
- **Why**: SVM performs better with high-quality features; VGG16 provides rich feature representations.

---

## 📌 Features Used

- Input images resized to **128×128×3** pixels.
- Preprocessing: `VGG16.preprocess_input` applied before feeding into the model.
- Output: Flattened convolutional features from VGG16 for SVM classification.

---

## 📈 Workflow

1. **Load and preprocess** images (resize, normalize).
2. **Feature extraction** using VGG16 (`include_top=False`).
3. **Flatten features** for input to SVM.
4. **Train SVM classifier** with a linear kernel.
5. **Evaluate** with accuracy, classification report, and confusion matrix.

---

## 🖼️ Sample Output

- Classification accuracy: **~80–90%** on the small dataset.
- Confusion matrix visualization for prediction results.

---

## 🚀 Technologies Used

- Python
- TensorFlow / Keras
- scikit-learn
- NumPy
- Matplotlib, Seaborn

---

## Result

<img width="461" height="617" alt="image" src="https://github.com/user-attachments/assets/2d3cb9e7-8c02-4eec-9a8f-7e9b5877fdee" />


---

## 📂 Files

- `task3_vgg16_svm_cats_dogs.ipynb` — full code
- `archive/` — dataset folder with `train/` and `test/` subfolders for cats and dogs.
- `README.md` — project documentation

---
