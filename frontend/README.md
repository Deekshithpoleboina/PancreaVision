# 🏥 PancreaVision — AI-Powered Pancreatic Cancer Detection System

PancreaVision is a **full-stack AI-based medical diagnostic prototype** developed as a **final-year B.Tech Computer Science project**.  
It demonstrates how **Deep Learning models** can be integrated into a real-world web application to assist in the **early detection of pancreatic cancer** from CT scan images.

![Status](https://img.shields.io/badge/Status-Final%20Year%20Project-orange)
![Stack](https://img.shields.io/badge/Stack-React%20%7C%20Flask%20%7C%20TensorFlow-blue)

> ⚠️ **Medical Disclaimer**  
> This software is a **research and educational prototype only**.  
> It is **not a certified medical device** and must **not** be used for real clinical diagnosis or treatment decisions.

---

## 🚀 Features

- **AI-Based Diagnosis**
  - Uses a **ResNet50-based transfer learning model** with custom classification layers to classify CT scans as **Benign** or **Malignant**.
- **Prediction Confidence**
  - Displays probability scores to indicate diagnostic confidence.
- **Patient Data Management**
  - Stores patient details and diagnosis history for reference.
- **Doctor Authentication**
  - Basic login and signup functionality using hashed credentials.
- **Interactive Dashboard**
  - Clean and responsive UI built with **React + Tailwind CSS**.
- **Local Database Storage**
  - Patient records stored in a **local MongoDB database**.

---

## 🛠️ Tech Stack

### Frontend
- React (Vite)
- Tailwind CSS
- Axios
- React Router DOM

### Backend
- Python (Flask)
- TensorFlow / Keras
- MongoDB (Community Edition – Local)
- Pillow (Image Processing)
- NumPy

### Machine Learning
- Model: **ResNet50 (Transfer Learning)**
- Input: 2D CT scan slices
- Output: Binary classification (Benign / Malignant)

---

## 📂 Project Structure

```text
PancreaVision/
├── backend/
│   ├── dataset/
│   │   ├── benign/
│   │   └── malignant/
│   ├── app.py
│   ├── train_model.py
│   ├── pancreas_model.h5
│   └── requirements.txt
│
└── frontend/
    ├── src/
    │   ├── components/
    │   └── pages/
    ├── package.json
    └── vite.config.js
```
