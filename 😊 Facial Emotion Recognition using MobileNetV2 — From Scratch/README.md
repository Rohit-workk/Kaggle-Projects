# 😊 Facial Emotion Recognition using MobileNetV2 — From Scratch

This project performs **Exploratory Data Analysis (EDA)**, **data preprocessing**, and **deep learning-based emotion classification** using the [Facial Emotion Recognition Dataset](https://www.kaggle.com/datasets/fahadullaha/facial-emotion-recognition-dataset/data).

The notebook demonstrates a complete end-to-end workflow — from dataset visualization and augmentation to transfer learning using **MobileNetV2** — achieving robust results for emotion recognition.

---

## 📊 Dataset Overview

**Dataset Link:** [Facial Emotion Recognition Dataset](https://www.kaggle.com/datasets/fahadullaha/facial-emotion-recognition-dataset/data)  
**Structure:** The dataset consists of preprocessed facial images categorized into **7 emotion classes**:

| Emotion | Image Count |
|----------|-------------|
| surprise | 5920 |
| fear     | 5920 |
| angry    | 5920 |
| neutral  | 8166 |
| sad      | 6535 |
| disgust  | 5920 |
| happy    | 11398 |

**Total Images:** 49,779  
**Image Size:** 96 × 96 pixels (RGB)

---

## 🔍 Exploratory Data Analysis (EDA)

### 🧩 Steps:
1. **Loaded and inspected dataset structure:**  
   Listed all emotion folders and counted images per class to analyze class balance.
2. **Visualized Class Distribution:**  
   Created a Seaborn barplot showing the number of images per emotion category.  
   - Observed clear **class imbalance** — especially more samples for *happy* and *neutral*.
3. **Displayed Sample Images:**  
   Plotted 5 sample images per emotion class using `matplotlib` to visually confirm dataset quality and class diversity.

### 💡 EDA Insights:
- The dataset is slightly imbalanced, with **“happy”** and **“neutral”** being dominant.  
- Image dimensions (96×96) make it suitable for lightweight CNN architectures like MobileNetV2.  
- Some emotions like *disgust* and *fear* are underrepresented — handled later via data augmentation.

---

## 🧠 Data Augmentation and Preprocessing

To balance and enhance dataset variability, **`ImageDataGenerator`** from Keras was used.

### Augmentation Techniques Applied:
- Random rotations (±20°)  
- Width & height shifts (±20%)  
- Shear and zoom transformations  
- Horizontal flips  
- Normalization (rescaling by 1/255)

### Data Split:
- **Training:** 80% (≈39,824 images)  
- **Validation:** 20% (≈9,955 images)

This approach reduced overfitting and improved generalization.

---

## ⚙️ Model Architecture — Transfer Learning with MobileNetV2

### 🔧 Base Model:
- Used **MobileNetV2** pretrained on ImageNet as the base feature extractor.  
- Input shape: `(96, 96, 3)`  
- Top layers removed (`include_top=False`)  
- Base model initially **frozen** to train only custom classification layers.

### 🧱 Custom Head:
- Global Average Pooling  
- Dropout (0.5) for regularization  
- Dense layer with 7 neurons and **softmax activation**

### ⚙️ Compilation:
python
optimizer = Adam(learning_rate=1e-3)
loss = 'categorical_crossentropy'
metrics = ['accuracy']


# 😊 Facial Emotion Recognition using MobileNetV2 (Transfer Learning)

This project focuses on building a **Facial Emotion Recognition (FER)** model using the **MobileNetV2** architecture through transfer learning.  
The model classifies human emotions from facial images into seven categories:  
`angry`, `disgust`, `fear`, `happy`, `neutral`, `sad`, and `surprise`.

---

## 📊 Dataset

**Source:** [Facial Emotion Recognition Dataset – Kaggle](https://www.kaggle.com/datasets/fahadullaha/facial-emotion-recognition-dataset/data)

- Total Images: **49,779**
- Image Size: **96×96 pixels**
- Emotions Covered: 7
- Observed class imbalance — particularly fewer samples in some emotion categories.

A visualization of the dataset distribution was performed, showing varying counts per emotion class (with `happy` having the largest share).

---

## ⚙️ Model Architecture

**Base Model:** MobileNetV2 (pretrained on ImageNet)  
**Input Size:** 96×96×3  
**Top Layers Added:**
- GlobalAveragePooling2D  
- Dropout (0.5)  
- Dense layer with Softmax activation (7 classes)

Initially, the MobileNetV2 base was frozen to train only the classifier layers.

---

## 🧩 Training and Performance

### Initial Training (Frozen Base)
- **Epochs:** 5  
- **Training Accuracy:** ~43.6%  
- **Validation Accuracy:** ~38.1%  
- **Loss:** ≈ 1.9  

This stage helped the model learn emotion-specific features without overfitting.

---

### 🔄 Fine-Tuning Phase
After initial training, the last 50 layers of MobileNetV2 were unfrozen and retrained with a **lower learning rate (1e-5)**.

| Epoch | Training Accuracy | Validation Accuracy | Validation Loss |
|-------|-------------------|---------------------|-----------------|
| 1 | 32.5% | 39.3% | 1.88 |
| 3 | 45.6% | 42.7% | 1.88 |
| 5 | 50.4% | 44.9% | 1.82 |
| 7 | 53.6% | 46.7% | 1.77 |
| 10 | 57.5% | 48.7% | 1.77 |

📈 **Visualization:**  
Accuracy and loss curves were plotted for both training and validation phases, showing steady improvements and minor overfitting at later epochs.

---

## 💡 Observations & Insights

- The model progressively learned emotion patterns, achieving **~49% validation accuracy**.  
- Overfitting began after epoch 8, mainly due to class imbalance and small image resolution.  
- Fine-tuning significantly boosted accuracy compared to training from scratch.  
- MobileNetV2 provided efficient training with moderate GPU usage.

---

## 🚀 Future Work

1. **Higher Resolution Inputs:**  
   Retrain using **255×255** images for improved facial detail extraction.

2. **Model Variations:**  
   - Experiment with **EfficientNet** or **custom CNNs**.  
   - Integrate **attention layers** for fine-grained emotion features.

3. **Regularization & Balancing:**  
   - Apply **SMOTE** or targeted augmentation.  
   - Introduce **Dropout** and **L2 regularization**.

4. **Web Application Integration:**  
   Build a real-time **Flask/Streamlit** app that:  
   - Accepts an uploaded image or webcam input  
   - Detects faces (via OpenCV/FaceNet)  
   - Predicts emotion using the trained model  
   - Displays real-time emotion tracking

---

## 🧰 Tools and Libraries

- **TensorFlow / Keras** — Model building & training  
- **OpenCV** — Image processing and visualization  
- **Matplotlib / Seaborn** — Data visualization  
- **NumPy / Pandas / OS** — Data handling and organization  
- **GPU Used:** Tesla P100 (Kaggle environment)

---

## 🤝 Credits

- **Dataset by:** [Fahad Ullah](https://www.kaggle.com/datasets/fahadullaha/facial-emotion-recognition-dataset/data)  
- **Developed by:** *Rohit*  
- **Model:** MobileNetV2 (Transfer Learning + Fine-Tuning)

---

## 📜 License

This project is intended for **educational and research purposes**.  
You may reuse or adapt the notebook with proper attribution.

