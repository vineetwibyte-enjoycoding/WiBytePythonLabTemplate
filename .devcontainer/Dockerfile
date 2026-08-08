FROM python:3.11-slim

# Prevent interactive prompts during apt installation
ENV DEBIAN_FRONTEND=noninteractive

# Install essential CLI tools and Tkinter GUI support
RUN apt-get update && apt-get install -y --no-install-recommends \
    git \
    curl \
    ca-certificates \
    openssh-client \
    python3-tk \
    && rm -rf /var/lib/apt/lists/*

# Pre-install Python libraries directly into the global site-packages
RUN pip install --no-cache-dir colorama pyfiglet

WORKDIR /workspaces/WiBytePythonLabDemo
