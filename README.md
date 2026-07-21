# GWB43-groundwater-drought-DIPI

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19371351.svg)](https://doi.org/10.5281/zenodo.19371351)

Reproducible analytical workflow and figure source-data package accompanying the HESS manuscript:

**Integrating propagation and recovery dynamics into groundwater drought vulnerability assessment through exposure, pressure, and aquifer system response**

## Repository structure

- `data_input/` — monthly groundwater-level and precipitation data, together with piezometer metadata
- `data_processed/` — derived SPI and SGI series, drought events and metrics, propagation matches, and DIPI analytical outputs
- `figure_source_data/` — source-data packages for main-text figures and appendices
- `notebooks/` — stepwise Jupyter notebooks reproducing the analytical workflow
- `requirements.txt` — Python dependencies
- `LICENSE` — repository licence

## Reproducibility workflow

Recommended notebook execution order:

1. `01_preprocessing_SPI_SGI.ipynb`
2. `02_event_metrics.ipynb`
3. `03_DIPI_construction.ipynb`

### Step 1: SGI preprocessing

The first notebook calculates trailing 3-, 6-, and 12-month groundwater-level means using only complete consecutive calendar-month windows. SGI is obtained through a non-parametric normal-score transformation performed separately for each calendar month:

\[
p = \frac{rank - 0.5}{n}, \qquad SGI = \Phi^{-1}(p)
\]

Average ranks are used for ties. Aquifer-group SGI is calculated as the mean of available well-level SGI values and retained only when at least 50% of wells assigned to the group and at least two wells are available.

### Step 2: Drought events and metrics

Groundwater drought months are defined by `SGI < -1.0`. Missing calendar months terminate an event. The workflow derives event duration, severity, intensity, vulnerability, resistance, resilience, recovery time, and SGI-3 to SGI-12 propagation probability at well and aquifer-group levels.

### Step 3: DIPI construction

The main weighted DIPI variant is calculated as:

\[
DIPI_{weighted} = 0.4E + 0.3P + 0.3S
\]

where `E` is exposure, `P` is pressure, and `S` is sensitivity. An equal-weight variant is also retained for robustness comparison:

\[
DIPI_{equal} = \frac{E + P + S}{3}
\]

The mapped DIPI products used in the manuscript were calculated from the corresponding GIS rasters. Point-scale values in `DIPI_components.csv` represent raster values sampled at piezometer locations.

## Quick start

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the notebooks in the order listed above from the repository root or from the `notebooks/` directory.

## Citation

Please cite the repository using the Zenodo DOI:

**https://doi.org/10.5281/zenodo.19371351**
