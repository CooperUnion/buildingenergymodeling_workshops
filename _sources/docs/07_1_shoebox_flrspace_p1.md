# Shoebox Model with OpenStudio-Part 1: Building the 3D Model

1. Model a 5mx5mx5m shoebox in OpenStudio. In OpenStudio go to the 'Geometry' Tab. In the Geometry window click on the 'Editor' tab. Then click on 'New'
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_1.png
:width: 100%
:align: center
```
<br/><br/>

2. In the next window click on 'New Create a new floorplan'.
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_2.png
:width: 100%
:align: center
```
<br/><br/>

3. Change the spacing to 0.5m as we are only building a 5x5x5m shoebox model. Zoom (middle mouse scroll) and pan (left click and drag) to the center of the view port.
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_3.png
:width: 100%
:align: center
```
<br/><br/>

4. Make sure the rectangular tool icon is selected. Click on the grid and draw a 5m x 5m square.
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_4.png
:width: 100%
:align: center
```
<br/><br/>

5. Click on the 'Expand' icon at the Space tab.
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_5.png
:width: 100%
:align: center
```
<br/><br/>

6. At the expanded tab, enter 5 for the 'Floor to Ceiling Height'. Clicked on 'Merged with Current OSM' register the modeling changes.
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_6.png
:width: 100%
:align: center
```
<br/><br/>

7. Click on the '3D View' tab to see the 3D model.
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_7.png
:width: 100%
:align: center
```

## Assign thermal zones
1. Click on the 'Assignments' tab. At the dropdown list choose 'Thermal Zone'.
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_8.png
:width: 100%
:align: center
```
<br/><br/>

2. Click on the '+' sign to add a thermal zone.
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_9.png
:width: 100%
:align: center
```
<br/><br/>

3. Now go back to the 'Floorplan' tab and click on the expand icon.
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_10.png
:width: 100%
:align: center
```
<br/><br/>

4. In the expanded tab go to the 'Thermal Zone' parameter and select the thermal zone you just created, in this case 'Thermal Zone 1'.
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_11.png
:width: 100%
:align: center
```

## Model the window
1. Now go to the 'Component' tab. At the dropdown list choose 'Window'.
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_12.png
:width: 100%
:align: center
```
<br/><br/>

2. Click on the '+' icon and add a window at the middle of the south wall as shown. 
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_13.png
:width: 100%
:align: center
```
<br/><br/>

3. Click on the expand button.
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_14.png
:width: 100%
:align: center
```
<br/><br/>

4. Change the window 'Height', 'Width' and 'Sill Height' to 1, 1, 2.5 accordingly. Then click on 'Merge with Current OSM'
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_15.png
:width: 100%
:align: center
```
<br/><br/>

5. Go to 3D view and see the model.
```{image} ../_static/shoebox_flrspace1/shoebox_flrspace1_16.png
:width: 100%
:align: center
```