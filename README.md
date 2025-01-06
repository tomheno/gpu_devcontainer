# GPU-Enabled Development Environment Demo

As a data scientist or ML engineer, you've likely faced the challenge of limited local GPU resources, complex environment setup, or the "works on my machine" problem when collaborating. This repository provides a pre-configured development environment that gives you:

- Instant access to GPU computing power without hardware investment
- A consistent, reproducible environment that works the same for everyone
- Pay-as-you-go pricing (e.g. only pay when you're actively using the environment)
- Persistent storage for your datasets and model checkpoints
- The ability to pause/resume your work from anywhere

**Using Gitpod with AWS, you can start training models on GPU hardware in minutes instead of spending hours on setup and configuration. Perfect for experimentation, model training, or when you need extra compute power for specific tasks.**

## What's Included

- `.devcontainer/` - Complete GPU-enabled development environment configuration
  - `devcontainer.json` - Environment setup with NVIDIA CUDA support
  - `Dockerfile` - Base container configuration using Ubuntu

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

## Verify Your Setup

Once your environment is running:

```bash
watch -n 1 nvidia-smi 
```

## Customization

- Modify `.devcontainer/devcontainer.json` to change GPU requirements
- Update `.devcontainer/Dockerfile` to add custom packages
- Adjust environment class in Gitpod settings for different GPU types

## Estimated Costs

- g5.xlarge: ~$1/hour
- Storage: $0.10/GB/month

**Note:** Refer to AWS documentation for precise costs. 

## Learn More

- [Gitpod Documentation](https://www.gitpod.io/docs)
- [Dev Container Specification](https://containers.dev)