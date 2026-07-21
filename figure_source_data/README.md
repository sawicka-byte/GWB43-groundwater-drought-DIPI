# Figure source data index

This directory contains source-data packages for the main-text figures and appendices accompanying the manuscript:

**Integrating propagation and recovery dynamics into groundwater drought vulnerability assessment through exposure, pressure, and aquifer system response**

## Main figures

- `fig01/` — study-area map layers, including piezometers, meteorological stations, groundwater-dependent ecosystems, mining areas, surface-water features, and the GWB 43 boundary
- `fig02/` — interpretative note for the conceptual hydrogeological cross-section
- `fig03/` — interpretative note for the conceptual synthesis diagram
- `fig04/` — SPI and revised aquifer-group SGI time series used in Figure 4
- `fig05_06/`
  - `fig05_group_drought_metrics.csv` — aquifer-group drought metrics used in Figure 5
  - `fig06_well_propagation_recovery.csv` — well-level propagation probability, SGI-12 vulnerability, and recovery status used in Figure 6
- `fig07_08/` — point-scale exposure, pressure, sensitivity, weighted DIPI, equal-weight DIPI, and E-P contrast values used to support Figures 7 and 8

## Appendices

- `Appendix_A/` — normalized DIPI subcomponents, exposure, pressure, sensitivity, weighted and equal-weight DIPI, and E-P contrast used in Figure A1
- `Appendix_B/` — full-period lagged SPI-SGI correlation matrices for lags of 0-12 months used in Figure B1
- `Appendix_C/` — moving-window stability analysis of the lag associated with the maximum SPI-SGI correlation used in Figure C1

## Methodological notes

- Revised SGI values were calculated using trailing 3-, 6-, and 12-month means and a calendar-month non-parametric normal-score transformation.
- Aquifer-group SGI values were retained only when at least 50% of wells assigned to the group and at least two wells were available.
- Positive SPI-SGI lags indicate that SGI follows SPI.
- Figure B1 uses full-period Pearson correlations for lags of 0-12 months.
- Figure C1 uses calendar-based 10-year moving windows shifted forward by 1 year; only windows with at least 96 valid paired monthly observations were retained.
- The main DIPI variant is calculated as `0.4E + 0.3P + 0.3S`.
- The equal-weight DIPI variant is retained as `(E + P + S) / 3` for robustness comparison.
- Manuscript DIPI maps were generated from GIS rasters. Point-scale tables contain values sampled at piezometer locations and are provided for transparency, quality control, and descriptive summaries.

Conceptual figures are accompanied by interpretative notes rather than standalone numerical datasets.
