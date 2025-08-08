# Ayna ML Assignment: Colored Polygon Generator

## 📌 Problem Statement
Given grayscale polygon outlines and a color label, generate a filled RGB image of the polygon with the correct color using a U-Net-based model.

## 🗂 Dataset Structure
```
dataset/
├── training/
│   ├── inputs/            # Grayscale polygon outlines (L mode)
│   ├── outputs/           # Target colored polygons (RGB)
│   └── data.json          # Maps input to color name and output
├── validation/
│   ├── inputs/
│   ├── outputs/
│   └── data.json
```

## 🧠 Model Overview
- U-Net with 3-level encoder-decoder structure
- Input: 1-channel grayscale image + 3-channel color vector broadcasted
- Output: RGB polygon with specified color
- Loss Function: MSELoss
- Optimizer: Adam

## 📊 Results (10 Epochs)
- Final Train Loss ≈ 0.0979
- Final Validation Loss ≈ 0.0657
- Inference predictions match expected shapes and colors (see `inference.ipynb`)

## 🧪 How to Run Inference
Use the `inference.ipynb` file to:
1. Load the saved model
2. Visualize predictions on validation samples

## 🔗 Weights & Biases (wandb)
Tracking: [Your wandb project link]

