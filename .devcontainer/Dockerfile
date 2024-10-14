# Use an official Python runtime as a parent image
FROM python:3.12-slim

# Set the working directory in the container
WORKDIR /workspace

# Install system dependencies
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

# Install Jupyter and Python dependencies
RUN pip install --no-cache-dir \
    jupyter \
    pandas \
    numpy

# Expose port for Jupyter notebook
#EXPOSE 8888

# Run Jupyter notebook
#CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--no-browser", "--allow-root"]
