# 🚁 Autonomous Drone Landing Zone Detection using Computer Vision

A Deep Learning-based Computer Vision system that analyzes aerial images and predicts whether a location is safe for drone landing.

The model classifies aerial imagery into:

- 🛬 Runway (Safe Landing Zone)
- ⚽ Football Field (Safe Landing Zone)
- 🏙️ Urban/City Area (Unsafe Landing Zone)

The project is designed to support autonomous drone operations by assisting in real-time landing zone assessment using image classification.

---

## 📌 Project Overview

Autonomous drones often require rapid identification of safe landing zones during emergencies, surveillance missions, logistics operations, and defense applications.

This project uses a Convolutional Neural Network (CNN) trained on approximately **6,000 aerial images** to classify landing zones and provide a landing recommendation with confidence scores.

---

## 🎯 Objectives

- Detect safe and unsafe landing zones from aerial imagery.
- Differentiate between runways, football fields, and urban regions.
- Provide confidence scores for predictions.
- Enable real-time image upload and inference through a web application.
- Support future integration with autonomous drone navigation systems.

---

# 🏗️ Project Architecture

```text
Aerial Image
      │
      ▼
Image Preprocessing
(Resize + Normalize)
      │
      ▼
CNN Model
(TensorFlow/Keras)
      │
      ▼
Class Prediction
      │
      ▼
Landing Decision Engine
      │
      ▼
Safe / Unsafe Recommendation
```

---

# 📂 Dataset

### Classes

| Class | Description |
|---------|------------|
| Runway | Safe landing zone |
| Football Field | Safe landing zone |
| City | Unsafe landing zone |

### Dataset Statistics

- Total Images: ~6,000
- Classes: 3
- Image Size: 128 × 128
- Format: JPG / PNG

### Dataset Structure

```text
dataset/
│
├── runway/
│   ├── img1.jpg
│   ├── img2.jpg
│
├── football/
│   ├── img1.jpg
│   ├── img2.jpg
│
└── city/
    ├── img1.jpg
    ├── img2.jpg
```

---

# 🧠 Model Architecture

The model uses a Convolutional Neural Network (CNN) built with TensorFlow/Keras.

### Layers

```text
Input Layer
      │
Conv2D + ReLU
      │
MaxPooling
      │
Conv2D + ReLU
      │
MaxPooling
      │
Conv2D + ReLU
      │
MaxPooling
      │
Flatten
      │
Dense Layer
      │
Dropout
      │
Output Layer (Softmax)
```

---

# ⚙️ Tech Stack

## Programming Language

- Python

## Deep Learning

- TensorFlow
- Keras

## Computer Vision

- OpenCV

## Data Processing

- NumPy
- Pandas

## Visualization

- Matplotlib
- Seaborn

## Deployment

- Streamlit

---

# 📊 Model Performance

### Final Accuracy

✅ **96% Accuracy**

### Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

### Visualization

- Training Accuracy Graph
- Validation Accuracy Graph
- Loss Curve
- Confusion Matrix Heatmap

---

# 🚀 Features

### Safe Landing Detection

Predicts whether a drone can safely land at the selected location.

### Confidence Score

Provides confidence percentages for each class.

Example:

```text
Runway            : 95.42%
Football Field    : 3.11%
City              : 1.47%

Decision:
SAFE TO LAND
```

---

# 🖥️ Streamlit Web Application

Users can upload aerial images and receive instant predictions.

### Workflow

```text
Upload Image
      │
      ▼
Preprocessing
      │
      ▼
CNN Prediction
      │
      ▼
Confidence Scores
      │
      ▼
Landing Recommendation
```

---

# 📸 Example Predictions

| Image Type | Prediction |
|------------|------------|
| Runway | Safe to Land |
| Football Field | Safe to Land |
| City | Unsafe to Land |

---

# 📁 Repository Structure

```text
Autonomous-Drone-Landing-Detection/
│
├── dataset/
│
├── model/
│   └── drone_landing_model.h5
│
├── notebooks/
│   └── training.ipynb
│
├── app.py
│
├── requirements.txt
│
├── README.md
│
└── assets/
```

---

# ▶️ Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/Autonomous-Drone-Landing-Detection.git
```

Move into the project folder:

```bash
cd Autonomous-Drone-Landing-Detection
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# ▶️ Run the Application

Start Streamlit:

```bash
streamlit run app.py
```

Open:

```text
http://localhost:8501
```

---

# 📈 Future Improvements

- Object Detection for obstacle-aware landing.
- Terrain slope estimation.
- Reinforcement Learning-based landing optimization.
- Real-time drone camera integration.
- Multi-class terrain classification.
- Defense and disaster-response deployment.

---

# 🎖️ Applications

### Defense

- Autonomous reconnaissance drones
- Emergency landing assistance
- Battlefield logistics

### Civil

- Delivery drones
- Disaster management
- Search and rescue missions
- Agricultural monitoring

---

# 👨‍💻 Authors

**Abhinav Srivastava**

DRDO Summer Internship Project

---

# ⭐ Acknowledgements

Special thanks to:

- DRDO
- TensorFlow Community
- OpenCV Community
- Streamlit
- Open Source Dataset Contributors

---

## 📜 License

This project is developed for educational, research, and internship purposes.

Feel free to fork, improve, and contribute to the project.

---

### ⭐ If you found this project useful, consider giving the repository a star!
