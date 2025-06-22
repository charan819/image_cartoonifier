# Image Cartoonifier

A Flask-based web application that applies artistic style transfer to images, transforming them into cartoon-like versions using TensorFlow and a pre-trained VGG19 model.

---

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup & Installation](#setup--installation)
- [Usage](#usage)
- [How It Works](#how-it-works)


## Overview

This project implements an image cartoonifier that stylizes a content image based on one or multiple style images using neural style transfer techniques. The application is built with Flask for the web interface and TensorFlow for the style transfer model.

Users can upload their own content images and style images or select from default styles provided. The output is a stylized image saved and served by the Flask backend.

---

## Features

- Upload content image (photo to be cartoonified).
- Upload multiple style images or choose from predefined styles.
- Real-time style transfer with neural network.
- Output stylized image download via Flask.
- Simple and user-friendly web interface.

---

## Technologies Used

- Python 3.x
- Flask
- TensorFlow (Keras)
- VGG19 pre-trained model (ImageNet weights)
- NumPy
- Pillow (PIL)
- Matplotlib (for debugging/visualization)
- Werkzeug (for secure file handling)
- Flask-JSGlue (for URL handling in templates)

---

## Setup & Installation

1. **Clone the repository:**
   ```bash
    git clone <repo-url>
    cd image_cartoonifier
2. Create and activate a virtual environment:
   ``` bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # macOS/Linux
   source venv/bin/activate
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
4. Run the Flask app:
   ```bash
   python UiHandler.py
5. Open your browser and navigate to http://localhost:8000

## USAGE

- Open the homepage.
- Upload a content image (your photo).
- Upload one or more style images or choose from default styles.
- Submit to generate the cartoonified image.
- The output image will be processed and available for download/viewing.

## HOW IT WORKS

How It Works
- StyleContentModel.py:
   - Defines a TensorFlow model based on VGG19 that extracts style and content feature representations. It calculates gram matrices for style layers to capture style features.

- ImageCartoonifier.py:
   - Implements the Cartoonifier class that loads images, computes losses based on style and content, and optimizes the input image to generate a stylized output using gradient descent.

- UiHandler.py:
   - Flask app that serves the frontend, handles file uploads, saves images, triggers the cartoonification process, and serves the output image.








