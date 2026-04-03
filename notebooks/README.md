# Notebook workflow

This directory contains the stepwise Jupyter notebooks used to reproduce the analytical workflow of the manuscript.

## Recommended execution order

1. `01_preprocessing_SPI_SGI.ipynb`  
   Loads monthly groundwater-level and precipitation datasets, computes SPI and SGI time series, and exports processed monthly outputs.

2. `02_event_metrics.ipynb`  
   Detects SGI-based drought events and derives cluster-level drought metrics including duration, propagation, recovery, resistance, resilience, and vulnerability.

3. `03_DIPI_construction.ipynb`  
   Constructs the Drought Impact Propagation Index (DIPI), including normalized subcomponents, exposure, pressure, sensitivity, and final DIPI values.

4. `run_full_reproducibility_workflow.ipynb`  
   Master reproducibility notebook summarizing the full workflow, expected outputs, repository structure, and execution logic.

## Output logic

Intermediate and final analytical outputs are exported to:

- `../data_processed/`
- `../figure_source_data/`

These notebooks form the full reproducible workflow accompanying the HESS manuscript.
