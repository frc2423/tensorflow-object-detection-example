FROM ubuntu:bionic

RUN mkdir -p /tensorflow
WORKDIR /tensorflow

COPY ./inference_graph /tensorflow/inference_graph

RUN pip install tensorflowjs[wizard]

