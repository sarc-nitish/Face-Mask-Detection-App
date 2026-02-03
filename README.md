# 😷 Face Mask Detection using Deep Learning (CNN)

A **Deep Learning–based Face Mask Detection system** built with **TensorFlow, Keras, and Streamlit**.
This project can **detect whether a person is wearing a face mask or not** from an image and also provides a **live web application** for easy usage.

🚀 **Live App:** [https://face-mask-detection-nitish.streamlit.app/](https://face-mask-detection-nitish.streamlit.app)

---

## 🌐 Live Demo (Streamlit App)

The project includes a fully functional **Streamlit web application** where users can:

*  Upload an image (Drag & Drop supported)
*  Get instant prediction (Mask / No Mask)
*  View confidence score

**App Features:**

* Clean & responsive UI
* Fast predictions
* Uses trained CNN model (`.h5`)

---

## 📁 Project Structure

```
Face-Mask-Detection/
│
├── Mask_face_analyser.ipynb   # Model training & evaluation notebook
├── app.py                     # Streamlit web app
├── mask_img_analyzer.h5       # Trained CNN model (Git LFS)
├── requirements.txt           # Project dependencies
├── README.md                  # Project documentation
└── .gitattributes             # Git LFS configuration
```

---

##  Model Overview

The model is a **custom Convolutional Neural Network (CNN)** trained from scratch.

### Architecture Highlights:

* Convolution + ReLU layers
* MaxPooling layers
* Fully Connected (Dense) layers
* Dropout for regularization
* Softmax output (2 classes)

**Input Shape:** `128 × 128 × 3`
**Classes:** `Mask`, `No Mask`

---

## 🗂️ Dataset Structure

```
face_data/
│
├── with_mask/        → Label: 1
│   ├── img1.jpg
│   └── ...
│
└── without_mask/     → Label: 0
    ├── img1.jpg
    └── ...
```

---

##  Training Details

* Image Size: `128 × 128`
* Normalization: `[0, 1]`
* Train/Test Split: `80% / 20%`
* Validation Split: `10%`
* Optimizer: `Adam`
* Loss: `Sparse Categorical Crossentropy`
* Epochs: `5`

Training and validation **accuracy & loss graphs** are visualized in the notebook.

---

##  Prediction Logic

The Streamlit app uses the following pipeline:

1. Image uploaded by user
2. Resize to `128×128`
3. Normalize pixel values
4. CNN model predicts probabilities
5. Highest probability class selected

### Output Example:

```
Prediction: Mask
Confidence: 92.45%
```

---

##  How to Run Locally

###  Clone the repository

```bash
git clone https://github.com/sarc-nitish/Face-Mask-Detection.git
cd Face-Mask-Detection
```

###  Install dependencies

```bash
pip install -r requirements.txt
```

###  Run Streamlit App

```bash
streamlit run app.py
```

---

##  Tech Stack

* Python
* TensorFlow / Keras
* OpenCV
* NumPy
* Pillow (PIL)
* Streamlit
* Jupyter Notebook

---

##  Future Improvements

*  Real-time webcam detection
*  Transfer Learning (MobileNetV2 / EfficientNet)
*  Mobile-friendly UI
*  Cloud deployment (AWS / GCP)

---

##  Author

**Nitish (sarc-nitish)**
Machine Learning & Computer Vision Enthusiast

---

⭐ If you found this project useful, don’t forget to **star the repository** on GitHub!
