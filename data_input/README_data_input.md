# data_input description

This folder contains the processed monthly input datasets used as the starting point for all reproducible analyses.

## Files
- `groundwater_levels_monthly.csv` – monthly groundwater-level observations in long format (`date`, `piezometer_id`, `groundwater_level_m`, `cluster_id`)
- `metadata_piezometers.csv` – piezometer metadata including coordinates, depth intervals, lithology, and stratigraphy
- `precipitation_monthly.csv` – monthly precipitation totals from monitoring stations used for SPI computation

## Temporal coverage
1985–2024 monthly records.

## Coordinate reference system
Piezometer coordinates are provided in **ETRF2000-PL / CS92 (EPSG:2180)**.

## Notes
These datasets represent the minimal reproducible input layer derived from institutional monitoring data and used directly by the analytical notebooks.
