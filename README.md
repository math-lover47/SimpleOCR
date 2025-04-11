# OCR using PyTorch

**Author**: Serikbay Arsen  
**University**: Astana IT University  
**Specialty**: Mathematical and Computational Science  
**Date**: 11 April 2025

---

## Table of Contents

1. [Introduction](#introduction)
2. [Project Structure](#project-structure)
3. [Libraries Used](#libraries-used)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Hypotheses](#hypotheses)
7. [Conclusion](#conclusion)

---

## Introduction

**Goal**: Build a PyTorch-based OCR system to extract text from images.  
**Scope**: Focus on English text recognition using a CRNN (Convolutional Recurrent Neural Network) with CTC loss.  
**Key Challenges**: Handling variable-length text sequences and aligning image features with text labels.

---

## Project Structure

```
SimpleOCR/
├── data/
│   ├── raw/            # Raw images and labels
│   ├── processed/      # Preprocessed images and serialized data
│   └── dataset.py      # Custom Dataset class for loading data
├── models/
│   ├── __init__.py
│   └── crnn.py         # CRNN (CNN + RNN) model architecture
├── config.py           # Hyperparameters (learning rate, batch size, etc.)
├── train.py            # Training script
├── inference.py        # Script to run OCR on new images
├── utils/
│   ├── preprocess.py   # Image preprocessing utilities
│   └── metrics.py      # Accuracy, CER (Character Error Rate)
├── requirements.txt    # Dependencies
└── README.md
```

---

## Libraries Used

- **PyTorch**: Model definition, training, and inference.
- **OpenCV/PIL**: Image preprocessing (resizing, normalization).
- **Pandas**: Dataset labeling (CSV files).
- **Matplotlib**: Visualization of training metrics.

---

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/math-lover47/SimpleOCR.git
   ```

---

## Usage

1. **Training**:
   ```bash
   python train.py --batch_size 32 --epochs 10
   ```
2. **Inference**:
   ```bash
   python inference.py --image_path test_image.png
   ```

---

## Hypotheses

1. A **CRNN architecture** (CNN + LSTM) will effectively capture spatial and sequential features.
2. **CTC loss** will solve alignment issues between image patches and text labels.
3. Limited to 2 weeks, the model will achieve >80% accuracy on synthetic datasets.

---

## Conclusion

This project demonstrates a minimal OCR pipeline using PyTorch. Future work includes:

- Support for multilingual text.
- Improved preprocessing (e.g., skew correction).
- Deployment via ONNX or TorchScript.

---
