---
title: "SmolLlama - Compact Language Model Training Pipeline"
excerpt: "SmolLlama is a 130M-parameter language model built from scratch using PyTorch, trained through a 3-stage process: pretraining on FineWeb, instruction tuning (SFT), and human preference alignment (DPO). Designed for efficiency, it achieves a validation loss of 4.01 after 3 epochs while requiring only 5GB VRAM in FP32 precision."
collection: portfolio
---

🔗 **Repo Link:** [SmolLlama - Compact Language Model Training Pipeline (Repo Private)](https://github.com/suvraadeep/Smol-llama.git)  



## Overview  
This project implements a streamlined pipeline for training compact LLMs (130M params) capable of human-like text generation. The framework supports distributed training across multiple GPUs and includes tools for model evaluation and deployment.  

## Key Features  
- **Three-Stage Training**:  
  1. **Pretraining**: Base model on 15M texts from FineWeb (10BT snapshot)  
  2. **SFT**: Instruction tuning for task-specific performance  
  3. **DPO**: Direct Preference Optimization for alignment  

- **Hardware Efficiency**:  
  - Runs on 4×RTX 4090 (24GB VRAM each)  
  - 5GB VRAM usage in FP32 mode  

- **Technical Specifications**:  
  ```markdown  
  | Parameter           | Value  | Description                          |  
  |---------------------|--------|--------------------------------------|  
  | Architecture         | Llama  | Decoder-only transformer             |  
  | Hidden Dim           | 768    | Embedding dimensions                 |  
  | Attention Heads      | 6      | Multi-head attention                 |  
  | Decoder Layers       | 6      | Depth of transformer stack           |  
  | Context Window       | 128    | Token limit per sequence             |  
  | Batch Size           | 64     | Global across 4 GPUs                 |  
  ```

## Installation  
1. **Clone Repository**:  
   ```bash  
   git clone https://github.com/suvraadeep/Smol-llama.git  
   cd SmolLlama  
   bash ./install.sh  
   ```

2. **Weights & Biases Setup**:  
   ```bash  
   pip install wandb  
   wandb login  
   ```

3. **Download Pretrained Weights**:  
   ```bash  
   python download_model_weight.py  
   ```

## Training Workflow  
### 1. Pretraining Configuration  
```bash  
torchrun --standalone --nproc_per_node=4 llama.py \  
    --epochs 3 \  
    --block_size 128 \  
    --batch_size 64 \  
    --max_lr 2e-4  
```

### 2. Key Hyperparameters  
- **Optimizer**: AdamW (`β1=0.9`, `β2=0.95`)  
- **Learning Rate**: Cosine annealing with warm restarts  
- **Regularization**: 0.1 weight decay  

### 3. Performance Metrics  
- **Training Loss**: 3.96  
- **Validation Loss**: 4.01  
- **Throughput**: 45k iterations/epoch (4×4090s)  

![Loss Curves](https://example.com/lrence  
```python  
from smolllama import SmolLlama  

model = SmolLlama.from_pretrained("smolllama-130M")  
output = model.generate(  
    prompt="It was a difficult time for me",  
    max_length=100,  
    temperature=0.8,  
    repetition_penalty=1.5  
)  
```

**Example Output**:  
```  
"It was a difficult time for me, but through consistent effort and support from my colleagues,  
I developed resilience and eventually overcame the challenges in my work life."  
```

## Custom Training  
Adjust core parameters via CLI:  
```bash  
torchrun --standalone --nproc_per_node=gpu llama.py \  
    --embeddings_dims 1024 \  
    --no_of_heads 8 \  
    --max_lr 3e-4 \  
    --prompt "Once upon a time"  
```

## References  
1. FineWeb Dataset: [Hugging Face](https://huggingface.co/datasets/fineweb)  
2. DPO Implementation: [arXiv:2305.18290](https://arxiv.org/abs/2305.18290)  










