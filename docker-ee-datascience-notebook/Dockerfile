FROM jupyter/datascience-notebook@sha256:eca7b98d0a26a026aedf1ded6b505e334855e2e8d80b13b28747795cddb928a9

MAINTAINER Tyler Erickson <tylere@google.com>

USER root

# Install Earth Engine non-Python dependencies
RUN apt-get update && apt-get install -y \
    libssl-dev \
    libffi-dev \
    git \
    && apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Add Conda-Forge as a recognized conda channel
RUN conda config --add channels conda-forge 

# Install crytography (an Earth Engine dependency)
RUN pip2 install cryptography
RUN pip3 install cryptography

# Install the Earth Engine Python API
RUN pip2 install earthengine-api==0.1.101
RUN pip3 install earthengine-api==0.1.101

# Install the GDAL
RUN conda install --quiet --yes -n python2 gdal
RUN conda install --quiet --yes gdal

# Install TensorFlow
RUN conda install --quiet --yes -n python2 tensorflow
RUN conda install --quiet --yes tensorflow

# Switch back to jovyan to avoid accidental container runs as root
USER jovyan