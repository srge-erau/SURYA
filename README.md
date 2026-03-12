# SURYA 

# NASA IMPACT Surya Workflow  

This repository contains HELIO's workflow for running the NASA IMPACT 

Surya pipeline using Google Co Lab and local environments. It documents 

our configuration, execution steps, and analysis methods so other 

members of the lab can reproduce results or adapt the pipeline for 

experimentation and simulation. 

  

NASA Impact Surya Github: https://github.com/NASA-IMPACT/Surya 

Hugging Face Repository: https://huggingface.co/nasa-ibm-ai4science 

  

## Project Overview 

Surya is a 366M-parameter foundation model for heliophysics, trained on full-resolution multi-instrument SDO observations (AIA & HMI). It learns general-purpose solar representations through spatiotemporal transformers, enabling state-of-the-art performance in solar flare forecasting, active region segmentation, solar wind prediction, and EUV spectra modeling. 

Our lab uses this system to: 

  

- Run Surya pipelines in Google Co Lab 

- Configure datasets and processing parameters 

- Test experimental workflows 

- Document reproducible analysis environments 

  

This repository provides the exact configuration and notebooks used in 

so others can replicate the setup. 


## Notebook Structure 

Each of the working Google Co Lab notebooks contain the Surya base model and its specific tasks are stored in the notebooks folder and are available for download for use in your google Co Lab account. 

- Surya_BaseModel.ipynb : This notebook contains the code for running and verifying the Surya base model. It also mounts data to save to your google drive. 

- Surya_SolarFlare_Prediction.ipynb: This Notebook houses the solar flare prediction task. Sections include mounting to google drive for output saving, the tutorial code for setting up the task for an example inference run, file formats, and an attempted run for a custom prediction inference run. 

- SURYA_WorkingTest1.ipynb: This notebook contains the base model and each of the four tasks (Solar Wind Prediction, Solar Flare Prediction, Active Region Segmentation, and EUV Spectra Analysis) tutorial set up steps loaded and working. Each task displays its trained example prediction from a predefined time range.

Inside the Notebook structure there are other files relating to Project HELIO's work with Surya:
- NOAA_Task_Verified: 

  
## Important Information 

  
- ERAU offers a free subscription to Google Co Lab Pro which is essential for more GPU/RAM capabilities and extended runtime sessions. 

- The email registered for your free Google Co Lab Pro account will also grant access to your google drive, which is necessary for saving output data, and Surya files. 

- It is recommended to register this same email with JSOC servers so you may access their SDO Data servers using this link: http://jsoc.stanford.edu/ajax/register_email.html 

- It is recommended that this email be used for your hugging face account, as Surya using Hugging Face Repositories for sorting datasets and more base model information. 


