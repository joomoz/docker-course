FROM ubuntu:16.04

ENV LC_ALL=C.UTF-8 
WORKDIR /yle-dl

RUN apt-get update && apt-get install -y \
    wget ffmpeg python3 python3-pip && \
    pip3 install pycryptodome && \
    pip3 install yle-dl && \
    rm -rf /var/lib/apt/lists/*

ENTRYPOINT ["yle-dl"]