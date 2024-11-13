# SmartShelf - Real-Time Product Recognition

SmartShelf is a computer vision-based project designed for real-time recognition of supermarket products using a camera mounted above the cashier area. The system leverages machine learning techniques to identify products in view, providing the top two most probable matches with corresponding confidence percentages. SmartShelf can be implemented in store environments to streamline checkout processes, assist in automated billing, and enhance inventory tracking.

## Table of Contents
- [Features](#features)
- [Setup](#setup)
- [Data Preparation](#data-preparation)
- [Training](#training)
- [Live Detection](#live-detection)
- [Project Structure](#project-structure)
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
