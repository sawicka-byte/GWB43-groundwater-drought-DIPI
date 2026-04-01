[![DOI](https://zenodo.org/badge/1198549464.svg)](https://doi.org/10.5281/zenodo.19371351)

This repository contains the processed datasets, reproducible Python notebooks, and figure source data used for the manuscript:

**Integrating propagation and recovery dynamics into groundwater drought vulnerability assessment: linking exposure, pressure, and system response**

## Repository structure

- `data_input/` – processed monthly groundwater levels, precipitation series, metadata, and cluster assignments
- `data_processed/` – SGI, SPI, drought-event metrics, DIPI components, and final outputs
- `figure_source_data/` – source CSV files for all main-text and appendix figures
- `code/` – stepwise Python notebooks for preprocessing, drought metrics, and DIPI construction
- `notebooks_reproducible/` – master end-to-end reproducibility notebook
- `requirements.txt` – Python dependencies

## Reproducibility workflow

Recommended notebook execution order:

1. `01_preprocessing_SPI_SGI.ipynb`
2. `02_event_metrics.ipynb`
3. `03_DIPI_construction.ipynb`
4. `04_figures_main_text.ipynb`

## Data policy

Raw institutional monitoring data from PIG-PIB may be subject to restrictions.

To ensure reproducibility, this repository provides processed monthly datasets used directly in the analyses.

## Citation

A DOI snapshot of this repository will be archived via Zenodo upon manuscript submission.
