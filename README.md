# Image Upscaler & Restorer using GFPGAN

This project utilizes the GFPGAN (Generative Facial Prior-Generative Adversarial Network) and Real-ESRGAN models to upscale and restore images, improving the quality of low-resolution images with a focus on human faces.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Dependencies](#dependencies)
- [Configuration](#configuration)
- [Troubleshooting](#troubleshooting)

## Introduction

The application enhances low-resolution images using advanced machine learning models, primarily focusing on enhancing facial features in images but also capable of general image upscaling. It integrates models like SRVGGNetCompact for image super-resolution and GFPGANer for facial enhancements.

## Installation

To set up this project, you will need Python installed on your system. You can then install the required dependencies.

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
    ```

2. Install the required Python libraries: `pip install -r requirements.txt`.

3. Download the necessary model files by running the script or manually downloading them into your project directory:

- `realesr-general-x4v3.pth`
- `GFPGANv1.2.pth`
- `GFPGANv1.3.pth`
- `GFPGANv1.4.pth`
- `RestoreFormer.pth`

## Usage

To run the application: `python app.py`. 

This will launch a Gradio interface where you can upload an image, select the enhancement version, and specify the rescaling factor to enhance the image.

## Features

- <b>Image Upscaling</b>: Upscales images using Real-ESRGAN.
- <b>Facial Enhancement</b>: Enhances facial features in images using GFPGAN models.
- <b>Flexible Scaling</b>: Allows specifying the scaling factor for upscaling the image.
- <b>Interactive UI</b>: Provides an easy-to-use Gradio interface to interact with the models.

## Dependencies

- Python 3.8+
- torch
- torchvision
- opencv-python
- gradio
- realesrgan
- gfpgan
- basicsr

## Configuration

Configuration involves setting up the models and their paths correctly, as well as ensuring all dependencies are installed. The script auto-downloads models if they're not present in the directory.

## Troubleshooting

Common issues:

- <b>Memory errors due to GPU limits</b>: Try running the script with a smaller tile size or on a system with more GPU resources.
- <b>Model files not found</b>: Ensure all model files are downloaded as per the installation instructions.
