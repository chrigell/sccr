# Seminar in Climatology and Climate Risks – Code Repository

This repository contains the code developed for the seminar report:

**“Verification of AIFS-ENS Forecast Performance Relative to ERA5 Reanalysis for a Foehn Storm in South America”**

The report was written by **Andrin Sutter and Christian Wenger** as part of the *Seminar in Climatology and Climate Risks* at the **Institute of Geography, University of Bern**.

The notebooks were used to process AIFS-ENS ensemble forecasts and ERA5 reanalysis data, calculate derived atmospheric variables, compare forecasts at different lead times, and generate the figures presented in the report. The repository is provided as supplementary material to support transparency and reproducibility.

## Case Study

The analysis examines a foehn storm over southern South America on **17 November 2025 at 18 UTC**.

The analysis focuses on:

- 10 m wind speed
- 500 hPa wind speed
- 500 hPa temperature
- 500 hPa specific humidity
- 500 hPa geopotential height (Z500)

AIFS-ENS forecasts are compared with ERA5 reanalysis using ensemble distributions, fixed-location and neighborhood diagnostics, spaghetti plots, and spatial difference maps.

## Data Availability

The analyses use AIFS-ENS ensemble forecast data and ERA5 reanalysis data stored in NetCDF format.

The input datasets are not included in this repository because of their file size and data-distribution considerations.

The notebooks expect the following files:

### ERA5

- `ERA5_02_Foehn_SouthAmerica_pl_2025-11-17_18UTC.nc`  
  ERA5 pressure-level data for the verification time.

- `ERA5_02_Foehn_SouthAmerica_sfc_2025-11-17_18UTC.nc`  
  ERA5 surface data for the verification time.

### AIFS-ENS

- `AIFS-ENS_02_Foehn_SouthAmerica_pl_2025-11-17_18UTC.nc`  
  AIFS-ENS pressure-level forecasts

- `AIFS-ENS_02_Foehn_SouthAmerica_sfc_2025-11-17_18UTC.nc`  
  AIFS-ENS surface forecasts

File paths may need to be adjusted before executing the notebooks.

## Code Overview

The repository contains four Jupyter notebooks.

### 1. Wind analysis

- **`01_case_study_foehn_storm_wind_final.ipynb`**

Processes surface and 500 hPa wind components and calculates wind speed. The notebook produces the wind-field maps, ensemble distributions, spaghetti plots, neighborhood diagnostics, and spatial difference plots used in the report.

### 2. Temperature analysis

- **`02_case_study_foehn_storm_temperature_final.ipynb`**

Processes 500 hPa temperature data, converts temperature from Kelvin to degrees Celsius, and generates the ensemble-distribution and spatial-difference figures.

### 3. Specific-humidity analysis

- **`03_case_study_foehn_storm_specific_humidity_final.ipynb`**

Processes 500 hPa specific humidity, converts values from kg kg⁻¹ to g kg⁻¹, and generates the corresponding ensemble-distribution and spatial-difference figures.

### 4. Geopotential-height analysis

- **`04_case_study_foehn_storm_Z500_final.ipynb`**

Processes 500 hPa geopotential, converts it to geopotential height in decametres, and generates the Z500 ensemble spaghetti plots, distribution plots, and spatial difference maps.

## Usage

The notebooks are research code accompanying the seminar report and are not intended as a standalone or operational software package.

To reproduce the analysis:

1. Download or obtain the required AIFS-ENS and ERA5 NetCDF files.
2. Place the files in the directory expected by the notebooks or update the file paths accordingly.
3. Install the required Python packages.
4. Run the notebooks in numerical order.

## Citation

When using or referring to this repository, please cite the accompanying seminar report:

Sutter, A. R., & Wenger, C. L. (2026). *Verification of AIFS-ENS Forecast Performance Relative to ERA5 Reanalysis for a Foehn Storm in South America*. Unpublished seminar report, Institute of Geography, University of Bern.

## Authors

- Andrin Sutter
- Christian Wenger

## License and Disclaimer

The code is provided for academic and reproducibility purposes. No warranty is provided regarding its suitability for operational forecasting or other applications.

<a href="https://example.com">Code of sccr</a> © 2026 by <a href="https://example.com">Andrin Sutter and Christian Wenger</a> is licensed under <a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a><img src="https://mirrors.creativecommons.org/presskit/icons/cc.svg" alt="" style="max-width: 1em;max-height:1em;margin-left: .2em;"><img src="https://mirrors.creativecommons.org/presskit/icons/by.svg" alt="" style="max-width: 1em;max-height:1em;margin-left: .2em;">
