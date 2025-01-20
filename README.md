# GPU-Enabled Development Environment Demo

As a data scientist or ML engineer, you've likely faced the challenge of limited local GPU resources, complex environment setup, or the "works on my machine" problem when collaborating. This repository provides a pre-configured development environment that gives you:

- Instant access to GPU computing power without hardware investment
- A consistent, reproducible environment that works the same for everyone
- Pay-as-you-go pricing (e.g. only pay when you're actively using the environment)
- Persistent storage for your datasets and model checkpoints
- The ability to pause/resume your work from anywhere

**Using Gitpod with AWS, you can start training models on GPU hardware in minutes instead of spending hours on setup and configuration. Perfect for experimentation, model training, or when you need extra compute power for specific tasks.**

## What's Included

- `devcontainer.json` - Decalarative and repeatable environment setup including:
  - NVIDIA CUDA support via features
  - GPU requirements and access configuration
  - VS Code Python and Jupyter extensions
  - Python interpreter and formatting settings
  - Automatic requirements.txt installation
  - Kernel specification for Jupyter notebooks
- `Dockerfile` - Base container configuration using Ubuntu with CUDA toolkit and Python packages, including: 
  - Python 3.10 with virtual environment
  - IPython kernel for Jupyter notebooks
  - Ollama for LLM inference
- `requirements.txt` - All Python dependencies installed including (but not limited to):
  - NumPy (>=1.24.0)
  - Pandas (>=2.0.0)
  - Matplotlib (>=3.7.0)
  - Seaborn (>=0.12.0)
  - scikit-learn (>=1.3.0)
  - Jupyter (>=1.0.0)
  - IPython Kernel (>=6.0.0)
  - Plotly (>=5.0.0)
  - Plotly Express (>=0.4.0)
  - nbformat (>=5.0.0)
- `.gitpod/automations.yaml` - Gitpod automation examples 
  - Starting the ollama server
  - Seeing GPU stats of the environment
  - Running Ollama LLM

## Quick Start

1. Fork this repository
2. Set up Gitpod with AWS
3. Click the button below to start your environment:

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://app.gitpod.io/#https://github.com/gitpod-samples/gpu-demo)

## Environment Specifications

- Base Instance: g5.xlarge (NVIDIA A10G GPU)
- Storage: 150 GiB persistent storage
- Pre-installed:
  - CUDA Toolkit
  - Python 3.x
  - Common ML libraries (PyTorch, TensorFlow)
  - Ollama for local inference

## Try It Out

Once your environment is running, here are some things you can try:

1. Run local inference with ollama:
```bash
ollama run phi3:medium
```

2. See nvidia GPU performance and stats:
```bash
watch -n 1 nvidia-smi 
```

3. Run a Jupyter notebook:
```bash
jupyter notebook
```

4. Execute a Python script:
```bash
python my_script.py
```
