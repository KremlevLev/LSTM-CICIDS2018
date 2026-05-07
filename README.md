# Network Intrusion Detection System (NIDS) using LSTM

This project implements a Deep Learning model to detect network intrusions using the **CIC-IDS-2018** dataset. The model is built with **PyTorch** and leverages an **LSTM** architecture to classify network traffic.

##  Key Features
*   **Large-scale Data Handling:** Implemented efficient data loading and memory optimization (downcasting, sampling, and garbage collection) to process massive CSV files within Kaggle's RAM limits.
*   **Multiclass Classification:** Detects multiple attack types, including DDoS (LOIC-HTTP), Brute Force (FTP/SSH), and Benign traffic.
*   **Deep Learning Pipeline:** End-to-end PyTorch implementation including custom `Dataset`, `DataLoader`, and `LSTM` architecture.

##  Performance
The model achieves high reliability across multiple metrics:
*   **ROC AUC Score:** ~0.9945
*   **DDoS Recall:** 0.95 (High detection rate for active threats)
*   **Overall Accuracy:** 98%

##  Tech Stack
*   **Framework:** PyTorch
*   **Data Analysis:** Pandas, NumPy, Scikit-learn
*   **Visualization:** Matplotlib, Seaborn

##  Challenges Addressed
*   **Memory Management:** Handled 30GB+ raw data by optimizing data types and using sampling techniques.
*   **Class Imbalance:** Evaluated performance using Confusion Matrix and ROC AUC instead of just Accuracy to ensure minority attack classes are detected.
