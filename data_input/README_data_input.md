# data_input description

This folder contains the monthly input datasets and piezometer metadata used as the starting point for the reproducible analyses.

## Files

- `groundwater_levels_monthly.csv` — monthly groundwater-level observations in long format, with the fields `date`, `piezometer_id`, `groundwater_level_m`, and `cluster_id`
- `metadata_piezometers.csv` — piezometer metadata, including aquifer-group assignment, coordinates, screened depth intervals, total well depth, stratigraphy, and lithology
- `precipitation_monthly.csv` — monthly precipitation totals from five IMGW monitoring stations used for SPI calculation

## Temporal coverage

- `groundwater_levels_monthly.csv`: July 1985–April 2024; record length and data availability vary among piezometers
- `precipitation_monthly.csv`: January 1986–April 2024

## Coordinate reference system

Piezometer coordinates are provided in **ETRF2000-PL / CS92 (EPSG:2180)**.

## Data structure notes

- `cluster_id` is retained as the original numerical group identifier for compatibility with the analytical workflow
- descriptive text in the manuscript and repository uses the term **aquifer group**
- groundwater-level records are monthly and stored in long format, with one row representing one piezometer and one month
- missing months are preserved as gaps and are not interpolated
- precipitation data are stored in wide format, with one column per monitoring station

## Reproducibility note

These datasets constitute the minimal input layer used directly by the analytical notebooks. Derived SGI series, drought events, drought metrics, propagation matches, and DIPI outputs are stored in `../data_processed/`.
