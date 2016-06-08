FROM ubuntu:16.04

MAINTAINER Tyler Erickson <tylere@google.com>

RUN apt-get update && apt-get install -y \
    libssl-dev \
    libffi-dev \
    python \
    python-dev \
    python-pip \
    git \
    && apt-get clean
RUN pip install cryptography
RUN pip install nose yolk
RUN pip install 'git+git://github.com/tylere/earthengine-api.git@master#subdirectory=python'
