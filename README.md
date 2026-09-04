# AeroContrail-UAE

**Persistent Contrail Susceptibility in UAE-Connected Flights**
Reconstructed Paths, ERA5 Reanalysis, and Leakage-Aware Prediction

A reproducible, proxy-based assessment of contrail-susceptible atmospheric
conditions across reconstructed UAE-connected flight corridors during
January 2022, combining OpenSky/Zenodo endpoint flight records with ERA5
reanalysis at six pressure levels.

---

## Overview

Persistent contrails are a non-CO2 climate forcing from aviation, but exposure
is hard to estimate when flight and meteorological records differ in spatial,
temporal, and vertical resolution. This project reconstructs UAE-connected
flight corridors from endpoint coordinates, links each waypoint to ERA5
atmospheric fields, and evaluates where contrail-susceptible conditions
(T ≤ -40 °C and RHi ≥ 100%) concentrate. It also trains a leakage-aware
XGBoost model under a strict temporal hold-out.

**Key results (January 2022):**
- Overall susceptibility prevalence: **0.913%**, peaking at **2.644% at 300 hPa**
- **4.292%** of waypoints and **18.07%** of flights intersected ≥1 susceptible layer
- XGBoost hold-out: **ROC-AUC 0.9958**, **PR-AUC 0.5951**

> These are proxy/upper-bound estimates of atmospheric opportunity, **not**
> confirmation of observed contrails.

---

## Repository structure

