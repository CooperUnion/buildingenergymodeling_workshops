# Shoebox Model-Part 1: 3D BIM

## Create slab, walls and window
1. Model a 5m x 5m x 5m box in FreeCAD. Create a floor slab that is 5m x 5m. Draw a rectangle that is 5m x 5m. Click on the Rectangle tool on the BIM workbench (highlighted in red box below). Draw a square.
```{image} ../_static/shoebox1/shoe1_1.png
:width: 100%
:align: center
```
<br/><br/>
2. Select the rectangle and click on the Slab tool on the workbench. A floor slab is created.
```{image} ../_static/shoebox1/shoe1_2.png
:width: 100%
:align: center
```
<br/><br/>

3. Click on the rectangle tool and draw a rectangle on the slab. If the appropriate snaps are on your cursor will snap to the edge points of your slab. 
```{image} ../_static/shoebox1/shoe1_20.png
:width: 100%
:align: center
```
<br/><br/>

4. Select the rectangle. And change the 'Make Face' parameter to 'false'
```{image} ../_static/shoebox1/shoe1_21.png
:width: 100%
:align: center
```
<br/><br/>

5. Select the rectangle and click on the 'Wall' icon.
```{image} ../_static/shoebox1/shoe1_22.png
:width: 100%
:align: center
```
<br/><br/>

6. Select the created 'Wall'. Change the 'Align' parameter to 'Right' so that the wall are within the slab.
```{image} ../_static/shoebox1/shoe1_23.png
:width: 100%
:align: center
```
<br/><br/>

7. Go to the Height parameter and change the height to 5000mm.
```{image} ../_static/shoebox1/shoe1_24.png
:width: 100%
:align: center
```
<br/><br/>

8. Now draw the roof slab. Draw a rectangle on top of the four walls. Make sure your working plane is Top.
```{image} ../_static/shoebox1/shoe1_9.png
:width: 100%
:align: center
```
<br/><br/>

9. Click on the slab icon and make the rectangle a slab.
```{image} ../_static/shoebox1/shoe1_10.png
:width: 100%
:align: center
```
<br/><br/>

10. Select the slab. Change the Predefined Type to Roof, and change the Normal Z direction to 1.00
```{image} ../_static/shoebox1/shoe1_11.png
:width: 100%
:align: center
```
<br/><br/>

11. Create a window on the front wall. Make sure your view is adjusted to Front. Click on the window icon and place your window on the lower left corner.
```{image} ../_static/shoebox1/shoe1_12.gif
:width: 100%
:align: center
```
<br/><br/>

12. Select the window and adjust the Height and Width of the window to 1500mm.
```{image} ../_static/shoebox1/shoe1_13.png
:width: 100%
:align: center
```
<br/><br/>

13. Select the window, change the position x and z of the window to 1750.
```{image} ../_static/shoebox1/shoe1_14.png
:width: 100%
:align: center
```

## Organize your model
1. Now it is time to organize your model. Click on the Site, Building and Level icons to create the respective objects.
```{image} ../_static/shoebox1/shoe1_15.png
:width: 100%
:align: center
```
<br/><br/>
2. Right click -> Level -> Move to group .... Left click on it. Move the Level to the Building object.
 ```{image} ../_static/shoebox1/shoe1_16.png
:width: 100%
:align: center
```
<br/><br/>
3. Right click -> Building -> Move to group ... Repeat the same procedure for moving the Building into the Site object.
 ```{image} ../_static/shoebox1/shoe1_17.png
:width: 100%
:align: center
```
<br/><br/>
4. Select the slabs and walls by Shift + Left Click. Right click -> Move to group ... Repeat the same procedure for moving the all the selected object into the Level object.
 ```{image} ../_static/shoebox1/shoe1_18.png
:width: 100%
:align: center
```
<br/><br/>
5. This is the end of Part 1. Your model should look like this.
 ```{image} ../_static/shoebox1/shoe1_19.png
:width: 100%
:align: center
```