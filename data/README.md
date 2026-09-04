# Data Documentation

This project uses two secondary, non-personal datasets. Raw data are not redistributed here due to licensing and file-size constraints. Use the links below to obtain them, and cite them under their applicable terms.

## 1. Flight data — OpenSky / Zenodo
- Source: OpenSky-derived flight-list archive (January 2022).
- DOI: https://doi.org/10.5281/zenodo.7923702
- Fields used: flight identifier, origin, destination, endpoint coordinates, first/last UTC timestamps.
- 

## 2. Meteorology — ERA5 (Copernicus / ECMWF)
- Source: ERA5 hourly data on pressure levels from 1940 to present.
- DOI: https://doi.org/10.24381/cds.bd0915c6
- Access: Copernicus Climate Data Store (https://cds.climate.copernicus.eu)
- Variables: temperature, relative humidity, specific humidity, cloud ice water content, cloud cover, horizontal winds, geopotential.
- Domain: 10–40°N, 30–70°E | Levels: 150, 200, 225, 250, 300, 350 hPa
- Resolution: 0.25° grid, 4-hour timesteps
- 

## Preprocessing (summary)
Endpoints → adaptive great-circle waypoints → rounded to nearest 0.25° ERA5 centre and nearest 4-hour timestep → many-to-one waypoint-to-key join. Full steps are in notebooks/AeroContrail_analysis.ipynb.

## Licensing note
OpenSky/Zenodo and Copernicus/ECMWF data must be used and cited according to their access and licence terms. Flight-level identifiers must not be used to infer individual behaviour or for surveillance.
