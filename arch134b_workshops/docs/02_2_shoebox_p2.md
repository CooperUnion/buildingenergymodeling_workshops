# Shoebox Model and Basic Visualizations

## Opening your shoebox model
Download the single family home Rhino model from Github: <a href="https://github.com/gaudi369/buildingenergymodeling_workshops/blob/main/arch134b_workshops/_downloads/single_family.3dm" target="_blank">here</a>

Open your single_family.3dm model. 

Hide the three layers as shown below. Your home should now appear as a simplified box. When we learn to analyze a building, we start with the simplest form first.

```{image} ../_static/shoebox2/shoebox2_1.png
:width: 100%
:align: center
```
<br/><br/>

## Create a "Geometry" component 
Double-click the canvas, type in "geometry", click to select the component, and click again on the canvas to place the component. 

```{image} ../_static/shoebox2/shoebox2_2.png
:width: 100%
:align: center
```
<br/><br/>

## Select objects
Locate the "Zones" sub-layer within the SINGLE_ZONE layer. Right click it and click "Select Objects"

```{image} ../_static/shoebox2/shoebox2_3.png
:width: 100%
:align: center
```
<br/><br/>

# Set one geometry
Right click your geometry component and select "Set one Geometry".
```{image} ../_static/shoebox2/shoebox2_4.png
:width: 100%
:align: center
```
<br/><br/>

## Check if geometry is set
If your geometry is set properly, clicking your geometry component will highlight your zone in green in Rhino. Clicking elsewhere in the canvas will highlight the zone in red. 

```{image} ../_static/shoebox2/shoebox2_5.png
:width: 100%
:align: center
```
<br/><br/>

## Create "Rooms Solid" Component
Create a "Rooms Solid" component similarly to how you searched an placed the "Geometry" component earlier. Connect your Geometry to the _geo input.

```{image} ../_static/shoebox2/shoebox2_6.png
:width: 100%
:align: center
```
<br/><br/>

## Set Windows and link to Aperture
Select the objects in your Window layer and "Set Multiple Geometries" in a new geometry component. Connect it to an "Aperture" component. 

```{image} ../_static/shoebox2/shoebox2_7.png
:width: 100%
:align: center
```
<br/><br/>

## Add Subface
Create the 'AddSubface' component. Connect rooms -> hb_obj and apertures -> '_sub_faces' as shown.

```{image} ../_static/shoebox2/shoebox2_8.png
:width: 100%
:align: center
```
<br/><br/>

## Create Model
Create the Model component, then connect hb_obj -> rooms_ as shown.

```{image} ../_static/shoebox2/shoebox2_9.png
:width: 100%
:align: center
```
<br/><br/>

## Visualize Room Attributes
Continue to recreate the block diagram step-by-step by searching for components, placing, and connecting them.

```{image} ../_static/shoebox2/shoebox2_10.png
:width: 100%
:align: center
```
<br/><br/>

## Specify Legend Parameters
The yellow box is a "Panel" component. This component can be double clicked and typed into. Alternatively, double click the canvas then type "6 and press enter. This should create the same panel as shown in the image. 

```{image} ../_static/shoebox2/shoebox2_11.png
:width: 100%
:align: center
```
<br/><br/>

## Check Room Attributes and Group Block
Selected components can be grouped into a purple box with CTRL+G. To select compontents, hold SHIFT and click them. Alternatively, hold left-click and drag the generated rectangular box around the components your want to select.

The ColorRoomAttributes component we created should color the floor of your shoebox model and generate a legend indicating the selected attribute and associated value. Click through several attributes in your dropdown menu component in Grasshopper and watch the generated visual change in Rhino . 

```{image} ../_static/shoebox2/shoebox2_12.png
:width: 100%
:align: center
```
<br/><br/>

## Check Face Attributes
Hide the Room Attribute visualization by right clicking the component and selecting "Hide Preview". The Face Attribute visual shows useful characteristics such as the material type. It can also visualize thermal resistance (called R-values) and thermal conductance (called U values or G values). Read more here: https://en.wikipedia.org/wiki/Thermal_conductance_and_resistance

```{image} ../_static/shoebox2/shoebox2_13.png
:width: 100%
:align: center
```e
<br/><br/>
