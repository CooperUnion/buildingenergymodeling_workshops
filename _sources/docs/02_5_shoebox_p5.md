# Shoebox Model-Part 5: Visualization of Results

## Download visualization template 
1. Go to this <a href="https://github.com/chenkianwee/ifc2osmod_gendgn_egs/blob/main/svg/viz_template.svg" target="_blank">webpage</a> and download the visualization template.
```{image} ../_static/shoebox5/shoe5_1.png
:width: 100%
:align: center
```
<br/><br/>

2. Open the 'viz_template.svg' with inkscape.
```{image} ../_static/shoebox5/shoe5_2.png
:width: 100%
:align: center
```
<br/><br/>

3. Turn on and off the Grid and Guide lines by going to View -> Page Grid and View -> Guides. Or shortcut key 'Shift + #' (toggle grid) and 'Shift + |' (toggle guides).
```{image} ../_static/shoebox5/shoe5_3.png
:width: 100%
:align: center
```

## Export image from FreeCAD
1. We want to add an image of the iteration to the template. We can grab an image by going back to the FreeCAD model. In FreeCAD, Go to View -> Perspective View. Adjust the view accordingly.
```{image} ../_static/shoebox5/shoe5_4.png
:width: 100%
:align: center
```
<br/><br/>

2. Go to File -> Print preview. To check if this is the view you want.
```{image} ../_static/shoebox5/shoe5_5.png
:width: 100%
:align: center
```
<br/><br/>

3. At the Print preview window click on the Print icon as shown below. The print window will pop up. Make sure to change the Name -> Print to File (PDF). You can specify the directory of the output file.
```{image} ../_static/shoebox5/shoe5_6.png
:width: 100%
:align: center
```
<br/><br/>

4. At the Print window you can click on Properties. In the Properties window you can decide how big you want your image to be by specifying the 'Paper size'. In this case I specify it to be 'A5' size.
```{image} ../_static/shoebox5/shoe5_7.png
:width: 100%
:align: center
```
<br/><br/>

5. Once everything is set. You can click on Print to save the image.
```{image} ../_static/shoebox5/shoe5_8.png
:width: 100%
:align: center
```
<br/><br/>

6. For some reason, Inkscape is not able to import the pdf exported by FreeCAD. We have to convert the pdf to png. Here I will be using Gimp to do the conversion. In Gimp, go to File -> Open and choose the exported pdf file. A Import from PDF window will pop up. Just click Import. 
```{image} ../_static/shoebox5/shoe5_9.png
:width: 100%
:align: center
```
<br/><br/>

7. Once opened in GIMP. Go to File -> Export as. In the dialog box change the name of the file to filename.png. Export the image as a png.
```{image} ../_static/shoebox5/shoe5_10.png
:width: 100%
:align: center
```
<br/><br/>

8. Import the image into Inkscape. In Inkscape go to File -> Import. Choose the image you want to import and click on Open. In the import dialog box choose Link. 
- Link: Inkscape is just referencing the image file and not storing it in Inkscape. So if you export and overwrite the image, Inkscape will automatically reflect that.
- Embed: The image file is stored in Inkscape. The image and Inkscape is totally independent.
```{image} ../_static/shoebox5/shoe5_11.png
:width: 100%
:align: center
```
<br/><br/>

9. Click on the image and resize it to fit in the template as shown.
```{image} ../_static/shoebox5/shoe5_12.png
:width: 100%
:align: center
```

## Grab graph from OpenStudio
1. Now lets go to OpenStudio Application and grab the graph of the HVAC load. Go to the Results Summary tab, from the Reports choose 'OpenStudio Results'. In the results window side bar, choose HVAC Load Profiles. Print screen the graph of the HVAC loads profile.
```{image} ../_static/shoebox5/shoe5_13.png
:width: 100%
:align: center
```
<br/><br/>

2. Import the image into the Inkscape svg visualization template. 
```{image} ../_static/shoebox5/shoe5_14.png
:width: 100%
:align: center
```
<br/><br/>

3. Remember to also import the legend so we can understand the graph.
```{image} ../_static/shoebox5/shoe5_15.png
:width: 100%
:align: center
```
<br/><br/>

4. Now lets go to the OpenStudio Results Summary tab again and go to Model Summary.
```{image} ../_static/shoebox5/shoe5_16.png
:width: 100%
:align: center
```
<br/><br/>

5. Go back to Inkscape. Let's put this information in the description of visualization template. Double click on the text box of the first row and fill in as accordingly.
```{image} ../_static/shoebox5/shoe5_17.png
:width: 100%
:align: center
```
<br/><br/>

6. Lets change the title of the panel to 'Shoebox Model Exploration'. Double-click on the title text box and change the title. Adjust it back to the position with help from guides (turn them on).
```{image} ../_static/shoebox5/shoe5_18.png
:width: 100%
:align: center
```
<br/><br/>

7. Congratulations!! You have successfully Model, Simulate and Visualize the shoebox model. Complete the template by varying design parameters like bigger window to wall ratio, thermal resistance and window u-value. So you can see how design parameters change HVAC performance.
```{image} ../_static/shoebox5/shoe5_19.png
:width: 100%
:align: center
```