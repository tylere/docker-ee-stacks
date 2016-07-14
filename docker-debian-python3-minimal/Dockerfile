FROM debian@sha256:32a225e412babcd54c0ea777846183c61003d125278882873fb2bc97f9057c51

MAINTAINER Tyler Erickson <tylere@google.com>

# Install Earth Engine non-Python dependencies
RUN apt-get update && apt-get install -y \
    libssl-dev \
    libffi-dev \
    python3 \
    python3-dev \
    python3-pip \
    git \
    && apt-get clean

# Install Earth Engine Python dependencies
RUN pip3 install cryptography

# Install the Earth Engine Python API
RUN pip3 install earthengine-api  
