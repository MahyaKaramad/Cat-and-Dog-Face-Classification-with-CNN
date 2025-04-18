# 🐶🐱 Cat and Dog Face Classification with CNN

This project is a deep learning-based image classification system designed to distinguish between cats and dogs using facial images. Developed as part of the *Deep Learning (SEP 740)* course under Dr. Sayyed Faridoddin Afzali, the model was implemented using TensorFlow and Keras, and explores the impact of various architectural and training strategies on classification performance.

## 📌 Project Overview

The core goal of this project is to develop a binary image classifier that can accurately predict whether a given image is of a cat or a dog, with a particular focus on facial features. Through iterative experimentation and data-driven refinement, the final Convolutional Neural Network (CNN) model achieves:

- ✅ **Training Accuracy**: 99.68%  
- ✅ **Validation Accuracy**: 97.69%  
- ⚠️ **Validation Loss**: 0.15 (Fluctuation observed; focus on improvement continues)

## 🧠 Key Features

- **Custom CNN Architecture** optimized with:
  - Conv2D + BatchNorm + MaxPooling blocks
  - Dropout & L2 Regularization to combat overfitting
  - Flatten + Dense layers with Sigmoid output
- **Advanced Training Techniques**:
  - EarlyStopping with model checkpointing
  - Learning rate tuning
  - Data augmentation (rotation, zoom, flipping)
- **Experiments with hyperparameters**, label types, and loss functions
- **Transition from general pet datasets** to focused facial image datasets like **PetFace** for better consistency and accuracy

## 📂 Dataset

- Initial Dataset: [Kaggle Cats vs Dogs](https://www.kaggle.com/datasets/samuelcortinhas/cat-and-dog)
- Final Dataset: [PetFace Dataset](https://arxiv.org/abs/2407.13555)
- Folder Structure:
  ```
  ├── train/
  │   ├── cat/
  │   └── dog/
  ├── validate/
      ├── cat/
      └── dog/
  ```

## 📊 Results & Lessons Learned

- **Overfitting** was the biggest challenge; solved through:
  - Dropout up to 0.6
  - L2 Regularization
  - Learning rate reduction (0.0001)
  - Proper dataset curation
- **Data consistency** had a massive impact: clean, focused face images worked far better than diverse body or AI-generated shots.
- **Proper label format** (integer vs float) directly affected model performance due to the loss function requirements.

## 🔭 Future Work

- Integrate **transfer learning** using pre-trained models like **ResNet** and **EfficientNet**
- Explore more robust **augmentation strategies**
- Convert the model into a **deployable API or mobile application**
- Expand to **multi-class classification** (e.g., cat breeds, dog breeds)

## 📚 References

The full list of citations and research sources is available in the final report.