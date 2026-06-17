FROM ghcr.io/santhosh-p653/base:latest

RUN pip install --no-cache-dir \
    torch==2.4.0+cpu \
    torchvision==0.19.0+cpu \
    torchaudio==2.4.0+cpu \
    --index-url https://download.pytorch.org/whl/cpu

LABEL org.opencontainers.image.title="Deep Learning Image"
LABEL org.opencontainers.image.description="PyTorch CPU environment"
LABEL org.opencontainers.image.source="https://github.com/Santhosh-p653/ml-base-images"
