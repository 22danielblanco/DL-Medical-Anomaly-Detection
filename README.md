# 🏥 Medical Anomaly Detection with Deep Learning  

This repository contains a complete **Deep Learning pipeline** for **detecting medical anomalies** using **unsupervised and supervised models**. Several models, including **Autoencoders, Isolation Forest, DBSCAN, a Risk Prediction Model, and LSTM**, have been implemented to analyze real-time medical data and predict potential health risks.  

---

## 🚀 **Project Overview**  

📌 **Main Goals:**  
✅ Medical anomalies in patient data are identified using unsupervised models.  
✅ Detection accuracy is improved by combining multiple models (**Autoencoders + Isolation Forest + DBSCAN**).
✅ A supervised model is trained to classify anomalies based on past predictions. 
✅ A real-time system is provided, allowing users to input medical data and receive risk predictions.  
✅ Future anomalies are predicted using **LSTM** based on historical trends.  
 
---

## 🔬 **Implemented Models & Approaches**  

### **1️⃣ Autoencoders for Anomaly Detection**  
An **unsupervised autoencoder** was trained to learn patterns in normal patient data. The **reconstruction error (MSE)** is used to identify anomalies:  

🔹 **Normal data → Low reconstruction error** ✅  
🔹 **Anomalous data → High reconstruction error** 🚨  

📈 **Improvements Applied**:  
- The **latent space** was optimized to capture more meaningful features.  
- **Dropout layers** were adjusted to reduce overfitting.  
- The **error threshold** was dynamically tuned using **ROC-AUC**.  

---

### **2️⃣ Enhancing Detection with Isolation Forest & DBSCAN**  
To improve anomaly detection, **three different unsupervised models** were combined:  

✅ **Autoencoder** → Outliers are identified based on reconstruction error.  
✅ **Isolation Forest** → Anomalies are detected by isolating rare patterns.  
✅ **DBSCAN (Density-Based Spatial Clustering)** → Clusters and outliers are identified.  

🔹 **Final Anomaly Decision:** If at least **two models** detect an anomaly, it is marked as **critical**.  

---

### **3️⃣ Real-Time Anomaly Detection with the Risk Model**  
To make the system interactive, a **supervised model** was trained to classify anomalies based on previous detections.  

✅ **User input is allowed** (Heart Rate, SpO2, Glucose, etc.).  
✅ **The risk of an anomaly is predicted** based on input data.  
✅ **Autoencoder and Isolation Forest results are used for classification.**  
✅ **More accurate results are achieved compared to standalone unsupervised models.**  

#### **📌 Testing the Model with User Input in Google Colab**
An interactive interface was implemented in Google Colab, allowing users to:  
1️⃣ **Manually input their medical data**.  
2️⃣ **Receive a real-time risk assessment** using the trained model.  

---

### **4️⃣ LSTM-Based Anomaly Prediction (Time-Series Analysis)**
A **Long Short-Term Memory (LSTM)** network was trained to analyze time-series medical data and predict future anomalies.

✅ Historical trends are analyzed to anticipate future risks.
✅ An attention mechanism is used to focus on key medical variables.
✅ False positives are reduced by analyzing trends over time.

---

## Run in Google Colab
The .ipynb file can be opened in Google Colab, where users can run the cells and interact with the model in real time.
