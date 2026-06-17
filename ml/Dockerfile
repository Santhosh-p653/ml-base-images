FROM ghcr.io/santhosh-p653/dl:latest

RUN pip install --no-cache-dir \
    transformers \
    datasets \
    accelerate \
    sentence-transformers \
    numpy \
    Pillow \
    opencv-python-headless \
    face-detection

LABEL org.opencontainers.image.title="ML Image"
LABEL org.opencontainers.image.description="Machine Learning and Transformer development environment"
LABEL org.opencontainers.image.source="https://github.com/Santhosh-p653/ml-base-images"
