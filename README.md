# Building Energy Modeling Workshops (Rhino & Ladybug Tools Edition) 2025

## ACTUAL LINK:
[energy_modeling_workshops](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/intro.html) (change link in about section ASAP)

tutorials for understanding hvac performance when doing architectural design 

- forked from arch134b_workshops by kian wee on 6/20/2025
- developed by Gautaman Asirwatham and Amber Sun under our advisor Professor Melody Baglione

## Tooling Details

**Core Simulation Engines:**

Energy Plus: thermal and energy modeling

Radiance: lighting

**Environment / Connectors:**

OpenStudio: alt frontend - Connects Pollination

Rhino 8 w/ Grasshopper: 3D modeling

Pollination: analysis suite (Rhino/Grasshopper Plugin)

**Other:**

VSCode: code editor

Inkscape: graphics editor

**Dependencies and Installation Notes:**
- Simulation engines are mainly Linux based applications
- Pollination is designed for Python 3.x environment
- Grasshopper plugins might need to be installed after Rhino
- Some issues may be caused on school computers due to SentinelOne blocking our software. Recomended fix: install on your own laptop.

### Note about why we chose these tools for our workflow
Our main constraint was that Rhino is our 3D modeling software of choice since Cooper Union architects are trained in Rhino. 

EnergyPlus and OpenStudio are common dependancies for energy simulation and were the most popular and well supported choices. There were 3 alternatives considered for how to connect our Rhino environment to our core simulation engines (EnergyPlus and OpenStudio). These are ClimateStudio, Design Builder, and Pollination. Of these, only Pollination has its source code available which was prioritized to enable debugging and allow for more control of the simulation logic. This choice also has the advantage of being free.

### Other Tools for future work

OpenFoam: fluid dynamics

Eddy 3D: Airflow analysis (Rhino/Grasshopper Plugin)

REopt: energy gen system sizing

System Advisor Model: system analysis

