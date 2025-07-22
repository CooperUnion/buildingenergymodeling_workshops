# Direct Conversion from Rhino to OpenStudio
If you want to conduct all of your energy performance simulations in the OpenStudio software itself and need the OSM file, here is a direct way to obtain it through Grasshopper environment.

## Components Used
Geometry ([2.6.2](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/02_2_shoebox_p2.html#create-a-geometry-component)), HB Room from Solid ([2.7.2](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/02_2_shoebox_p2.html#create-rooms-solid-component)), HB Model ([2.7.5](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/02_2_shoebox_p2.html#create-model)), HB Model to OSM([3.1.1](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/03_1_simulation_p1.html#model-to-osm-component)), Boolean Toggle, Panel ([2.5.2](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/02_1_shoebox_p1.html#place-your-first-component))

## Conversion Breakdown
1. Download Rhino8 and then Pollination as referenced in [module 2](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/02_shoebox.html). Find your weather file as shown in [1.3.1](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/01_1_climate_p1.html#get-weather-file).
2. Open your model in the Rhino application. Open Grasshopper like in [2.5.1](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/02_1_shoebox_p1.html#open-grasshopper-from-rhino-by-clicking-the-circled-green-icon).
3. Recreate the [components](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/08_open_studio.html#components-used) as shown in the image below. 
```{image} ../_static/start/conversion2osm.png
:width: 100%
:align: center
```
<br/><br/>
   
