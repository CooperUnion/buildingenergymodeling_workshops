# Shoebox Model-Part 2: Defining the Thermal Properties of the Model

## Create thermal spatial zone 
1. Next we will try to draw the thermal zone for the shoebox. First hide the walls and roof of the shoebox. Shift+select all the walls and the slab as shown in the image below. Right click -> Toggle visibility. You can also use the keyboard shortcut key Space to turn on/off the visibility.
```{image} ../_static/shoebox2/shoe2_1.png
:width: 100%
:align: center
```
<br/><br/>
2. Draw a square on the slab. Use the 2d offset function to offset -100mm to the square. We want to create a zone that coincides with the centerline of each wall. Each wall is 200mm thick. 
```{image} ../_static/shoebox2/shoe2_2.png
:width: 100%
:align: center
```
<br/><br/>
3. Select the floor slab and toggle visibility (press space to toggle visibility). Click on the arrow on the offset2d and also toggle visibility of Rectangle002. Select Offset2d and adjust the z position to -100mm. The floor slab like the wall slab is also 200mm thick. For the zone to be in the centerline you need the z-position to be -100mm.
```{image} ../_static/shoebox2/shoe2_3.png
:width: 100%
:align: center
```
<br/><br/>
4. Select the Offset2D and click extrude. Extrude along 5200mm and click on OK.
```{image} ../_static/shoebox2/shoe2_4.png
:width: 100%
:align: center
```
<br/><br/>
5. Select the extrude and click on Space icon.
```{image} ../_static/shoebox2/shoe2_5.gif
:width: 100%
:align: center
```
<br/><br/>
6. Select the Space. In the data view, change the Ifc Type to 'Spatial Zone' and the Predefined Type to 'THERMAL'
```{image} ../_static/shoebox2/shoe2_6.png
:width: 100%
:align: center
```
<br/><br/>
7.Right click -> Space -> Move to group ... Move the Space into the Level object.
```{image} ../_static/shoebox2/shoe2_7.png
:width: 100%
:align: center
```
<br/><br/>
8.Right click -> Site -> Recompute object. Turn on the visibility of all the object. Your model should look like this
```{image} ../_static/shoebox2/shoe2_8.png
:width: 100%
:align: center
```

## Add custom thermal psets to the objects

1. Make sure you have added the CustomPset.csv file into the FreeCAD folder. Refer to [Getting Started Steps 7-8](02_shoebox.md#freecad) for instructions.

2. Click on Manage IFC Properties ... At the window choose the Order by to IFC type.
```{image} ../_static/shoebox2/shoe2_9.png
:width: 100%
:align: center
```
<br/><br/>
3. Select the slab object. Left click on the Add property set... parameter. Press O on the keyboard and choose 'Osmod Thermal Resistance'. Do this for the roof, floor and walls.
- Enter the following values for the slab and walls.
```
Floor slab = 0.00
Roof slab = 0.00
Walls = 0.00
```
```{image} ../_static/shoebox2/shoe2_10.gif
:width: 100%
:align: center
```
<br/><br/>

4. Select the window object. Left click on the Add property set... parameter. Press O on the keyboard and choose 'Osmod Ufactor'.
- Enter the following values for the window.
```
Window = 0.00
```
```{image} ../_static/shoebox2/shoe2_11.gif
:width: 100%
:align: center
```
<br/><br/>

5. Select the space object. Left click on the Add property set... parameter. Press O on the keyboard and choose 'Osmod Space'. Key in the values for the space.
```{image} ../_static/shoebox2/shoe2_12.gif
:width: 100%
:align: center
```
<br/><br/>

6. Key in the following values
```
FloorAreaPerPerson = 18.6
LightingPowerPerFloorArea = 6.18
ElectricEquipmentPowerPerFloorArea = 6.78
OutdoorAirFlowPerFloorArea = 0.0
```

## Export to IFC
1. Select the Site. Go to File -> Export.
```{image} ../_static/shoebox2/shoe2_13.gif
:width: 100%
:align: center
```
<br/><br/>
2. Check the exported file by opening it in FreeCAD again. Go to File -> Open
```{image} ../_static/shoebox2/shoe2_14.png
:width: 100%
:align: center
```
<br/><br/>
3. In the import window just click ok and stick with the default settings.
```{image} ../_static/shoebox2/shoe2_15.png
:width: 100%
:align: center
```
<br/><br/>
4. Double click on the IFC objects to fully load the properties and information of the object.
```{image} ../_static/shoebox2/shoe2_16.png
:width: 100%
:align: center
```
<br/><br/>

5. Now that we have exported the model to IFC. We will convert the model to OpenStudio Model in part 3 of this tutorial.