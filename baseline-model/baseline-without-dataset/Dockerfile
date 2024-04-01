FROM pytorch/pytorch:2.2.1-cuda12.1-cudnn8-devel

LABEL maintainer="SeongjunPark<sj.park@donga.ac.kr>"

RUN apt-get update && \
    apt-get install -y python3.11 && \
    apt-get install -y python3.11-distutils

RUN apt-get install -y python3.11-dev && \
    apt-get install -y wget && \
    wget https://bootstrap.pypa.io/get-pip.py && \
    python3.11 get-pip.py && \
    rm get-pip.py

RUN apt-get install -y git

RUN echo "alias python=python3.11" >> ~/.bashrc && \
    echo "alias pip=pip3.11" >> ~/.bashrc

RUN /bin/bash -c "source ~/.bashrc"

WORKDIR /workspace

RUN git clone https://github.com/Labbeti/dcase2024-task6-baseline

RUN pip3.11 install -e dcase2024-task6-baseline/.