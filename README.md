# 🐾 AI-Based Wildlife Species Identification  
### Vision Transformer (ViT) for Camera Trap Image Classification  

**Author:** Khadija Saeed  
Department of Computer Science  
University of Engineering and Technology (UET), Lahore, Pakistan  

---

## 📌 Project Overview

This project presents a **high-performance wildlife species classification system** using a **Vision Transformer (ViT-B/16)** model. The system automatically identifies animals in camera trap images to support:

- 🌿 Biodiversity monitoring  
- 🐘 Wildlife conservation  
- ⚠️ Human–wildlife conflict prevention  
- 🚨 Public safety alert systems  

The model was fine-tuned on the **Animals-10 dataset** and achieved:

- ✅ **98.04% Validation Accuracy**
- ✅ **98.41% Test Accuracy**

The system outperforms several traditional CNN-based architectures in both accuracy and robustness.

---

## 🎯 Objectives

- Develop an automated wildlife species identification system.
- Improve classification performance in:
  - Low-light conditions  
  - Complex backgrounds  
  - Partially occluded animals  
- Provide explainable AI outputs using **LIME**.
- Compare transformer-based performance with CNN architectures.

---

## 🗂 Dataset

**Dataset Used:** Animals-10 (Kaggle)  
**Total Images:** 38,285  
**Number of Classes:** 10 animal species  

| Class       | Samples |
|------------|----------|
| Cat        | 2,493 |
| Dog        | 7,088 |
| Horse      | 3,826 |
| Butterfly  | 3,089 |
| Elephant   | 2,141 |
| Chicken    | 4,543 |
| Spider     | 7,035 |
| Squirrel   | 2,716 |
| Cow        | 2,708 |
| Sheep      | 2,646 |

### Dataset Split
- 70% Training  
- 15% Validation  
- 15% Testing  

---

## 🏗 Model Architecture

We used **Vision Transformer (ViT-B/16)** pretrained on ImageNet-21k.

### Key Components

- Image resizing to **224×224**
- Patch size: **16×16**
- Linear patch embedding
- Positional encoding
- Transformer encoder blocks (Self-attention mechanism)
- Modified classification head (10 output classes)
- Transfer learning (frozen backbone + fine-tuned classifier)

### Why Vision Transformer?

Unlike CNNs, ViT:

- Captures **global relationships** in images  
- Performs better with **partially visible objects**  
- Handles complex backgrounds effectively  

---

## 🛠 Tech Stack

- Python  
- PyTorch  
- Hugging Face Transformers  
- OpenCV  
- NumPy  
- Matplotlib  
- LIME (Explainability)  
- Google Colab (Tesla T4 GPU)  

---

## ⚙️ Training Configuration

| Parameter | Value |
|------------|--------|
| Optimizer | Adam |
| Learning Rate | 2e-5 |
| Batch Size | 32 |
| Epochs | 12 |
| Loss Function | Cross-Entropy |
| Early Stopping | Enabled |
| LR Scheduler | Enabled |

**Training Time:** ~3 hours (Tesla T4 GPU)

---

## 📊 Performance Metrics

### Final Test Results

- **Accuracy:** 98.41%  
- **Precision:** 98.12%  
- **Recall:** 98.35%  
- **F1-Score:** 98.23%  
- **Best Validation Accuracy:** 98.04%

### Key Improvements

- +6.4% accuracy improvement over traditional CNN models  
- +22% boost in identifying hard-to-classify animals  
- Strong performance in partially occluded conditions  

---

## 🔍 Explainability with LIME

To improve transparency and trust, we integrated **LIME (Local Interpretable Model-Agnostic Explanations)**.

LIME highlights:

- Important image regions influencing predictions  
- Model focus areas (e.g., elephant ears, butterfly wings)

This increases reliability for:

- Ecological research  
- Wildlife monitoring departments  
- Public safety systems  

---

## 📈 Evaluation Tools

- Confusion Matrix  
- Accuracy & Loss Curves  
- Class-wise Precision & Recall  
- F1-Score  
- LIME Visual Explanations  

---

## ⚠️ Limitations

- Slight performance drop in underrepresented classes (e.g., squirrel)  
- Background clutter may affect predictions  
- Hardware constraints limit batch size scalability  

---

## 🔮 Future Improvements

- Hybrid CNN + ViT architectures  
- Advanced augmentation strategies  
- Class balancing techniques  
- Edge AI deployment for real-time wildlife alerts  
- Larger transformer models (ViT-L, Swin Transformer)

---

## 🌍 Real-World Applications

- Wildlife monitoring in national parks  
- Endangered species tracking  
- Human–wildlife conflict prevention  
- Smart surveillance systems  
- Ecological research automation  

---

## 👩‍💻 Author

**Khadija Saeed**  
Computer Science Student  
University of Engineering and Technology, Lahore  
📧 khadijasaeed683@gmail.com  

---

## ⭐ Support

If you found this project useful, please consider giving it a ⭐ on GitHub to support research in AI-driven wildlife conservation.

---

**Transformers for conservation. AI for safety.** 🐾🌿
