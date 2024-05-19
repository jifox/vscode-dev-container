FROM mcr.microsoft.com/devcontainers/base:jammy

# Avoid warnings by switching to noninteractive
ENV DEBIAN_FRONTEND=noninteractive

# Configure apt and install packages
RUN apt update \
    && apt upgrade -y \
    && apt install -y software-properties-common \
    && add-apt-repository ppa:deadsnakes/ppa -y \
    && apt update \
    && apt install --no-install-recommends -y \
       git mime-support libxml2 libxmlsec1-dev libxmlsec1-openssl libmariadb3 openssl \
       python3.9 python3.9-venv python3.9-dev python3.9-distutils python3.9-tk \
       python3-pip python3-venv python3-dev python3-distutils python3-tk \
       python3.11 python3.11-venv python3.11-dev python3.11-distutils \
       python3.12 python3.12-venv python3.12-dev python3.12-distutils python3.12-tk \
       pipx \
    && apt autoremove -y \
    && apt clean -y

RUN update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.9 1 \
    && update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.11 2 \
    && update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.12 3
