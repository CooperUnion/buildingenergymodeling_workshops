# Passive Design and Comfort Part 2: Visualizing Thermal Comfort and Energy Reduction

## Set Shade geometry
Right click the ExistingShades sub-layer and select the layer.

```{image} ../_static/psvdgn1/psvdgn1_1.png
:width: 100%
:align: center
```
<br/><br/>

Then, right-click the geometry component and select Set Multiple Geometries.

```{image} ../_static/psvdgn1/psvdgn1_2.png
:width: 100%
:align: center
```
<br/><br/>

## Verify Shade Geometry
Verify that selecting the geometry component linked to the shades highlights the shades in green. Clicking elsewhere in the canvas highlights the shade red. Then, hide the preview for the geometry component.

```{image} ../_static/psvdgn1/psvdgn1_3.png
:width: 100%
:align: center
```
<br/><br/>

Find a video demonstration here:
[![Watch the video](https://github.com/gaudi369/buildingenergymodeling_workshops/blob/main/arch134b_workshops/_static/psvdgn1/psvdgn1_2.png)](https://github.com/gaudi369/buildingenergymodeling_workshops/blob/main/arch134b_workshops/_static/psvdgn1/psvdgn1_1.mp4)

## Link Shades to Model
```{image} ../_static/psvdgn1/psvdgn1_5.png
:width: 100%
:align: center
```
<br/><br/>

## Add Window Border Shades
Use a "LB Cumulative Sky Matrix" component. Connect the outputs of ImportEPW component to the respective inputs of SkyMatrix. This models an adjustable border along the perimeter of the windows. 

```{image} ../_static/psvdgn1/psvdgn1_6.png
:width: 100%
:align: center
```
<br/><br/>

## Create Sky Matrix from Imported EPW Data
Insert a "LB Analysis Period" component and connect to the _hoys output of SkyMatrix. Create two integer-type Number Sliders, one ranging from 1 to 12 and the other from 1 to 31. Connect the former to _start month and _end month inputs to represent the 12 months of the year. Wire the latter to _start day and _end day for the 30 days of the month.

```{image} ../_static/psvdgn1/psvdgn1_7.png
:width: 100%
:align: center
```
<br/><br/>

## Set Analysis Period for Summer Design Day
June 21st is chosen as our model summer design day.

```{image} ../_static/psvdgn1/psvdgn1_8.png
:width: 100%
:align: center
```
<br/><br/>

## Create Incident Radiation Visualization
```{image} ../_static/psvdgn1/psvdgn1_9.png
:width: 100%
:align: center
```
<br/><br/>

## Reference Screenshot: Linking Geometry to the Incident Radiation Block
Note the geometries are connected all the way back to the IncidentRadiation _geometry input.

```{image} ../_static/psvdgn1/psvdgn1_10.png
:width: 100%
:align: center
```
<br/><br/>

## Generated Incident Radiation Visualization in Rhino
This shows how much sunlight hits each part of the model's surface. Use a perspective view to explore the visualization. What do you notice?
**need to fix bug that shows part of the roof as not having incident radiation**

```{image} ../_static/psvdgn1/psvdgn1_11.png
:width: 100%
:align: center
```
<br/><br/>

## Create Radiation Dome Visualization
```{image} ../_static/psvdgn1/psvdgn1_12.png
:width: 100%
:align: center
```
<br/><br/>

## Generated Radiation Dome Visualization in Rhino
This shows the apparent sunlight hitting our location from the sky. Notice it is not exactly symmetrical. 

```{image} ../_static/psvdgn1/psvdgn1_13.png
:width: 100%
:align: center
```
<br/><br/>


