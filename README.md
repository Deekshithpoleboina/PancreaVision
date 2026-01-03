# 🏥 PancreaVision — AI-Powered Pancreatic Cancer Detection System

PancreaVision is a **full-stack AI-based medical diagnostic prototype** developed as a **final-year B.Tech Computer Science project**.  
It demonstrates how **Deep Learning models** can be integrated into a real-world web application to assist in the **early detection of pancreatic cancer** from CT scan images.

> ⚠️ **Medical Disclaimer**  
> This software is a **research and educational prototype only**.  
> It is **not a certified medical device** and must **not** be used for real clinical diagnosis or treatment decisions.

---

## 🚀 Features

- **AI-Based Diagnosis**  
  Uses a **ResNet50-based transfer learning model** with custom classification layers to classify CT scans as **Benign** or **Malignant**.

- **Prediction Confidence**  
  Displays probability scores to indicate diagnostic confidence.

- **Patient Data Management**  
  Stores patient details and diagnosis history for reference.

- **Doctor Authentication**  
  Basic login and signup functionality using hashed credentials.

- **Interactive Dashboard**  
  Clean and responsive UI built with **React + Tailwind CSS**.

- **Local Database Storage**  
  Patient records stored in a **local MongoDB database**.

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
## ⚠️ Dataset Note

The dataset images are included **only for academic demonstration and ease of local testing**.  
In real-world production systems, **medical datasets would never be committed to version control** and would be stored using secure, compliant storage solutions.

---

## ⚙️ Installation & Local Setup

### ❗ Deployment Note

This project is **not deployed** on platforms like Vercel or Render because it involves:

- Large medical image datasets
- Local ML model execution
- High compute and storage requirements

The application is intended to be **run locally** for evaluation and learning purposes.

---

## 1️⃣ Prerequisites

Ensure the following are installed:

- Python **3.8+**
- Node.js & npm
- MongoDB Community Server (running on `localhost:27017`)
- Git

---

## 2️⃣ Backend Setup (Flask + ML)

### Navigate to backend
```bash
cd backend
```

## 2️⃣ Backend Setup (Flask + ML)

### Create & activate virtual environment

**Windows**
```bash
python -m venv venv
venv\Scripts\activate
```
**Mac / Linux**
```bash
python3 -m venv venv
source venv/bin/activate
```
**Install dependencies**
```bash
pip install -r requirements.txt
```
**Dataset structure**
```text
backend/dataset/
├── benign/
└── malignant/
```
**Train the AI model**
```bash
python train_model.py
```
**Start backend server**
```bash
python app.py
```
**Backend runs at:**
```bash
http://localhost:5000
```

---

## 📖 How to Use the Application

1. Ensure **MongoDB** is running.
2. Start the **backend server**.
3. Start the **frontend server**.
4. Open `http://localhost:5173`.
5. Register or log in as a doctor.
6. Enter patient details.
7. Upload a CT scan image.
8. View prediction and confidence score.
9. Access diagnosis history.

---

## 🧠 How the AI Model Works

- **Input**: CT scan resized to `224 × 224`
- **Feature Extraction**: ResNet50 CNN extracts visual patterns
- **Classification**: Custom dense layers analyze features
- **Output**:
  - Value between `0` and `1`
  - `> 0.5` → **Malignant**
  - `≤ 0.5` → **Benign**

---

## 🎯 Learning Outcomes

- End-to-end **product development**
- Integrating **ML models** into real applications
- Frontend–backend communication
- Debugging and refactoring complex systems
- Practical experience with **AI-driven products**

---

## 🤝 Contributing

This project is open for learning and improvement.  
Suggestions related to:
- Model accuracy
- UI enhancements
- Code refactoring  

are welcome.
