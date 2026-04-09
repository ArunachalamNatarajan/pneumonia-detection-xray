# 🩺 Pneumonia Detection using Chest X-Ray Images

## 📌 Problem Statement

Pneumonia is a serious lung infection that can be life-threatening if not detected early.
This project builds a deep learning model to classify chest X-ray images as:

* **Normal**
* **Pneumonia**

---

## 🎯 Objective

To develop a reliable deep learning model that assists in early detection of pneumonia using medical imaging.

---

## 📂 Dataset

Dataset used: Chest X-ray images (Kaggle)

* Training set
* Validation set
* Test set

All images are resized to **128x128** and normalized.

---

## ⚙️ Approach

### 1️⃣ Baseline CNN

* Built a CNN model from scratch
* Observed overfitting and poor generalization (~70% accuracy)

---

### 2️⃣ Transfer Learning (Final Model) 🚀

* Used **MobileNetV2 (pretrained on ImageNet)**
* Frozen base model for feature extraction
* Achieved **~86–87% test accuracy**

---

### 3️⃣ Fine-Tuning (Experiment)

* Attempted fine-tuning
* Resulted in overfitting due to limited data
* Not used in final model

---

## 🏋️ Model Training

* Loss: Binary Crossentropy
* Optimizer: Adam
* EarlyStopping used to prevent overfitting

---

## 📊 Evaluation

* Test Accuracy: **~86–87%**
* Balanced precision and recall
* Strong pneumonia detection performance

---

## 🎯 Threshold Optimization

A threshold of **0.4** was used instead of 0.5 to:

* Reduce missed pneumonia cases
* Improve recall (important in healthcare)

---

## 🧪 Inference

The trained model predicts new chest X-ray images:

* Resized to (128,128)
* Normalized
* Prediction based on trained model

---

## 💾 Model Saving

```python
model.save("final_pneumonia_model.keras")
```

---

## 🧠 Tech Stack

* Python
* TensorFlow / Keras
* NumPy
* Scikit-learn

---

## 🚀 Future Improvements

* Use larger datasets
* Try EfficientNet
* Deploy using Streamlit

---

## 📌 Conclusion

Transfer learning significantly improved performance over a baseline CNN.
The model demonstrates strong potential for assisting in early pneumonia detection.

---

## 👤 Author

**Arunachalam**
