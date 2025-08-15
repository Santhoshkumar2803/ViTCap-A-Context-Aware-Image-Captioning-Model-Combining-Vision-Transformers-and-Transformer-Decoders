# ViTCap: Vision Transformer for Image Captioning

This repository contains a PyTorch implementation of an image captioning model that uses a Vision Transformer (ViT) as an encoder and a Transformer-based decoder.

## Overview

The model is designed to generate context-aware, human-like descriptions for images. It leverages a pre-trained Vision Transformer to extract rich visual features, which are then fed into a Transformer decoder to generate the text caption word by word.

## Architecture
* **Encoder**: A pre-trained Vision Transformer (`vit_b_16`) that converts an image into a high-level feature vector.
* **Decoder**: A standard Transformer decoder that takes the image features and generates a text sequence.

## How to Use

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/ViTCap.git](https://github.com/your-username/ViTCap.git)
    cd ViTCap
    ```
2.  **Create a virtual environment and install dependencies:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    pip install -r requirements.txt
    ```
3.  **Prepare your data:**
    * Place your images in a `data/image_data/` folder.
    * Create a `data/captions.txt` file where each line is `image_name.jpg<TAB>caption text`.
4.  **Run the training script:**
    ```bash
    python src/train.py
    ```