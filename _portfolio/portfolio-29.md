---
title: "Paper to .ipynb"
excerpt: "A full-stack AI application that converts research paper PDFs into executable Jupyter notebooks using LLM-powered code generation, multi-provider support, and real-time pipeline streaming."
collection: portfolio
---

🔗 **GitHub Repo:** [Paper to .ipynb](https://github.com/suvraadeep/Paper-to-.ipynb.git)  


### Key Features:
1. **LLM-Powered Notebook Generation**: Converts research papers into fully executable notebooks with explanations and code.
2. **Multi-Provider Support**: Works with Gemini, Claude, Groq, and OpenAI models.
3. **4-Step Intelligent Pipeline**: Analyze → Design → Generate → Validate workflow for structured output.
4. **Real-Time Streaming (SSE)**: Live progress + AI reasoning visualization during notebook generation.
5. **Customizable Generation**: Supports multiple frameworks (PyTorch, TensorFlow, JAX) and difficulty levels. :contentReference[oaicite:0]{index=0}  


### Example Workflow:
#### Input: *Upload a research paper PDF*
1. **Analysis**:
   - Extracts architecture, algorithms, and key insights.
2. **Design Phase**:
   - Plans implementation (CPU/GPU modes).
3. **Generation**:
   - Produces structured notebook with code + explanations.
4. **Validation**:
   - Fixes errors and ensures executable output.

#### Input: *Paste arXiv link*
1. **Auto Processing**:
   - Converts link → PDF → parsed content.
2. **Notebook Output**:
   - Fully reproducible implementation with markdown explanations.




### Technologies Used:
- **FastAPI & Python**: Backend API and pipeline orchestration.
- **Next.js & React (TypeScript)**: Frontend UI and interaction.
- **LLM APIs (Gemini, Claude, OpenAI, Groq)**: Code and notebook generation.
- **pdfplumber & httpx**: PDF processing and extraction.
- **nbformat**: Programmatic notebook creation.
- **Tailwind CSS & Framer Motion**: UI styling and animations.
