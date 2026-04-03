# HESS_JCWPd43_reproducibility_notebook

## Purpose
This master notebook provides the primary end-to-end reproducibility entry point for the HESS manuscript.

It reproduces the complete analytical workflow from processed monthly input datasets to final DIPI outputs, cluster summaries, and figure source tables.

---

## Full workflow
1. Load processed monthly groundwater-level datasets
2. Load monthly precipitation datasets
3. Compute SPI and SGI time series
4. Detect drought events based on SGI thresholds
5. Compute drought-event metrics (severity, duration, recovery, vulnerability, propagation)
6. Construct exposure, pressure, and sensitivity layers
7. Calculate final DIPI values
8. Export figure source tables for all main-text and appendix figures
9. Export cluster summary statistics

---

## Notebook chain
Run the detailed notebooks in the following order:

1. `../notebooks/01_preprocessing_SPI_SGI.ipynb`
2. `../notebooks/02_event_metrics.ipynb`
3. `../notebooks/03_DIPI_construction.ipynb`
4. `../notebooks/04_figures_main_text.ipynb`

Alternatively, this notebook serves as the main reproducibility overview for the complete workflow.

---

## Required files
- `../data_input/`
- `../data_processed/`
- `../figure_source_data/`

---

## Expected outputs
- SGI/SPI tables
- drought metrics tables
- DIPI components
- figure source CSV files
- cluster summary statistics

---

## HESS submission note
This notebook is intended as the primary reproducibility entry point accompanying the HESS manuscript submission.

The executable end-to-end notebook version will replace this placeholder before final manuscript acceptance.
