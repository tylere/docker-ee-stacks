FROM ubuntu:16.04

MAINTAINER Tyler Erickson <tylere@google.com>

RUN apt-get update && apt-get install -y \
    libssl-dev \
    libffi-dev \
    python3 \
    python3-dev \
    python3-pip \
    git \
    && apt-get clean
RUN pip3 install cryptography
RUN pip3 install nose yolk
RUN pip3 install 'git+git://github.com/tylere/earthengine-api.git@master#subdirectory=python'
