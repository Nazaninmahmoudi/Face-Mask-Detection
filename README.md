# Face-Mask-Detection-Deep Learning

## **📌Project Overview**
This project explores face mask detection by building a custom CNN model and comparing its performance with a transfer learning approach. It evaluates both models on a balanced dataset and analyzes their generalization ability on real-world images, highlighting the benefits of using pretrained networks for visual classification tasks.


### **⚙️CNN Model Summary**
A CNN model was designed for binary face mask classification using 128×128×3 RGB images. It consists of:

Conv2D (32) + MaxPooling: Extracts low-level features.

Conv2D (64) + MaxPooling: Captures more abstract patterns.

Flatten + Dense (128, ReLU) + Dropout (0.5)

Dense (64, ReLU) + Dropout (0.5)

Dense (2, Softmax): Outputs class probabilities for with_mask and without_mask.

The model uses ReLU activations and dropout for regularization.

### **📈 Model Evaluation**
Testing on a test set of 1,511 images, with an overall accuracy of 92.85% and no major class bias.

**Precision:**

 • With Mask: ~93.2%
 
 • Without Mask: ~92.4%

**Recall:**

 • With Mask: ~92.6%
 
 • Without Mask: ~93.0%

**F1-Score: ~92.7% (both classes)**

**AUC: 0.98** — indicating excellent separability and low false-positive rate

**Training Accuracy: ~96%**

**Validation Accuracy: ~92%**

**Testing on Unseen Data :  96.24%**

🎥**Live Webcame Test:**

With Mask: ~93% average confidence

Without Mask: ~83.65% average confidence

### **👁️ Explainable AI (XAI)**
To interpret predictions, Integrated Gradients (IG) was applied:

Computes pixel-level attributions for the predicted class

Generates colored heatmaps to visualize influential regions

Displays: Original Image | Heatmap | Overlay


## ⚖️ Coparing Evaluation Results:

| **Metric**                      | **Implemented CNN**                             | **MobileNetV2**                 |
|:------------------------------:|:------------------------------------------:|:-------------------------------------:|
| **Train Accuracy**              | \~95.3%                                    | \~99.5%                               |
| **Validation Accuracy**         | \~95.5%                                    | \~98.5%                               |
| **Test Accuracy**               | 95.5%                                      | **99%**                               |
|                                 |                                            |                                       |
| **Precision**                   | With Mask: 96.4%  <br> Without Mask: 94.4% | With Mask: 98% <br> Without Mask: 99% |
| **Recall**                      | With Mask: 94.7%  <br> Without Mask: 96.4% | With Mask: 99% <br> Without Mask: 98% |
| **F1-Score**                    | \~95% (both classes)                       | **\~99% (both classes)**              |
| **False Positives**             | 27                                         | **4**                                 |
| **False Negatives**             | 41                                         | **16**                                |
|                                 |                                            |                                       |
| **AUC (ROC)**                   | 0.99                                       | **1.00 (perfect)**                    |
| **Average Precision (AP)**      | **0.99**                                   | **0.99**                              |
|                                 |                                            |                                       |
| **Unseen Data Accuracy**        | 87.06%                                     | **90%**                               |
| **Webcam Inference Confidence** | With Mask: 93% <br> Without Mask: 83.65%   | With Mask: 99% <br> Without Mask: 99% |
|                                 |                                            |                                       |
| **Overfitting Observed?**       | No – good generalization                   | No – very stable                      |
| **XAI Insight**                 | acceptable focus on facial areas      | had decent more precise facial focus |


### For more detailed information and in-depth analysis, please refer to the Jupyter notebooks included in this repository.


## **🗂️ Dataset Summary**

Total: 13,600 images (balanced)

Classes: With Mask / Without Mask

 • Train: 10,880
 
 • Val: 1,360
 
 • Test: 1,360

Each split contains equal samples per class.

Kaggle Dataset URL: https://www.kaggle.com/datasets/omkargurav/face-mask-dataset



## 👩‍💻**Contact**


📌 Project by: Nazanin Mahmoudy, 2025                 
📧 Email: nazaninmahmoudy@gmail.com                 
🔗 GitHub: github.com/NazaninMahmoudi                    
🔗 Kaggle: kaggle.com/nazaninmahmoudy                      

