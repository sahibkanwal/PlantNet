# PlantNet 🌽  
Corn Crop Disease Classifier – APS360 Project (University of Toronto)  

> **Note:** This repository documents the project only. **Source code is not included** per course policy.

## 📖 Overview  
PlantNet is a deep learning project developed for **APS360: Applied Fundamentals of Deep Learning** at the University of Toronto.  

Corn is one of Ontario’s most important crops, but diseases like **Common Rust, Gray Leaf Spot, and Northern Corn Leaf Blight** can cause major yield losses and put farmer livelihoods at risk. The challenge is that symptoms are often subtle, appear late, or are visually similar, making them hard to detect with the human eye.  

PlantNet uses **convolutional neural networks (CNNs)** to recognize these patterns, supporting farmers with faster and more reliable disease detection in the field.  

<img width="1730" height="595" alt="image" src="https://github.com/user-attachments/assets/ed241946-e6cb-43d9-a8c7-a0b5ebf4caca" />

---

## 🔑 Key Features  
- **Custom feature extractor** pretrained on thousands of non-corn plant disease images.  
- **Corn-specific classifier** trained exclusively on multiple real-world corn datasets.  
- Achieved **94% accuracy** on validation data and **96% accuracy** on unseen datasets.  
- Robust across varied lighting, backgrounds, and field conditions.  

---

## 📂 Datasets  
- **Pretraining**: [PlantVillage](https://arxiv.org/abs/1511.08060), [PlantDoc](https://doi.org/10.1145/3371158.3371196) (corn excluded).  
- **Corn fine-tuning**:  
  - [CD&S Dataset (Ahmad et al., 2021)](https://osf.io/s6ru5/)  
  - [Roboflow Corn Diseases](https://universe.roboflow.com/corn-disease-7/corn-diseases-oxojk)  
  - [IDADP (Lei et al., 2025)]  

---

## ⚙️ Technical Details  
- **Architecture**: LargeNet (AlexNet-inspired CNN with BatchNorm, Dropout, Adaptive Pooling).  
- **Training**:  
  - Optimizer: Adam  
  - Learning Rate: 0.001  
  - Batch Size: 64  
  - Epochs: 50  
- **Framework**: PyTorch
  
<img width="959" height="444" alt="image" src="https://github.com/user-attachments/assets/7e7d6af1-662d-4b8d-9f18-9e48e0be63ac" />

---

## 📊 Results  
- Validation Accuracy: **94%**  
- Accuracy on unseen test datasets: **96%**  
- Improved significantly over a baseline CNN (86%).  
- Qualitative results show strong classification, with occasional confusion between visually similar diseases such as Northern Corn Leaf Blight and Gray Leaf Spot.  

---

## 🌱 Motivation  
This project demonstrates how deep learning can move beyond the lab and into real-world problems. By detecting corn diseases early, tools like PlantNet could:  
- Reduce the need for costly lab testing.  
- Save farmers time and resources.  
- Lower the uncertainty of visual inspection.  

Our aim was not just high accuracy, but to imagine how accessible tools like this could support farmers and Ontario’s agricultural economy.  

---

## 👥 Team  
Developed by **Group 45** (APS360, University of Toronto):  
- Kishan Patel  
- Sahib Kanwal  
- Aditya Pisharoty  
- Mark Samuel  

---

## ⚖️ Ethical Considerations  
While PlantNet shows strong accuracy, false positives and false negatives can still occur. Farmers should use this tool as a decision aid rather than a replacement for expert assessment. Dataset bias (e.g., lighting, geography, corn variety) is another limitation that must be addressed before field deployment.  

---

## 📌 References  
- Hughes & Salathé, 2015 – PlantVillage Dataset.  
- Singh et al., 2020 – PlantDoc Dataset. 
- Ahmad et al., 2021 – CD&S Dataset.  
- Lei et al., 2025 – IDADP Dataset.  
- Mohanty et al., 2016 – Early CNNs for Plant Disease Detection.  
- Ferentinos, 2018 – Deep Learning for Crop Diseases.  
- Li et al., 2024 – Lightweight YOLOv8s for Corn Disease.   
