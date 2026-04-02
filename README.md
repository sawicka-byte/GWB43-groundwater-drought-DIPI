# Integrating propagation and recovery dynamics into groundwater drought vulnerability assessment: linking exposure, pressure, and system response

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19371351.svg)](https://doi.org/10.5281/zenodo.19371351)

This repository contains the input datasets, processed outputs, reproducible Jupyter notebooks, and figure source data used in the manuscript.

---

## Repository structure

- `data_input/` – input datasets used for reproducible analyses (monthly groundwater levels, precipitation series, spatial predictors, metadata, and cluster assignments)
- `data_processed/` – SGI, SPI, drought-event metrics, DIPI components, and final outputs
- `figure_source_data/` – source CSV files for all main-text and appendix figures
- `notebooks/` – stepwise Jupyter notebooks for preprocessing, drought metrics, and DIPI construction
- `notebooks_reproducible/` – master end-to-end reproducibility notebook
- `requirements.txt` – Python dependencies

---

## Reproducibility workflow

Recommended notebook execution order:

1. `01_preprocessing_SPI_SGI.ipynb`
2. `02_event_metrics.ipynb`
3. `03_DIPI_construction.ipynb`
4. `04_figures_main_text.ipynb`

Alternatively, the complete workflow can be reproduced using the master notebook in `notebooks_reproducible/`.

---

## Quick start

Install dependencies:

```bash
pip install -r requirements.txt
```

Then run the notebooks in the order listed above, or execute the master notebook in `notebooks_reproducible/`.

---

## Software environment

The analyses were developed in **Python 3.11** using Jupyter notebooks.

Main packages:
- pandas 2.2
- numpy 1.26
- scipy 1.13
- matplotlib 3.8
- geopandas 0.14
- rasterio 1.3
- scikit-learn 1.4

All dependencies are fully listed in `requirements.txt`.

---

## Figure source mapping

- **Fig. 1** → `figure_source_data/fig1_study_area/`
- **Fig. 2** → `figure_source_data/fig2_spi_sgi/`
- **Fig. 3** → `figure_source_data/fig3_metrics/`
- **Fig. 4** → `figure_source_data/fig4_dipi_maps/`
- **Appendix A** → `figure_source_data/appendix_A/`
- **Appendix B** → `figure_source_data/appendix_B/`

---

## Data policy

Raw institutional monitoring data from **PIG-PIB / Polish Hydrogeological Survey** are subject to access restrictions and therefore cannot be redistributed.

To ensure reproducibility, this repository provides the processed monthly datasets and all derived analytical products used directly in the study.

---

## Citation

This repository is archived on Zenodo under DOI: **10.5281/zenodo.19371351**
