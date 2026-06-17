
# ML Base Images

Reusable Docker images for AI, Machine Learning, and Deep Learning workflows, automatically built and published to GitHub Container Registry (GHCR).

## Overview

This repository provides a layered container architecture for AI development. Instead of repeatedly installing dependencies for every project, developers can pull prebuilt images from GHCR and build on top of them.

The goal is to provide reusable, production-ready foundations for Machine Learning, Deep Learning, NLP, Computer Vision, and future AI workloads.

## Architecture

base
 │
 ▼
dl
 │
 ▼
ml

## Base Image

Provides common system dependencies required by most Python projects.

### Includes:

- Python 3.11
- Git
- Curl
- Build Essentials
- Updated Pip

---

## Deep Learning Image

Built on top of the Base Image.

### Includes:

- PyTorch
- TorchVision
- TorchAudio

---

## Machine Learning Image

Built on top of the Deep Learning Image.

### Includes:

- Transformers
- Datasets
- Accelerate
- Sentence Transformers
- NumPy
- Pillow
- OpenCV
- Face Detection

---

## Repository Structure

.
├── .github
│   └── workflows
│       └── build.yml
├── base
│   └── Dockerfile
├── dl
│   └── Dockerfile
├── ml
│   └── Dockerfile
└── README.md

## CI/CD Pipeline

GitHub Actions automatically builds and publishes images to GitHub Container Registry whenever changes are pushed to the main branch.

### Workflow:

build-base
     ↓
 build-dl
     ↓
 build-ml

## Published Packages:

ghcr.io/santhosh-p653/base
ghcr.io/santhosh-p653/dl
ghcr.io/santhosh-p653/ml

## Pull Images

Base

docker pull ghcr.io/santhosh-p653/base:latest

Deep Learning

docker pull ghcr.io/santhosh-p653/dl:latest

Machine Learning

docker pull ghcr.io/santhosh-p653/ml:latest

Usage Examples

Using the DL Image

FROM ghcr.io/santhosh-p653/dl:latest

COPY . .

CMD ["python", "train.py"]

Using the ML Image

FROM ghcr.io/santhosh-p653/ml:latest

COPY . .

CMD ["python", "app.py"]

## Why This Repository?

Many AI projects spend significant time recreating environments and reinstalling common dependencies.

This project aims to:

- Reduce setup time
- Promote reusable AI infrastructure
- Standardize development environments
- Enable rapid prototyping
- Demonstrate containerized AI workflows
- Showcase CI/CD with GitHub Actions and GHCR

## Roadmap

### Planned future images:

- Gradio
- Streamlit
- Computer Vision
- NLP
- Agent Frameworks
- RAG Tooling
- MLOps Utilities

### Proposed architecture:

base
├── dl
│   ├── vision
│   └── nlp
├── gradio
├── streamlit
├── agent
└── rag

## Technologies Used

- Docker
- GitHub Actions
- GitHub Container Registry (GHCR)
- Python 3.11
- PyTorch
- Transformers

## License

This project is licensed under the MIT License.
