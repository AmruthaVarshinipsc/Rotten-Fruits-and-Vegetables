# 🍎 Rotten Fruits & Vegetables Recognition System

## 📌 Project Overview

The Rotten Fruits and Vegetables Recognition System is a Machine Learning-based web application developed using TensorFlow and Streamlit.  

This system automatically classifies fruits and vegetables as **Fresh** or **Rotten** using a Convolutional Neural Network (CNN).

The main objective of this project is to reduce food wastage, minimize manual inspection errors, and demonstrate the practical implementation of deep learning concepts including dataset preprocessing, model training, evaluation, and deployment.

---

## 🚀 Features

- Image upload functionality
- CNN-based prediction
- Real-time classification
- Confidence percentage display
- Light and Dark theme options
- Interactive Streamlit dashboard
- User-friendly interface

---

## 🧠 Technologies Used

- Python 3.13
- Streamlit
- TensorFlow (CPU)
- NumPy
- Pillow (PIL)
- Keras ImageDataGenerator

---

## 🏗️ Model Architecture

The Convolutional Neural Network (CNN) includes:

- Conv2D Layer (32 filters, 3x3 kernel, ReLU activation)
- MaxPooling2D Layer
- Flatten Layer
- Dense Layer (128 neurons, ReLU activation)
- Output Layer (Softmax activation)

### Image Preprocessing:
- Resize images to 64x64 pixels
- Normalize pixel values (0–1 scaling)

The trained model is saved as:

trained_model/trained_model.h5

---

## 📂 Project Structure

ROTTEN FRUITS AND VEGETABLES  
│  
├── project files  
│   ├── code  
│   │   ├── projectprocess.py  
│   │   ├── run file.py  
│   │  
│   ├── trained_model  
│   │   └── trained_model.h5  
│   │  
│   ├── labels  
│   │   └── labels.txt  
│   │  
│   ├── images  
│   │   └── dataset folders  
│   │  
│   └── background img  
│  
└── .git  

---

# ⚙️ How to Run the Project (VS Code Method)

### 1️⃣ Go to Project Root (IMPORTANT: not inside code folder)

cd "C:\Users\LENOVO\OneDrive\Desktop\Rotten-Fruits-and-Vegetables-main\ROTTEN FRUITS AND VEGETABLES"

---

### 2️⃣ Create and Activate Python 3.13 Virtual Environment

py -3.13 -m venv C:\v\rfv313  
C:\v\rfv313\Scripts\activate  

---

### 3️⃣ Install Required Packages

python -m pip install -U pip setuptools wheel  
pip install streamlit tensorflow-cpu pillow numpy  

---

### 4️⃣ Update Dataset Path in Training Script (If Required)

$proj = "C:\Users\LENOVO\OneDrive\Desktop\Rotten-Fruits-and-Vegetables-main\ROTTEN FRUITS AND VEGETABLES"  
$img = "$proj\images"  
(Get-Content "$proj\code\projectprocess.py") -replace "^dataset_dir\s*=.*$", "dataset_dir =  r'$img'" | Set-Content "$proj\code\projectprocess.py"  

---

### 5️⃣ Train the Model

python ".\code\projectprocess.py"

This will generate:

trained_model/trained_model.h5

---

### 6️⃣ Run the Application

streamlit run ".\code\run file.py"

---

## 🌐 Access the Application

After running, Streamlit will automatically open:

http://localhost:8501

Upload an image and click **Predict** to view whether the item is:

- Fresh  
- Rotten  

Along with prediction confidence percentage.

---

## 🧪 Testing

Model testing includes:

- Training accuracy monitoring
- Validation accuracy monitoring
- Loss evaluation

Functional testing includes:

- Image upload verification
- Prediction validation
- Error handling for invalid inputs

---

## ⚠️ Known Limitations

- Detects only visible external spoilage
- Cannot detect internal defects
- Performance may vary with lighting conditions
- Limited dataset size may affect generalization

---

## 🔮 Future Enhancements

- Multi-class classification (fruit type detection)
- Real-time webcam detection
- Cloud deployment
- Mobile application integration
- Transfer learning with advanced CNN architectures
- Database integration for storing prediction history

---

## 📊 Dataset

The dataset contains categorized images of fruits and vegetables labeled as Fresh or Rotten.  
Images are organized into training and validation directories by class.

---


