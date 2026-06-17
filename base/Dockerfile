FROM python:3.11-slim

RUN apt-get update && apt-get install -y \
    git \
    curl \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

RUN pip install --no-cache-dir --upgrade pip

LABEL org.opencontainers.image.title="Base AI Image"
LABEL org.opencontainers.image.description="Reusable Python base image for AI and ML workloads"
LABEL org.opencontainers.image.source="https://github.com/Santhosh-p653/ml-base-images"
