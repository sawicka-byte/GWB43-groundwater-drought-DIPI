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

---

## Software environment

The analyses were developed in **Python 3.11** using Jupyter notebooks.

Main packages:
- pandas
- numpy
- scipy
- matplotlib
- geopandas
- rasterio
- scikit-learn

All dependencies are listed in `requirements.txt`.

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

Some institutional monitoring data from **PIG-PIB / Polish Hydrogeological Survey** may be subject to access restrictions.

To ensure reproducibility, this repository provides the processed monthly datasets and derived analytical products used directly in the study.

---

## Citation

This repository is archived on Zenodo under DOI: **10.5281/zenodo.19371351**
