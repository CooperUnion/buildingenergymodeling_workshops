# Direct Conversion from Rhino to OpenStudio
If you want to conduct all of your energy performance simulations in the OpenStudio software itself and need the OSM file, here is a direct way to obtain it through Grasshopper environment.

## Components Used
Geometry ([2.6.2](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/02_2_shoebox_p2.html#create-a-geometry-component)), HB Room from Solid ([2.7.2](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/02_2_shoebox_p2.html#create-rooms-solid-component)), HB Model ([2.7.5](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/02_2_shoebox_p2.html#create-model)), HB Model to OSM ([3.1.1](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/03_1_simulation_p1.html#model-to-osm-component)), Boolean Toggle, Panel ([2.5.2](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/02_1_shoebox_p1.html#place-your-first-component))

## Step-by-Step Breakdown
1. Download Rhino8 and then Pollination as referenced in [module 2](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/02_shoebox.html). Find your weather file as shown in [1.3.1](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/01_1_climate_p1.html#get-weather-file).
2. Open your model in the Rhino application. Open Grasshopper like in [2.5.1](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/02_1_shoebox_p1.html#open-grasshopper-from-rhino-by-clicking-the-circled-green-icon).
3. Use the following [components](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/08_open_studio.html#components-used).

### Recreate as shown in the image below.
```{image} ../_static/start/conversion2osm.png
:width: 100%
:align: center
```
<br/><br/>

5. Set your "Geometry" component as demonstrated in [2.7](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/02_2_shoebox_p2.html#set-one-geometry). If you have multiple zones, select _Set Multiple Geometries_ and take care with naming them for work clarity. Connect all your geometries to a "HB Room from Solid" component. 
6. Wire the output rooms to the input rooms_ of a new component, "HB Model."
7. Bring in a "HB Model to OSM" component to convert the model to an OSM file. 
8. Use a "Panel" to paste the [path](https://cooperunion.github.io/buildingenergymodeling_workshops/docs/02_2_shoebox_p2.html#set-one-geometry) to your downloaded weather file, then connect it to the _epw_file input of ModeltoOSM. This contains data about the climate of where your model is for environmental analysis.
9. Create a Boolean Toggle and double-click on False to switch to True. Wire it to both the _write and run input of ModeltoOSM.

<br/><br/>
Credit: Thank you to Danielle Chiu for this Loisaida building Rhino model as well as Loisaida Inc. for permitting their location to be used as educational material. 
   
