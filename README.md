# $J/\psi$ decay

[![Github Codespace](https://img.shields.io/badge/open-GH_Codespaces-blue?logo=github)](https://codespaces.new/aprozo/jpsi?quickstart=1) [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/aprozo/jpsi/HEAD)

This is an interactive lecture on $J/\psi$ decay via 2 muons channel in CMS from [OpenData](https://opendata.cern.ch/record/5203) <img src="https://github.com/user-attachments/assets/27b56157-e2bb-4dbb-bb6c-6a614397cce0" alt="cmslogo" width="50"/> 

The schematic decay picture:

<img src="https://github.com/user-attachments/assets/6bc622c3-8443-45f8-9126-fa9e1cf6ee1d" alt="go" width="200"/> 

| | Notebook | What you do |
|---|---|---|
| Day 1 | [invariantMass.ipynb](invariantMass.ipynb) | measure the $J/\psi$ peak in real CMS data: invariant mass, histograms, fitting, uncertainties |
| Day 2 | [simulation.ipynb](simulation.ipynb) | simulate $J/\psi$ mesons with PYTHIA 8, add a toy detector, compare with the data |

The CMS Open Data files ([record 5203](https://opendata.cern.ch/record/5203), [record 5208](https://opendata.cern.ch/record/5208)) are included in [data/](data/)

---
# How to start

**GitHub Codespaces (recommended).** Click the [Codespaces button](https://codespaces.new/aprozo/jpsi?quickstart=1) above. It starts a container with ROOT, Jupyter and PYTHIA pre-installed (defined in [.devcontainer/](.devcontainer/)).
The first start takes a few minutes while the container is built. Stop the codespace when you are done to save quota.

**Binder.** The [Binder button](https://mybinder.org/v2/gh/aprozo/jpsi/HEAD) builds the same environment from [environment.yml](environment.yml)

**Locally.** With [conda](https://conda-forge.org/download/):

```bash
git clone https://github.com/aprozo/jpsi
cd jpsi
conda env create -f environment.yml
conda activate jpsi
jupyter lab
```
