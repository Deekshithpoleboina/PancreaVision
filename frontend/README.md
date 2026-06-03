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
- **Database Storage**
  - Patient records stored in **MongoDB Atlas or a local MongoDB database** via `MONGODB_URI`.

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
- MongoDB (Atlas or Local)
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

>⚠️ **Dataset Note**
> The dataset images are included only for academic demonstration and ease of local testing.
> In real-world production systems, medical datasets would never be committed to version control and would be stored using secure, compliant storage solutions.

---

## ⚙️ Installation & Local Setup

### ❗ Deployment Note
This project can be deployed with a **Render backend** and **Vercel frontend** (see deployment steps below).

### 1️⃣ Prerequisites

Ensure the following are installed:

- Python **3.8+**
- Node.js & npm
- MongoDB Atlas connection string or a local MongoDB server
- Git

### 2️⃣ Backend Setup (Flask + ML)

#### Navigate to backend
```bash
cd backend
```

#### Create & activate virtual environment

Windows
```bash
python -m venv venv
venv\Scripts\activate
```

Mac / Linux
```bash
python3 -m venv venv
source venv/bin/activate
```

Install dependencies
```bash
pip install -r requirements.txt
```

Configure environment
```bash
export MONGODB_URI="mongodb+srv://<user>:<password>@<cluster>/<db>?retryWrites=true&w=majority"
export MONGODB_DB="pancreas_app_db"
```

### Dataset structure
```text
backend/dataset/
├── benign/
└── malignant/
```

Train the AI model
```bash
python train_model.py
```

Start backend server
```bash
python app.py
```

Backend runs at:
```bash
http://localhost:5000
```
### 3️⃣ Frontend Setup (React)

Open a new terminal:
```bash
cd frontend
npm install
npm run dev
```

Frontend runs at:
```bash
http://localhost:5173
```
---
## 📖 How to Use the Application

---

## ☁️ Deployment (Render + Vercel)

### Backend (Render)
1. Create a new **Web Service** in Render with the repo and select the `backend` root directory.
2. Set the environment variables:
   - `MONGODB_URI` (MongoDB Atlas connection string)
   - `MONGODB_DB` (optional, defaults to `pancreas_app_db`)
3. Deploy the service.

### Frontend (Vercel)
1. Import the repo in Vercel and set the root directory to `frontend/`.
2. Set `VITE_API_URL` to your Render backend URL.
3. Deploy.
