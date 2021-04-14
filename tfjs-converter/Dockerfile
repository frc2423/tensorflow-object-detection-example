FROM "ubuntu:bionic"

# Install apt dependencies
RUN apt-get update && apt-get install -y \
    git \
    python-pip
    
RUN pip install --upgrade pip

RUN mkdir -p /tensorflow
WORKDIR /tensorflow

COPY ./inference_graph /tensorflow/inference_graph

RUN pip install tensorflowjs[wizard]

