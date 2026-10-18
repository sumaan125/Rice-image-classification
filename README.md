# 🌾 Rice Variety Classification
A deep learning web application that classifies images of individual rice grains into five distinct varieties. Powered by a custom Convolutional Neural Network (CNN), this model achieves a highly reliable **99% accuracy**.

## 📌 Supported Rice Varieties
The model is trained to recognize the following five classes:
*   **Arborio**
*   **Basmati**
*   **Ipsala**
*   **Jasmine**
*   **Karacadag**

## 📊 Dataset
The model was trained on the **[Murat Koklu Rice Image Dataset](https://www.kaggle.com/datasets/muratkokludataset/rice-image-dataset)**. It contains tens of thousands of individual rice grain images categorized into the five classes mentioned above. The large dataset enables the CNN to accurately learn the distinct shape, texture, and size features of each variety.

## 🧠 Model Training Process
The model was trained using TensorFlow and Keras, following a structured data pipeline detailed in `model_training.ipynb`:

*   **Data Preparation:** The Murat Koklu Rice Image Dataset was extracted from an archive.
*   **Data Splitting:** The `splitfolders` library was used to cleanly divide the dataset folders into training, validation, and testing sets.
*   **Preprocessing & Augmentation:** TensorFlow's `ImageDataGenerator` was utilized to load the images efficiently in batches. During processing, the images were resized to 160x160 pixels and normalized (pixel values scaled between 0 and 1 by dividing by 255.0).
*   **Architecture:** A Convolutional Neural Network (CNN) was trained to recognize the distinct textures and shapes of the grains. 
*   **Export:** The highly accurate trained model was saved as `Rice_image_classification_cnn_model.h5` for deployment.

## 💻 Tech Stack
*   **Deep Learning:** TensorFlow & Keras
*   **Frontend/Deployment:** Streamlit
*   **Data Processing:** NumPy, Pillow (PIL), Split-folders

## 🚀 Live Demo
You can try the model without installing anything by visiting the deployed Streamlit application:

[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://rice-image-classification-efpsawblvhhhxu5entsjq8.streamlit.app/)

