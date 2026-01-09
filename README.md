# THERMOSYNTH.AI

**A Self-Learning Urban Heat Intelligence & Policy Digital Twin**  
*Software-only digital twin for simulating, visualizing, and optimizing urban heat mitigation strategies.*

---

## Table of Contents
- [Project Overview](#project-overview)
- [Core Features](#core-features)
- [System Architecture](#system-architecture)
- [Installation & Setup](#installation--setup)
- [Running the Project](#running-the-project)
- [Usage & Dashboard](#usage--dashboard)
- [Future Development](#future-development)
- [Contributors](#contributors)

---

## Project Overview

**THERMOSYNTH.AI** is a software-based platform designed to model, simulate, and optimize urban heat and its socio-environmental impacts. It integrates:

- Spatial city modeling  
- Temporal heat simulation  
- Human vulnerability estimation (Heat Vulnerability Index, HVI)  
- Policy experimentation and reinforcement learning-based planning  
- Interactive visualization for decision support  

This tool allows urban planners, policymakers, and researchers to evaluate interventions **before real-world implementation**, helping reduce heat, inequality, and cost.

---

## Core Features

1. **Spatially Realistic Urban Grid**  
   - City represented as a 2D grid of blocks/buildings  
   - Each block has attributes: density, roof type, vegetation, population

2. **Dynamic Heat Simulation**  
   - Time-series simulation of heat and HVI over days/weeks  
   - Monte Carlo simulations for policy scenarios

3. **Policy Brain & Reinforcement Learning**  
   - RL agent suggests optimal interventions (trees, cool roofs, pavements)  
   - Long-horizon planning and scenario comparison

4. **Interactive Dashboard**  
   - 2D and 3D heat maps  
   - Time-series graphs  
   - Sensitivity analysis and spider charts  
   - Click-to-explore blocks for detailed data  
   - Explanatory tooltips for common users and reviewers

5. **Scientific Rigor**  
   - Predictive analytics for next-week heat trends  
   - Policy efficiency scoring combining cost, heat reduction, and equity  
   - Uncertainty bands using Monte Carlo simulations

---

### Layer Details

1. **Satellite / GIS Data**
   - Source of baseline geographic, land-use, and urban structure information.
   - Provides input for all downstream layers.

2. **Thermal Core (LST Prediction)**
   - Predicts Land Surface Temperature (LST) per city block/grid.
   - Uses machine learning (XGBoost / LightGBM) trained on satellite-derived temperature data.

3. **Structural Layer (Roof & Material Intelligence)**
   - Encodes building properties: roof type, area, albedo, cooling potential.
   - Computes marginal heat contribution per building for policy planning.

4. **Flow Layer (Airflow & Heat Dissipation)**
   - Models wind corridors and heat dispersion across the city.
   - Identifies heat stagnation zones dynamically without heavy CFD simulations.

5. **Human Layer (Heat Vulnerability Index)**
   - Computes HVI using population density, income proxy, and vulnerable groups.
   - Highlights socially critical heat hotspots for equitable planning.

6. **Policy Brain (Reinforcement Learning Agent)**
   - Suggests optimal interventions like tree planting, cool roofs, and open corridors.
   - Balances objectives: minimize heat, HVI, cost, and maximize equity.

7. **Interactive Dashboard (2D / 3D Visualization)**
   - Provides intuitive visualizations for heat, HVI, policy suggestions, and sensitivity analysis.
   - Enables click-to-explore grids, scenario comparison, and time-series animations.

---

## Installation & Setup

1. Clone the repository:

```bash
git clone <repository_url>
cd THERMOSYNTH_AI

## System Architecture

