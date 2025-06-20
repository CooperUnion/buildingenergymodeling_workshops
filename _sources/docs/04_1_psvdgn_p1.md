# Evaluating Passive HVAC Design Strategies Part 1: Designing Windows and Shade

## Modeling shading in FreeCAD
1. In this tutorial we will be using the shoebox model that was constructed in the [previous exercise](02_shoebox.md#shoebox-model). Open the FreeCAD shoebox.FCStd model.
```{image} ../_static/psvdgn1/psvdgn1_1.png
:width: 100%
:align: center
```
<br/><br/>

2. Draw a rectangle with the rectangle tool.
```{image} ../_static/psvdgn1/psvdgn1_2.png
:width: 100%
:align: center
```
<br/><br/>

3. Select the rectangle and change the height and width
- height = 1500 mm
- width = 1500 mm
```{image} ../_static/psvdgn1/psvdgn1_3.png
:width: 100%
:align: center
```
<br/><br/>

4. Select the rectangle and extrude it.
```{image} ../_static/psvdgn1/psvdgn1_4.png
:width: 100%
:align: center
```
<br/><br/>

5. Make sure you have the mid point snap on. Select the extruded rectangle. Click on move and move it to the top of the window. 
```{image} ../_static/psvdgn1/psvdgn1_5.png
:width: 100%
:align: center
```
<br/><br/>

6. Select the extruded rectangle. Then click on slab. The extruded rectangle will now become a IFC slab object.
```{image} ../_static/psvdgn1/psvdgn1_6.png
:width: 100%
:align: center
```
<br/><br/>

7. Select the slab object in the model window. In the Data tab, look for the Ifc Type parameter and change it to 'Shading Device'.
```{image} ../_static/psvdgn1/psvdgn1_7.png
:width: 100%
:align: center
```
<br/><br/>

8. Rename the slab to 'shade'.
```{image} ../_static/psvdgn1/psvdgn1_8.png
:width: 100%
:align: center
```
<br/><br/> 

9. Right click on the shade. Select Move to group.
```{image} ../_static/psvdgn1/psvdgn1_9.png
:width: 100%
:align: center
```
<br/><br/>

10. Select Level. The shade will be added into the Level group. Save your model.
```{image} ../_static/psvdgn1/psvdgn1_10.png
:width: 100%
:align: center
```
<br/><br/> 

11. Select the Site object. Then go to File -> Export. Export the model to Wavefront OBJ - Arch module (*.obj).
```{image} ../_static/psvdgn1/psvdgn1_11.png
:width: 100%
:align: center
```

## 3D sun path analysis

1. Go to the <a href="https://drajmarsh.bitbucket.io/sunpath3d.html" target="_blank">3D sun path web app</a>. Change your Geographic location to New York:
- Latutide: 40.701
- Longitude: -74.009
- Time Zone: Eastern Time
```{image} ../_static/psvdgn1/psvdgn1_13.png
:width: 100%
:align: center
```
<br/><br/>

2. Load the shoebox_shade.obj file that was exported from FreeCAD.
```{image} ../_static/psvdgn1/psvdgn1_14.png
:width: 100%
:align: center
```
<br/><br/>

3. Once loaded, you will realize the model is not position correctly. Follow the instructions below to position it correctly.
- Shadow Model -> Mirror in Y Axis
- Shadow Model -> Swap Y and Z Axis
- Shadow Model -> Mirror in Y Axis
- Shadow Model -> Reverse Normals
- After these 3 transformation. Your model should be positioned correctly. The shaded window must be facing the south.
```{image} ../_static/psvdgn1/psvdgn1_15.png
:width: 100%
:align: center
```
<br/><br/>

4. Go to Sun-path Setting. Change the Diagram Size to 200% and untick Annual Area.
```{image} ../_static/psvdgn1/psvdgn1_16.png
:width: 100%
:align: center
```
<br/><br/>

5. Go to Date/Time panel. Click on Useful Dates -> Winter Solstice. Click on Time of Day and enter 7.
```{image} ../_static/psvdgn1/psvdgn1_17.png
:width: 100%
:align: center
```
<br/><br/>

6. Cycle through the day by clicking on the outer arrow of the Time of Day parameter. The time will move in 30 mins with each click. You can see that at noon 12pm half of the window is shaded. This is not desireable as we want winter heating. The shading is too long. 
```{image} ../_static/psvdgn1/psvdgn1_18.png
:width: 100%
:align: center
```
<br/><br/>

7. Repeat the step 5-6 for Autumn and Spring equinox and summer solstice. For e.g. the image below shows at summer solstice the shading shades the window most of the time except 9-10am and 1.30-3.30pm timing with a slice of window exposed to direct sun.
```{image} ../_static/psvdgn1/psvdgn1_19.png
:width: 100%
:align: center
```
<br/><br/>

8. You can reduce the length of the shade or size/shape of window to optimize the window and shading design.
