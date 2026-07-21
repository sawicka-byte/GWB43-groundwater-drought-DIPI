# Notebook workflow

This directory contains the stepwise Jupyter notebooks used to reproduce the analytical workflow of the manuscript.

## Recommended execution order

1. `01_preprocessing_SPI_SGI.ipynb`  
   Loads monthly groundwater-level data and piezometer metadata, calculates well-level SGI-3, SGI-6, and SGI-12 using the revised calendar-month normal-score procedure, and derives dynamically supported aquifer-group SGI series.

2. `02_event_metrics.ipynb`  
   Detects SGI-based groundwater drought events and calculates well-level and aquifer-group metrics, including duration, severity, intensity, vulnerability, resistance, resilience, recovery, and SGI-3 to SGI-12 propagation probability.

3. `03_DIPI_construction.ipynb`  
   Calculates the weighted DIPI as `0.4E + 0.3P + 0.3S`, retains the equal-weight variant `(E + P + S) / 3`, checks the legacy DIPI column, and exports updated point-scale and aquifer-group summaries.

## Main outputs

The notebooks export analytical products to:

- `../data_processed/`

The figure source-data packages are stored separately in:

- `../figure_source_data/`

## Notes

- The notebooks use the term **aquifer group** rather than **cluster** in descriptive text.
- The identifier `cluster_id` is retained in some files for backward compatibility with the original data structure.
- The mapped DIPI products in the manuscript were generated from GIS rasters; point-scale DIPI values are sampled representations used for quality control and summary analyses.
