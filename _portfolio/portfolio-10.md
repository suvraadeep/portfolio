---
title: "Amazon ML Challenge-High computing Approach [TrOCR]"
excerpt: "This project implements an OCR  pipeline using TrOCR (Transformer OCR), a state-of-the-art model for recognizing text in images. The workflow includes dataset preparation, model fine-tuning, and evaluation using Hugging Face's transformers library. The pipeline is optimized for low-resolution images and supports augmentation techniques to enhance training. It achieves high accuracy in extracting structured information from images, such as weights, volumes, and other product details."
collection: portfolio
---

🔗 **Notebook Link:** [Amazon ML Challenge-High computing Approach [TrOCR]](https://www.kaggle.com/code/suvroo/trocr-amazon-ml-approach-1-high-computing)  


## Tech Stack
- **TrOCR**: Vision-to-Language Transformer model for OCR.
- **Hugging Face Transformers**: For loading and fine-tuning the TrOCR model.
- **PyTorch**: For deep learning computations.
- **Pandas**: For data manipulation.
- **Matplotlib**: For visualizing results.
- **Evaluate**: For computing evaluation metrics like CER (Character Error Rate).

## Features
1. **Data Preparation**:
   - Extracts image paths and metadata from CSV files.
   - Filters missing or invalid data entries.
   - Supports augmentations like `ColorJitter` and `GaussianBlur`.

2. **Custom Dataset Class**:
   - Loads images and applies augmentations.
   - Prepares pixel values and tokenized labels for training.

3. **Model Fine-Tuning**:
   - Fine-tunes the `TrOCR-Small-Handwritten` model on custom datasets.
   - Uses AdamW optimizer with FP16 training for efficiency.

4. **Evaluation Metrics**:
   - Computes CER (Character Error Rate) to evaluate model performance.

5. **Visualization**:
   - Displays sample images with predicted text during evaluation.


## Workflow

### 1. Data Preparation
- Extracts image paths and metadata from a CSV file.
- Applies augmentations to improve model robustness.
- Splits data into training and validation sets.

### 2. Model Training
- Fine-tunes the TrOCR model using Hugging Face's `Seq2SeqTrainer`.
- Training configurations:
  - Batch Size: 10
  - Epochs: 10
  - Learning Rate: 0.00005
  - Evaluation Strategy: Per Epoch

### 3. Evaluation
- Evaluates the trained model on unseen test data.
- Computes CER to measure text recognition accuracy.

### 4. Inference
- Performs OCR on new images using the fine-tuned TrOCR model.
- Visualizes the results with extracted text.










