# NetSentinel: AI-Powered DDoS Detection in SDN Systems


## Overview
NetSentinel is a deep learning system designed to detect Distributed Denial of Service (DDoS) attacks in Software Defined Networking (SDN) environments.

This project focuses on building a model that can identify both common and evolving attack patterns using a combination of unsupervised feature learning and hybrid deep learning architectures.

---

## Problem Statement
Modern DDoS attacks are increasingly complex and difficult to detect using traditional rule-based or shallow machine learning methods. Key challenges include:

- High-volume and high-velocity network traffic  
- Evolving and previously unseen attack patterns  
- Severe class imbalance in real-world datasets  

This project aims to address these challenges using deep learning techniques.

---

## What I Built
- End-to-end deep learning pipeline for DDoS detection  
- Data preprocessing and feature engineering workflow  
- Stacked Sparse Denoising Autoencoder (SSDAE) for feature extraction  
- Hybrid CNN-LSTM model for classification  
- Evaluation framework with multiple performance metrics  

---

## Dataset
- CIC-DDoS2019 dataset  
- ~125,000 samples  
- 78 features  
- Multi-class classification (multiple attack types + benign traffic)

---

## Approach

### 1. Data Preprocessing
- Removed rows and columns with excessive missing values  
- Normalized feature values  
- Encoded labels for classification  
- Imputed missing data  
- Eliminated irrelevant or constant features  

### 2. Feature Learning (SSDAE)
- Used a stacked sparse denoising autoencoder  
- Learned compressed, noise-resistant feature representations  
- Improved model generalization  

### 3. Classification Model (CNN + LSTM)
- CNN layers for spatial feature extraction  
- LSTM layers for temporal pattern recognition  
- Dense layers for classification  
- Applied class weights to handle imbalance  

---

## Results
- Accuracy: ~79%  
- Weighted F1 Score: ~0.81  
- Macro F1 Score: ~0.51  

### Key Insights
- Strong detection performance for common attack types  
- Lower performance on rare classes due to imbalance  
- Effective combination of spatial and temporal learning  

---

## Challenges
- Handling severe class imbalance  
- Cleaning noisy and incomplete data  
- Improving performance on minority classes  

---

## Limitations
- Reduced accuracy on rare attack types  
- Not optimized for real-time deployment  
- Model compression not implemented  

---

## Future Improvements
- Advanced imbalance handling (SMOTE, ADASYN)  
- Model optimization (pruning, quantization)  
- Real-time deployment in SDN systems  
- Explainability (SHAP, LIME)  

---

## Tech Stack
- Python  
- TensorFlow / Keras  
- NumPy, Pandas  
- Scikit-learn  

---

## How to Run

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Run the notebook:
```bash
Open deepshield.ipynb and execute all cells
```

---

## Project Structure

```
.
├── deepshield.ipynb 
├── requirements.txt  
└── README.md  
```

---

## Conclusion
Deep Shield demonstrates how combining unsupervised feature learning with hybrid deep learning models can improve DDoS detection in SDN environments. The project reflects both the strengths and challenges of applying deep learning to real-world cybersecurity problems.
