FROM mcr.microsoft.com/devcontainers/python:1-3.11-bullseye

# Prevent interactive prompts during apt installation
ENV DEBIAN_FRONTEND=noninteractive

# Install system utilities, X11 stack, and Tkinter C-bindings
RUN apt-get update && apt-get install -y \
    procps \
    psmisc \
    netcat-openbsd \
    xvfb \
    x11vnc \
    openbox \
    novnc \
    python3-tk \
    && rm -rf /var/lib/apt/lists/*

# Pre-compile Python packages into /usr/local/bin
RUN pip install --no-cache-dir \
    websockify \
    pillow \
    colorama \
    pyfiglet

WORKDIR /workspaces/WiBytePythonLabDemo



