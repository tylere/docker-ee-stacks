FROM debian@sha256:32a225e412babcd54c0ea777846183c61003d125278882873fb2bc97f9057c51

MAINTAINER Tyler Erickson <tylere@google.com>

# Earth Engine dependencies
RUN apt-get update && apt-get install -y \
    libssl-dev \
    libffi-dev \
    python3 \
    python3-dev \
    python3-pip \
    git \
    && apt-get clean

RUN pip3 install cryptography
RUN pip3 install nose
RUN pip3 install yolk3k

RUN pip3 install -U pip  # install a more recent version of pip that understands subdirectories
RUN pip install 'git+git://github.com/tylere/earthengine-api.git@master#subdirectory=python'
