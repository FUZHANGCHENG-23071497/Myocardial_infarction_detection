# Early Myocardial Infarction Detection over Deep Learning based on Echocardiography

## 🩺 Introduction
Myocardial infarction (MI), commonly known as a heart attack, is a major cause of morbidity and mortality worldwide. Early detection plays a crucial role in improving patient outcomes. Traditional diagnostic techniques are time-consuming and heavily reliant on expert interpretation of echocardiographic images.  

This project explores the use of **deep learning-based models** to analyze echocardiographic videos (A2C and A4C views) for the early detection of myocardial infarction. The approach leverages both **spatial and temporal features** of the heart by implementing **CNN+LSTM** and **3D CNN architectures**.

Kaggle Dataset: https://www.kaggle.com/datasets/aysendegerli/hmcqu-dataset

---

## 🎯 Objectives
- To preprocess and standardize echocardiographic videos into machine-readable formats.  
- To implement **CNN+LSTM** and **3D CNN** models for detecting early MI.  
- To evaluate model performance across different echocardiographic views (A2C, A4C).  
- To provide a framework for future clinical AI systems in cardiology.  

---

## 🧪 Methodology
1. **Data Acquisition & Preprocessing**  
   - Convert `.avi` echocardiography videos to `.npy` format using  
     [save_avi_to_npy.ipynb](save_avi_to_npy.ipynb)
   - Metadata and labels are provided in:  
     - [A2C Dataset (CSV)](A2C.csv)  
     - [A4C Dataset (CSV)](A4C.csv) 
   - Videos can be visualized with  
     [display_npy_video.ipynb](display_npy_video.ipynb)

2. **Model Architectures**  
   - **CNN+LSTM:**  
     - Implemented in [hmc_qu_cnn+lstm_model_training.ipynb](notebook/hmc_qu_cnn%2Blstm_model_training.ipynb).  
     - CNN extracts spatial features; LSTM models temporal dependencies.  
   - **3D CNN:**  
     - Implemented in [hmc_qu_3d_cnn_model_training.ipynb](notebook/hmc_qu_3d_cnn_model_training.ipynb).  
     - Learns spatio-temporal features directly from video volumes.  

3. **Training & Evaluation**  
   - General training workflows available in [hmc_qu_model_training.ipynb](hmc_qu_model_training.ipynb).
   - Metrics: Accuracy, Precision, Recall, F1-score.  
   - Comparison between A2C and A4C view performance.  

---

## 📊 Dataset
- **A2C (Apical 2-Chamber) and A4C (Apical 4-Chamber)** echocardiographic views.  
- Labels:  
  - **MI**: Presence of regional wall motion abnormalities.  
  - **Non-MI**: Normal cardiac function.  
- Ground-truth labels provided by domain experts.  

---

## 📚 References
[P1] A. Degerli, S. Kiranyaz, T. Hamid, R. Mazhar, and M. Gabbouj, “Early Myocardial Infarction Detection over Multi-view Echocardiography,” Biomedical Signal Processing and Control, vol. 87, 2024, https://doi.org/10.1016/j.bspc.2023.105448.

[P2] A. Degerli, M. Zabihi, S. Kiranyaz, T. Hamid, R. Mazhar, R. Hamila, and M. Gabbouj, "Early Detection of Myocardial Infarction in Low-Quality Echocardiography," in IEEE Access, vol. 9, pp. 34442-34453, 2021, https://doi.org/10.1109/ACCESS.2021.3059595.

[P3] S. Kiranyaz, A. Degerli, T. Hamid, R. Mazhar, R. E. F. Ahmed, R. Abouhasera, M. Zabihi, J. Malik, R. Hamila, and M. Gabbouj, "Left Ventricular Wall Motion Estimation by Active Polynomials for Acute Myocardial Infarction Detection," in IEEE Access, vol. 8, pp. 210301-210317, 2020, https://doi.org/10.1109/ACCESS.2020.3038743.

[P4] I. Adalioglu, M. Ahishali, A. Degerli, S. Kiranyaz and M. Gabbouj, "SAF-Net: Self-Attention Fusion Network for Myocardial Infarction Detection Using Multi-View Echocardiography," 2023 Computing in Cardiology (CinC), pp. 1-4, 2023, https://doi.org/10.22489/CinC.2023.240.

---

## ⚖️ License
This project is released under the **MIT License**.  

---
