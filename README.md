# SURYA Heliophysics Workflows

Google Colab notebooks used by Project HELIO at the SRGE Lab to install, verify, and experiment with NASA IMPACT's [Surya](https://github.com/NASA-IMPACT/Surya) heliophysics foundation model.

Surya is a spatiotemporal model trained on Solar Dynamics Observatory observations. The upstream project supports downstream workflows such as solar-flare prediction, solar-wind forecasting, active-region segmentation, and EUV spectra prediction. This repository records the lab's reproducible Colab setup and exploratory task runs; it does not vendor the Surya model or datasets.

## Start here

Google Colab with a GPU runtime is the intended environment.

1. Open `notebooks/Surya_BaseModel.ipynb` in Colab.
2. Connect Google Drive when prompted so checkpoints and outputs survive runtime resets.
3. Add any Hugging Face or data-service credentials through Colab Secrets; never place tokens directly in a notebook cell.
4. Run cells in order and confirm the upstream Surya verification test passes.
5. Continue with a task notebook after the base environment is working.

After a Colab runtime disconnect, follow the notebook's restart notes instead of reinstalling every cached dependency.

## Notebooks

| Notebook | Purpose |
| --- | --- |
| `Surya_BaseModel.ipynb` | Install and verify the base Surya model; configure Drive persistence |
| `Surya_SolarFlare_Prediction.ipynb` | Explore the solar-flare task, expected files, example inference, and a custom time-range pipeline |
| `SURYA_WorkingTest1.ipynb` | Working setup for solar wind, solar flare, active-region segmentation, and EUV spectra tasks |

The large notebooks may render slowly on GitHub. Download them or open them in Colab for reliable execution.

## NOAA verification materials

`kylie-noaa-task_verified.zip` contains a small archived workflow for comparing selected flare events against NOAA records. Extract it locally before use:

```bash
unzip kylie-noaa-task_verified.zip -d noaa-task
```

Read the documentation inside the extracted directory before running its scripts. The archive is separate from the main Surya notebooks.

## External access

- Upstream code: [NASA-IMPACT/Surya](https://github.com/NASA-IMPACT/Surya)
- Models and datasets: [nasa-ibm-ai4science on Hugging Face](https://huggingface.co/nasa-ibm-ai4science)
- SDO/JSOC email registration: [JSOC registration](http://jsoc.stanford.edu/ajax/register_email.html)

Model access and solar-data queries may require separate accounts or terms of use. ERAU users should use the current university guidance for Colab entitlements rather than relying on a README guarantee about subscription availability.

## Reproducibility checklist

For each result, record:

- the upstream Surya Git commit and model checkpoint;
- notebook name and revision;
- Python, CUDA, and key dependency versions;
- input time range, instruments/channels, and preprocessing;
- random seed and downstream-task configuration; and
- output metrics and artifact locations.

## Scope

These notebooks are experimental research workflows. Verify upstream licenses, model cards, dataset terms, and scientific assumptions before redistributing artifacts or using predictions operationally.

## Maintainer

[Space Robotics and Generative Estimation (SRGE) Lab](https://github.com/srge-erau), Embry-Riddle Aeronautical University.
