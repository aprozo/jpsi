# ROOT 6.34 on Ubuntu 24.04 (python 3.12). Only tags that exist on Docker Hub work here:
# https://hub.docker.com/r/rootproject/root/tags  (6.34.00-ubuntu24.04, 6.36.00-ubuntu25.04, ...)
FROM rootproject/root:6.34.00-ubuntu24.04

RUN apt-get update \
 && apt-get install -y --no-install-recommends git ca-certificates python3-pip \
 && rm -rf /var/lib/apt/lists/*

# Jupyter + the packages the lecture uses. pythia8mc is a pre-built PYTHIA 8 wheel (day 2).
RUN python3 -m pip install --no-cache-dir --break-system-packages \
      jupyterlab notebook ipywidgets numpy pandas matplotlib pythia8mc
