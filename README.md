# SmartShelf - Real-Time Product Recognition

SmartShelf is a computer vision-based project designed for real-time recognition of supermarket products using a camera mounted above the cashier area. The system leverages machine learning techniques to identify products in view, providing the top two most probable matches with corresponding confidence percentages. SmartShelf can be implemented in store environments to streamline checkout processes, assist in automated billing, and enhance inventory tracking.

## Table of Contents
- [Features](#features)
- [Setup](#setup)
- [Data Preparation](#data-preparation)
- [Training](#training)
- [Live Detection](#live-detection)
- [Technologies Used](#technologies-used)
- [Future Improvements](#future-improvements)
- [License](#license)

## Features
- **Real-Time Product Detection**: Identifies products as they appear under the camera.
- **Top Predictions Display**: Shows the top two most probable products and their confidence levels on-screen.
- **Model Combination**: Utilizes a combination of neural networks (MLP) and AdaBoost for optimized accuracy in complex environments.
- **Focus Area Detection**: Only processes images within a highlighted box area to enhance performance.
- **Background Removal**: Improves accuracy by removing backgrounds from images before processing.

## Setup

### Prerequisites
- Python 3.7+
- Install the required packages:
```bash
pip install -r requirements.txt
```


## Data Preparation
Dataset: Create a folder named data and organize images into subfolders for each class/product (e.g., data/apple, data/banana, etc.).
Augmentation (Optional): Data augmentation techniques such as rotation, flipping, and color adjustments can be applied to increase model robustness.

## Training
Feature Extraction: The code uses HOG, LBP, and color histograms to create feature vectors.
Training Models:
First, train the Multi-Layer Perceptron (MLP) using sklearn.neural_network.MLPClassifier.
Use AdaBoost with the MLP predictions to improve accuracy in challenging scenarios.

## Live Detection
To start real-time detection, connect a camera and run:
```bash
python run.py
```
In live detection mode, a red box marks the area of interest in the center of the screen. Every two seconds, the frame inside this box is processed, and the top two detected products, along with their confidence scores, are displayed.

## Technologies Used
Python
OpenCV for image processing
Scikit-learn for machine learning models (MLP and AdaBoost)
Numpy for data manipulation


## Future Improvements
Fine-tuning of Neural Network Architecture: Experiment with CNNs to improve feature extraction.
Deployment Options: Implement options for deploying on edge devices or in-store servers.
Additional Augmentation Techniques: Implementing synthetic data generation for rare products.


## License
This project is licensed under the MIT License - see the LICENSE file for details.
