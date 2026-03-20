<div align="center">

# 🐱 AI AdverseCat: Adversarial Attacks with TensorFlow
### 🛡️ Exploring Deep Learning Vulnerabilities & Robustness

![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

</div>

## 📌 Project Overview
**AI AdverseCat** is a hands-on Deep Learning research project designed to demonstrate **Adversarial Attacks** on pre-trained image classification models. Even the most accurate neural networks can be tricked by adding meticulously calculated, human-imperceptible noise to an input image. 

This notebook leverages **TensorFlow and Keras** to dissect how image classifiers (trained on ImageNet) make decisions, applying adversarial techniques (like Fast Gradient Sign Method - FGSM) to manipulate their predictions—forcing the model to confidently misclassify a dog as a cat or another target class.

## ✨ Key Features
- **Vulnerability Demonstration**: Proves that traditional Convolutional Neural Networks (CNNs) without adversarial training are highly vulnerable to crafted input perturbations.
- **Gradient-Based Attacks**: Utilizes backpropagation to calculate gradients *with respect to the input image*, rather than the model weights, to generate noise maps.
- **ImageNet Integration**: Uses robust, real-world data mappings (`imagenet_classes.json`) to simulate attacks on large-scale classification tasks.
- **Visual Interpretability**: Includes `matplotlib` visualizations comparing the original image, the extracted noise layer, and the final adversarial image.

## 🛠️ Technology Stack
* **Framework**: `TensorFlow` & `Keras`
* **Data Manipulation**: `NumPy`
* **Image Processing**: `Pillow (PIL)`
* **Visualization**: `Matplotlib`
* **Environment**: `Jupyter Notebook`

## 🚀 Getting Started

### Prerequisites
Make sure you have Python 3.8+ installed along with the required scientific libraries:
```bash
pip install tensorflow numpy matplotlib pillow jupyter
```

### Running the Notebook
1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/CHUH00/AI_AdverseCat.git
   cd AI_AdverseCat
   ```
2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Open `AdversarialCat_TF.ipynb` and execute the cells sequentially to observe the adversarial attack in real-time.

## 🧪 How It Works
1. **Target Identification**: A base image (`dog-from-unsplash.jpg`) is fed into the classification model to secure its baseline prediction.
2. **Gradient Calculation**: We compute the gradient of the loss function corresponding to a *target* wrong class, tracing it back to the input pixels.
3. **Perturbation Injection**: The image is modified slightly in the direction of the gradient, deceiving the network while looking completely unchanged to the human eye.

---
*Created by [Woojin Choi](https://github.com/CHUH00) as part of my continuous exploration into Artificial Intelligence, Deep Learning, and Computer Vision.*
