
# 🧠 Fine-Tuning Cat and Dog Classifier with ResNet50

This project represents the **second version** of my cat and dog classification project, where I explored using a **pre-trained ResNet50** model combined with fine-tuning techniques to improve classification performance.

---

## 📋 Project Overview

Initially, I disabled the trainable mode of the ResNet50 base model:

```python
base_model.trainable = False
```

Training was performed for **10 epochs** with a **learning rate of 0.0001**.

### 📊 Validation Dataset:
- **Total Validation Images**: 260
  - 130 cat images
  - 130 dog images

### 🧮 Confusion Matrix Results:
- **Cat Predictions**:
  - ✅ 121 cats correctly predicted
  - ❌ 5 cats incorrectly predicted
- **Dog Predictions**:
  - ✅ 121 dogs correctly predicted
  - ❌ 9 dogs incorrectly predicted

---

## 🔄 Fine-Tuning Step

After the initial training, I enabled the trainable mode of the base model:

```python
base_model.trainable = True
```

Training was continued for another **10 epochs** with a **reduced learning rate of 0.00001** to avoid overfitting and to carefully fine-tune the ResNet50 weights.

---

## ⚠️ Observations and Notes

Although the training and validation metrics were promising, testing on completely new images revealed occasional false predictions.

I believe this is primarily due to **data leakage**, meaning the training and validation datasets were very similar in style and content.  
Thus, the model learned patterns specific to the dataset instead of generalizing to truly new, unseen data.

> **Conclusion:**  
> To make the model more robust and reliable, a more diverse dataset with different styles, lighting, and backgrounds should be used.

---

✅ Future steps could involve:
- Using a larger, more varied dataset
- Applying stronger data augmentation techniques
- Experimenting with other pre-trained architectures like EfficientNet

---

## 🚀 Technologies Used

- TensorFlow
- Keras
- ResNet50 (Pre-trained on ImageNet)

---

# 📚 End of Report
