# Exposure interpolation

This folder contains the piezometer-level inputs and leave-one-out cross-validation outputs used to construct and evaluate the spatial Exposure component of the Drought Impact Potential Index (DIPI).

## Files

- `Exposure_SGI12_piezometers_GIS_join.csv` — piezometer-level SGI-12 drought metrics and normalized Exposure inputs for the 16 monitoring wells. The table contains coordinates, aquifer-group assignment, vulnerability, resilience, maximum drought duration, normalized subcomponents, and the resulting Exposure score.
- `TopoToRaster_LOO_results.csv` — detailed leave-one-out cross-validation results for the three interpolated Exposure subcomponents. For each omitted piezometer and variable, the file reports the observed value, predicted value, prediction error, and number of training points.
- `TopoToRaster_LOO_summary.csv` — summary leave-one-out performance statistics for each interpolated Exposure subcomponent, including mean error (ME), mean absolute error (MAE), root mean square error (RMSE), and the observed–predicted Pearson correlation coefficient.

## Exposure formulation

The piezometer-level Exposure score was calculated as:

```text
EXPOSURE = 0.4 × VUL_N + 0.3 × CRS_INV + 0.3 × MAXDUR_N
```

where:

- `VUL_N` is min–max-normalized SGI-12 vulnerability;
- `CRS_INV` is the inverse min–max-normalized resilience score;
- `MAXDUR_N` is min–max-normalized maximum SGI-12 drought duration.

All normalized variables range from 0 to 1.

## Input-table fields

- `PIEZ_ID` — piezometer identifier
- `X`, `Y` — projected coordinates
- `CLUSTER` — aquifer-group identifier used in the analytical workflow
- `VUL12` — SGI-12 vulnerability, expressed as the maximum absolute cumulative drought deficit
- `VUL_N` — min–max-normalized vulnerability
- `CRS12` — SGI-12 resilience, defined as the one-step probability of transition from drought to non-drought conditions
- `CRS_N` — min–max-normalized resilience
- `CRS_INV` — inverse normalized resilience score, calculated as `1 - CRS_N`
- `MAXDUR12` — maximum SGI-12 drought-event duration in months
- `MAXDUR_N` — min–max-normalized maximum duration
- `EXPOSURE` — composite piezometer-level Exposure score

## Spatial reference

The `X` and `Y` coordinates are provided in ETRF2000-PL / CS92 (EPSG:2180).

## Interpolation and cross-validation

`VUL_N`, `CRS_INV`, and `MAXDUR_N` were interpolated separately using the Topo to Raster algorithm with drainage enforcement disabled. The same GWB 43 boundary, raster extent, cell size, and snap raster were used for all three surfaces.

Leave-one-out cross-validation was performed separately for the three subcomponents. In each iteration, one of the 16 piezometers was omitted, the interpolation surface was regenerated from the remaining 15 wells using the same settings as the final surface, and the predicted value was extracted at the omitted location.

The cross-validation outputs are intended to quantify empirical interpolation performance at the monitoring locations. They do not constitute a continuous model-based prediction-standard-error surface.
