# SURYA
# NASA IMPACT Surya Workflow 

This repository contains HELIO's workflow for running the NASA IMPACT
Surya pipeline using Google Colab and local environments. It documents
our configuration, execution steps, and analysis methods so other
members of the lab can reproduce results or adapt the pipeline for
experimentation and simulation.

## Project Overview

Surya is a 366M-parameter foundation model for heliophysics, trained on full-resolution multi-instrument SDO observations (AIA & HMI). It learns general-purpose solar representations through spatiotemporal transformers, enabling state-of-the-art performance in solar flare forecasting, active region segmentation, solar wind prediction, and EUV spectra modeling.
Our lab uses this system to:

- Run Surya pipelines in Google Colab
- Configure datasets and processing parameters
- Test experimental workflows
- Document reproducible analysis environments

This repository provides the exact configuration and notebooks used in
so others can replicate the setup.

##Repository Structure 

