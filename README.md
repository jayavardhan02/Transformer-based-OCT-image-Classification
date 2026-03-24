# Transformer-Based OCT Image Classification

This project implements a lightweight **MobileViT-XS** model to classify retinal **OCT (Optical Coherence Tomography)** images into four categories:

* CNV (Choroidal Neovascularization)
* DME (Diabetic Macular Edema)
* DRUSEN
* NORMAL

The model is trained on a **10% stratified subset of the OCT2017 dataset** and achieves high accuracy while remaining efficient enough for **CPU inference and lightweight deployment**.

---

## Reference Paper

This project follows the architecture described in the research work **“MobileViT: Light-weight, General-purpose, and Mobile-friendly Vision Transformer”** by Sachin Mehta and Mohammad Rastegari.

Key ideas used from the paper:

* Combination of **CNNs for local feature extraction** and **Transformers for global feature learning**
* **Patch-based global attention mechanism**
* **Lightweight architecture** suitable for mobile and edge devices

---

## Project Structure

oct_mobilevit_app/

mobilevit_model.py — MobileViT-XS architecture implementation
mobilevit_xs_best.pth — Trained model weights
infer.py — Script for single image prediction
app.py — Streamlit web application
requirements.txt — Project dependencies
README.md — Project documentation

---

## Installation

### 1. Clone the Repository

git clone Transformer-based-OCT-images-classification
cd Transformer-based-OCT-images-classification

---

### 2. Create and Activate Virtual Environment

**Windows**

python -m venv .venv
.venv\Scripts\activate

**macOS / Linux**

python3 -m venv .venv
source .venv/bin/activate

---

### 3. Install Dependencies

pip install -r requirements.txt

---

## Run Inference on a Single Image

Place an OCT image (JPG or PNG) inside the project folder and run:

python infer.py

Example output:

Prediction: CNV (96.12% confidence)

---

## Run the Streamlit Web Application

To start the web interface run:

streamlit run app.py

A local browser interface will open where you can upload an OCT image and receive the predicted class using the trained **MobileViT-XS model**.

---

## Model Performance (10% OCT2017 Subset)

Accuracy: 0.9407
Precision: 0.9090
Recall: 0.9281
F1 Score: 0.9179

---

## Dataset

This project uses the **OCT2017 Retina Dataset** which contains retinal OCT images belonging to four categories:

* CNV
* DME
* DRUSEN
* NORMAL

A **10% stratified subset** of the dataset was used to reduce computational requirements while maintaining class balance.

---

## Disclaimer

This project is intended only for **research and educational purposes**.
It is **not designed for clinical diagnosis or medical decision making**.

---

## Acknowledgements

* Authors of the MobileViT architecture
* OCT2017 dataset creators
* PyTorch community
* Streamlit community
