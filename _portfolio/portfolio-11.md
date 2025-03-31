---
title: "Amazon ML Challenge- Optimal Approach [BERT+PaddleOCR]"
excerpt: "This project implements an OCR-based entity extraction pipeline to process product images, extract text, and map it to structured data fields. It leverages PaddleOCR for text recognition and BERT for fine-tuned entity mapping. The pipeline handles large-scale datasets, performs preprocessing, and applies machine learning techniques for accurate predictions of entity values such as weight, dimensions, and voltage."
collection: portfolio
---

🔗 **Notebook Link:** [Amazon ML Challenge- Optimal Approach [BERT+PaddleOCR]](https://www.kaggle.com/code/suvroo/bert-paddleocr-amazon-ml-final-approach)  

## Overview
This project combines **OCR (Optical Character Recognition)** with **machine learning models** to extract structured information from product images. Using **PaddleOCR**, the pipeline extracts text from images, which is then processed using a fine-tuned **BERT model** to predict entity values like weight, height, and voltage. The system is designed to handle large datasets efficiently while ensuring accuracy in text recognition and entity mapping.


## Tech Stack
- **PaddleOCR**: For fast and accurate text extraction from images.
- **BERT (Bidirectional Encoder Representations from Transformers)**: For fine-tuned entity mapping.
- **Hugging Face Transformers**: For model training and inference.
- **PyTorch**: For deep learning computations.
- **Tesseract & EasyOCR**: Initial OCR tools tested before switching to PaddleOCR.
- **FuzzyWuzzy**: For correcting unit spellings in extracted data.
- **Pandas & NumPy**: For data manipulation and preprocessing.


## Features
1. **Text Extraction (OCR)**:
   - Extracts text from product images using PaddleOCR.
   - Preprocessing steps include contrast enhancement, noise removal, and thresholding.

2. **Entity Mapping with BERT**:
   - Fine-tunes a BERT model to map extracted text to structured fields like `item_weight`, `voltage`, etc.
   - Handles noisy data with custom preprocessing.

3. **Data Cleaning**:
   - Applies regex-based cleaning for extracted text.
   - Corrects unit spellings using FuzzyWuzzy for consistency.

4. **Model Training**:
   - Fine-tunes BERT for sequence-to-sequence tasks using Hugging Face's `BartForConditionalGeneration`.
   - Evaluates performance using BLEU scores and exact match accuracy.

5. **Large-Scale Processing**:
   - Handles datasets with over 90K images efficiently.
   - Optimized for GPU acceleration using PaddleOCR and PyTorch.

---

## Workflow

### 1. Data Preparation
- Extracts image paths and metadata from CSV files.
- Preprocesses images to enhance OCR performance (e.g., grayscale conversion, CLAHE).

### 2. Text Extraction
- Uses PaddleOCR for fast text extraction from images.
- Stores extracted text in a structured format (CSV).

### 3. Entity Mapping
- Fine-tunes a BERT model to map extracted text to target fields (e.g., `item_weight` → "180 gram").
- Handles noisy outputs with regex cleaning and unit correction.

### 4. Evaluation
- Evaluates predictions using BLEU scores and exact match accuracy.
- Example Metrics:
  - Exact Match Accuracy: 39.64%
  - Average BLEU Score: 0.1249

### 5. Postprocessing
- Corrects unit spellings using FuzzyWuzzy.
- Filters out invalid or missing predictions.


## Results
```markdown
| Metric                  | Value          |
|-------------------------|----------------|
| Exact Match Accuracy    | 39.64%         |
| Average BLEU Score      | 0.1249         |
| Processing Time (90K Images) | ~7 minutes (PaddleOCR) |
```

## Improvements & Future Work
1. Train on a larger dataset with more epochs for better accuracy.
2. Explore advanced OCR models like TrOCR for improved text recognition.
3. Use GANs or Fourier Transform methods to enhance image quality before OCR.
4. Implement additional preprocessing pipelines for noisy or low-resolution images.










