---
title: "Fooling a neural network"
excerpt: "This project demonstrates the concept of adversarial attacks on neural networks using GoogLeNet. By introducing small, imperceptible perturbations to input images, the model's predictions are intentionally altered, showcasing vulnerabilities in deep learning models. The pipeline includes loading pretrained models, performing adversarial attacks, and visualizing the impact of perturbations on predictions."
collection: portfolio
---

🔗 **Notebook Link:** [Fooling a neural network](https://www.kaggle.com/code/suvroo/fooling-the-neural-network-adverserial-attack)  


## Overview
This Jupyter Notebook explores **adversarial attacks** on neural networks, highlighting how small input modifications can lead to incorrect classifications. Using **GoogLeNet**, the project demonstrates:
- Standard image classification.
- Generating adversarial examples through gradient-based perturbations.
- Visualizing the effect of adversarial noise on model predictions.


## Tech Stack
- **PyTorch**: For loading and evaluating the pretrained GoogLeNet model.
- **GoogLeNet**: Pretrained on ImageNet for image classification.
- **Matplotlib**: For visualizing images and gradients.
- **FuzzyWuzzy**: For text similarity in adversarial text examples (optional).
- **Pandas & NumPy**: For data manipulation.


## Features
1. **Standard Image Classification**:
   - Uses GoogLeNet to classify images with confidence scores.
   - Displays top 5 predictions with probabilities.

2. **Adversarial Example Generation**:
   - Computes gradients for each pixel to create adversarial noise.
   - Modifies input images to mislead the model into incorrect classifications.

3. **Visualization**:
   - Displays original and modified images side-by-side.
   - Highlights gradient maps showing perturbations applied to input images.

4. **Adversarial Text Examples (Optional)**:
   - Demonstrates adversarial attacks on text by altering characters or semantics.


## Applications & Future Work

1. **Applications**:
   - Understanding vulnerabilities in neural networks.
   - Enhancing robustness against adversarial attacks in critical systems like self-driving cars or fraud detection.

2. **Future Work**:
   - Extend adversarial attacks to other modalities like text or audio.
   - Experiment with different attack methods (e.g., FGSM or PGD).










