# Evaluating Passive HVAC Design Strategies Part 2: Testing Shading Design Using Energy Simulation

## Running energy simulation with OpenStudio
1. Run a base simulation using the openstudio model from [workshop 3 on thermal comfort](03_1_cmf_p1.md#thermal-comfort-model-part-1-predicting-thermal-comfort).
```{image} ../_static/psvdgn2/psvdgn2_1.png
:width: 100%
:align: center
```
<br/><br/>

2. Open the shoebox model with shade in FreeCAD and export it to IFC. Select Site. Then go to File -> Export. Export it to .ifc. 
```{image} ../_static/psvdgn2/psvdgn2_2.png
:width: 100%
:align: center
```
<br/><br/>

3. Follow the instruction in [workshop 2 shoebox modeling part 3](02_3_shoebox_p3.md#shoebox-model-part-3-openstudio-model-schedules) and [workshop 2 shoebox modeling part 4](02_4_shoebox_p4.md#shoebox-model-part-4-openstudio-model-constructions) to convert it to osmod file and run a simulation. 

4. After you run the simulation. Open the results and look at them side by side to see the results. In my case the EUI reduce from 611 kWh/m2 to 603 kWh/m2. A ~1.5% (8 kWh/m2) decrease.
```{image} ../_static/psvdgn2/psvdgn2_3.png
:width: 100%
:align: center
```

## Visualize the results
1. Download the visualization .svg template from <a href="https://github.com/chenkianwee/ifc2osmod_gendgn_egs/blob/main/svg/viz_psv_template.svg" target="_blank">here</a>.
```{image} ../_static/psvdgn2/psvdgn2_6.png
:width: 100%
:align: center
```
<br/><br/>

2. Print screen the shading studies paste it onto the template
```{image} ../_static/psvdgn2/psvdgn2_5.png
:width: 100%
:align: center
```
<br/><br/>

3. Follow the instructions from [this section on exporting image from FreeCAD](02_5_shoebox_p5.md#export-image-from-freecad) and [this section on grabbing graph results from OpenStudio](02_5_shoebox_p5.md#grab-graph-from-openstudio) in the shoebox tutorial.

4. We are trying to visualize the shading studies and its energy impact. Below is an example of the visualization.
```{image} ../_static/psvdgn2/psvdgn2_4.jpg
:width: 100%
:align: center
```