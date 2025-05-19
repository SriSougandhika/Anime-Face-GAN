# Anime Face Generation using GANs 🎨✨
This project is a Generative Adversarial Network (GAN) implemented using TensorFlow to generate anime-style faces. It is trained on the Anime Face Dataset (NTUMLDS).

## 🧠 Overview
The goal is to train a GAN model that can learn to generate anime faces from noise vectors. The training is done using a simple DCGAN architecture with TensorFlow and Keras. The dataset contains thousands of 64x64 anime faces.

## 🗂️ Dataset

- **Source:** [Kaggle - Anime Face Dataset (NTUMLDS)](https://www.kaggle.com/datasets/stanley13579/anime-face-dataset-ntumlds)
- **Path Format:** `/kaggle/input/anime-face-dataset-ntumlds/images/*.jpg`
- **Resolution:** 64x64 pixels
- **Preprocessing:** Normalized pixel values to [-1, 1]

## ⚙️ Model Architecture

### Generator
- Dense + Reshape
- Conv2DTranspose layers with BatchNorm and LeakyReLU
- Output: 64x64x3 image with Tanh activation

### Discriminator
- Conv2D layers with LeakyReLU and Dropout
- Output: Single sigmoid neuron (Real/Fake)

## 🚀 Training Details

- **Epochs:** 150
- **Loss Function:** Binary Cross-Entropy
- **Optimizer:** Adam (β1=0.5)
- **Batch Size:** 128
- **Framework:** TensorFlow / Keras
- **Hardware:** GPU (Kaggle)

## 📈 Results
Generated samples improve steadily over epochs, starting as gray noise and gradually forming colorful anime faces.

## 🖼️ Sample Outputs
- Sample output images after few epochs are attached in the images. 
- Although it requires some fine-tuning, the images seem a little realistic despite them being a little blur and distorted.

## 📦 Requirements
See [`requirements.txt`](requirements.txt)

## 🙌 Credits
Project by Sri – an aspiring Data Scientist exploring AI in creative ways!
