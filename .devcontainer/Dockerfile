FROM mcr.microsoft.com/devcontainers/base:jammy

# Avoid warnings by switching to noninteractive
ENV DEBIAN_FRONTEND=noninteractive

# Configure apt and install packages
RUN sudo apt update \
    && sudo apt upgrade -y \
    && sudo apt install -y software-properties-common \
    && sudo add-apt-repository ppa:deadsnakes/ppa -y \ 
    && sudo apt update \
    && sudo apt install -y python3.9 python3.9-venv python3.9-dev python3.9-distutils python3.9-tk \
    && sudo apt install -y python3-pip python3-venv python3-dev python3-distutils python3-tk \
    && sudo apt install -y python3.11 python3.11-venv python3.11-dev python3.11-distutils \
    && sudo apt install -y python3.12 python3.12-venv python3.12-dev python3.12-distutils python3.12-tk \
    && sudo apt autoremove -y \
    && sudo apt clean -y
