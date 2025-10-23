# 🐶🐱 Dogs vs Cats Image Classification using CNN

## 🧠 Project Description
This project builds a Convolutional Neural Network (CNN) model to classify images of dogs and cats using TensorFlow and Keras.  
Using the Dogs vs Cats dataset from Kaggle, the network leverages image augmentation, convolutional layers, and dense layers for binary classification.  
The project covers full pipeline stages including data preprocessing, model building, training, validation, testing, evaluation, and visualization of results.

---

## 🎯 Objectives
- To create a deep learning model capable of distinguishing cats from dogs accurately.  
- To improve generalization through image augmentation techniques.  
- To evaluate model performance on unseen test images.  
- To provide clear visual insights of training dynamics and prediction results.

---

## 📂 Dataset
- **Source:** [Dogs vs Cats Dataset - Kaggle](https://www.kaggle.com/datasets/princelv84/dogsvscats)  
- **Training Images:** 16,000 images (used for training)  
- **Validation Images:** 4,000 images (from training set split)  
- **Test Images:** 5,000 images (used for final evaluation)  
- **Classes:** Two classes - cats (label 0) and dogs (label 1)

---

## ⚙️ Tools & Libraries Used
- Python  
- TensorFlow / Keras  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- PIL (Python Imaging Library)

---

## 🧩 Methodology

### Data Preparation
- Utilized `ImageDataGenerator` for real-time augmentation including normalization, rotation, zoom, and horizontal flips.  
- Set image size to 224×224 for uniform input and batch size of 32.  
- Split training data into 80% training and 20% validation sets with shuffling enabled to promote model learning variety.

### CNN Architecture
- Three convolutional blocks with increasing filter sizes (32, 64, 124) each followed by batch normalization and max-pooling layers.  
- Flattened feature maps before passing into fully connected (dense) layers with ReLU activations.  
- Final output layer uses sigmoid activation for binary classification.  

### Model Training
- Used binary cross-entropy loss with Adam optimizer.  
- Incorporated early stopping to avoid overfitting by monitoring validation loss with patience of 5 epochs.  
- Trained for up to 30 epochs with batches drawn from the augmented data generator.

---

## 📊 Results

### Training Performance
- Achieved approximately 90.5% training accuracy and 89.1% validation accuracy at final epoch.  
- Loss decreased steadily indicating effective learning and convergence.  
- Plots of accuracy and loss over epochs show consistent improvement and controlled overfitting.

### Test Performance
- Obtained a test accuracy of approximately 50%, indicating potential issues with model generalization or prediction mismatch.  
- Confusion matrix indicated that the model predicted all test images as cats, suggesting thresholding or evaluation logic needs adjustment.

---

## 🔍 Analysis & Insights
- The CNN architecture effectively learns patterns for cats and dogs during training and validation phases.  
- The large dense layer with over 14 million parameters suggests high model capacity but risks of overfitting.  
- Test evaluation revealed the importance of using appropriate decision thresholds on sigmoid outputs rather than argmax for binary classes.  
- Further techniques like class balancing, dropout regularization, or transfer learning could enhance robustness.

---

## 🛠️ Future Work
- Implement class weighting or oversampling techniques to address data imbalance.  
- Add dropout layers to reduce overfitting risks.  
- Experiment with pre-trained CNN models (e.g., VGG16, ResNet) via transfer learning.  
- Tune hyperparameters including learning rate, batch size, and network depth.  
- Develop a user-friendly front-end for real-time image classification.

---

## 💡 Conclusion
This project lays out a foundational image classification pipeline for distinguishing cats and dogs using CNNs.  
While training results are promising, test accuracy emphasizes the need for refined evaluation techniques and stronger generalization strategies.  
The work provides a basis for further exploration and improvement in deep learning image classifiers.

---
 
