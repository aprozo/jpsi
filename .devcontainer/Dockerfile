# ROOT 6.34 on Ubuntu 24.04 (python 3.12). Only tags that exist on Docker Hub work here:
# https://hub.docker.com/r/rootproject/root/tags  (6.34.00-ubuntu24.04, 6.36.00-ubuntu25.04, ...)
#
# This image is built and tested by .github/workflows/build-image.yml and published to
# ghcr.io/aprozo/jpsi, which devcontainer.json uses. Codespaces never builds it itself.
FROM rootproject/root:6.34.00-ubuntu24.04

# numpy/pandas/matplotlib come from Ubuntu: the base image already has Ubuntu's numpy 1.26 (used by ROOT),
# and installing pandas/matplotlib with pip would pull numpy 2 and fail trying to replace it.
RUN apt-get update \
 && apt-get install -y --no-install-recommends git ca-certificates python3-pip \
      python3-numpy python3-pandas python3-matplotlib \
 && rm -rf /var/lib/apt/lists/*

# Jupyter via pip (not in Ubuntu) and pythia8mc, a pre-built PYTHIA 8 wheel (part 2). Versions are pinned.
COPY requirements.txt /tmp/requirements.txt
RUN python3 -m pip install --no-cache-dir --break-system-packages -r /tmp/requirements.txt \
 && rm /tmp/requirements.txt
