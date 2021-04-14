FROM tensorflow/tensorflow:2.4.0-gpu

ARG DEBIAN_FRONTEND=noninteractive

# Install apt dependencies
RUN apt-get update && apt-get install -y \
    git \
    gpg-agent \
    python3-cairocffi \
    protobuf-compiler \
    python3-pil \
    python3-lxml \
    python3-tk \
    wget \
    ffmpeg \
    libsm6 \
    libxext6 \
    python3-opencv

    
RUN python -m pip install -U pip


RUN mkdir -p /tensorflow
WORKDIR /tensorflow

COPY ./inference_graph /tensorflow/inference_graph

RUN python -m pip install tensorflowjs[wizard]

