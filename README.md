# GWB43-groundwater-drought-DIPI

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19371351.svg)](https://doi.org/10.5281/zenodo.19371351)

Reproducible analytical workflow and figure source-data package accompanying the HESS manuscript:

**Integrating propagation and recovery dynamics into groundwater drought vulnerability assessment through exposure, pressure, and aquifer system response**

---

## Repository structure

- `data_input/` – processed monthly input datasets used in reproducible analyses (groundwater levels, precipitation, metadata)
- `data_processed/` – derived SPI, SGI, drought-event metrics, and DIPI analytical outputs
- `figure_source_data/` – source-data packages for all main-text figures and appendices
- `notebooks/` – stepwise Jupyter notebooks and the master reproducibility workflow
- `requirements.txt` – Python dependencies

---

## Reproducibility workflow

Recommended notebook execution order:

1. `01_preprocessing_SPI_SGI.ipynb`
2. `02_event_metrics.ipynb`
3. `03_DIPI_construction.ipynb`
4. `run_full_reproducibility_workflow.ipynb`

The final notebook serves as the master entry point summarizing the full analytical chain and expected outputs.

---

## Quick start

Install dependencies:

```bash
pip install -r requirements.txt
