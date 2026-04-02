---
title: "Prompted Segmentation for Drywall QA"
excerpt: "This project implements a prompt-based image segmentation system using CLIPSeg to detect drywall seams and wall cracks. It combines multi-dataset training, synthetic data generation, and efficient fine-tuning to achieve robust segmentation with minimal labeled data."
collection: portfolio
---

🔗 **Notebook Link:** [Prompted Segmentation for Drywall QA](https://www.kaggle.com/code/suvroo/prompted-segmentation-for-drywall-qa)  


### Key Features:
1. **Prompt-Based Segmentation**: Uses CLIPSeg to segment regions (e.g., cracks, seams) via natural language prompts.
2. **Multi-Dataset Training**: Combines drywall and crack datasets with automatic fallback to synthetic data generation.
3. **Efficient Fine-Tuning**: Freezes CLIP encoder and trains only lightweight decoder (~1M params) for low-data regime.
4. **Robust Pipeline**: Includes data augmentation, TTA (flip), and bbox-to-mask conversion for weak supervision.
5. **Performance Optimized**: Achieves ~0.65 mIoU with fast inference (~95 ms/image).

### Example Workflow:
#### Query: *"segment crack"*
1. **Prompt Encoding**: Converts text prompt into CLIP text embeddings.
2. **Image Processing**: Processes input image via CLIP vision encoder.
3. **Segmentation Output**:
   - Generates binary mask highlighting crack regions.

#### Query: *"segment drywall seam"*
1. **Prompt Encoding**: Uses seam-specific prompts.
2. **Inference + TTA**:
   - Applies horizontal flip augmentation for robustness.
3. **Output**:
   - Produces segmentation mask for drywall taping areas.

### Technologies Used:
- **CLIPSeg (Transformers)**: Prompt-based image segmentation.
- **PyTorch**: Model training and optimization.
- **Albumentations & OpenCV**: Data augmentation and preprocessing.
- **Roboflow + Synthetic Data**: Dataset handling and fallback generation.
- **NumPy & Matplotlib**: Evaluation and visualization.
