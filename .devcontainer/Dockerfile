FROM mcr.microsoft.com/devcontainers/python:3.11

# Avoid interactive prompts during package installation
ENV DEBIAN_FRONTEND=noninteractive

# Install system dependencies for Tkinter
RUN apt-get update && apt-get install -y --no-install-recommends \
    python3-tk \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Install curriculum Python packages globally
RUN pip install --no-cache-dir \
    colorama \
    pyfiglet \
    Pillow

WORKDIR /workspaces/WiBytePythonLabDemo



