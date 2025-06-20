# Shoebox Model-Part 4: OpenStudio Model Constructions

## Specify the construction of the building envelope
1. Next click on the Spaces tab. Click on the Surfaces tab. We can see that the shoebox model only have 6 surfaces. 4 walls 1 roof and 1 floor. Here you can see the specification of each surface.

## Add a new wall construction
1. Next go to the Constructions tab. In the window go to the Constructions tab at the top. Click on the + button at the Constructions tab. Change the name of the construction to 'wall'. At the right window click on the 'My Model' tab. There are no wall materials yet.
```{image} ../_static/shoebox4/shoe4_10.png
:width: 100%
:align: center
```
<br/><br/>

2. Go to the Materials tab. Click on the 'No Mass Materials'. Click on the '+' button. Name the new material 'wall insulation'. Adjust the value of the properties as follows.
- Roughness: MediumSmooth
- Thermal Resistance: 1.65
- Thermal Absorptance: 0.9
- Solar Absorptance: 0.7
- Visible Absorptance: 0.7
```{image} ../_static/shoebox4/shoe4_11.png
:width: 100%
:align: center
```
<br/><br/>

3. Click on 'Materials'. Click on the '+' button. Name the new material '16mm gypsum board'. Adjust the value of the properties as follows.
- Roughness: MediumSmooth
- Thickness: 0.016
- Conductivity: 0.16
- Density: 800
- Specific Heat: 1090
- Thermal Absorptance: 0.9
- Solar Absorptance: 0.7
- Visible Asorptance: 0.7
```{image} ../_static/shoebox4/shoe4_5.png
:width: 100%
:align: center
```
<br/><br/>

4. Next we will use a material from the standard material library of OpenStudio Application. Click on 'Library' on the right window. Search for 'stucco'. Drag and drop '1IN Stucco' to the 'Drag from Library' parameter. Pay attention to the arrow to turn to a '+' sign before dropping the material. You will be able to see 1IN stucco in the Materials tab.
```{image} ../_static/shoebox4/shoe4_12.png
:width: 100%
:align: center
```
<br/><br/>

5. Now we can go back to the Constructions tab. Click on the wall construction. Go to the My Model tab at the right window. Search for '1IN Stucco'. Drag and drop the material onto the wall construction. Repeat for the rest of these materials.
- 16mm gypsum board
- wall insulation
- 16mm gypsum board
```{image} ../_static/shoebox4/shoe4_13.png
:width: 100%
:align: center
```
<br/><br/>

6. Your wall construction should look like this.
```{image} ../_static/shoebox4/shoe4_14.png
:width: 100%
:align: center
```
<br/><br/>

7. Do the same for the roof and floor construction.

## Roof and floor construction
1. Create a no mass roof insulation with the following values:
- Roughness: MediumSmooth
- Thermal Resistance: 8.1
- Thermal Absorptance: 0.9
- Solar Absorptance: 0.7
- Visible Absorptance: 0.7

2. Reuse the 16mm gypsum board for your roof construction. Your roof construction should look like this.
```{image} ../_static/shoebox4/shoe4_6.png
:width: 100%
:align: center
```
<br/><br/>

3. Now let's create the construction for your floor. Create a no mass material for your floor called 'floor insulation'.
- Roughness: MediumSmooth
- Thermal Resistance: 4.13
- Thermal Absorptance: 0.9
- Solar Absorptance: 0.7
- Visible Absorptance: 0.7

4. Next create a material called '100mm normal weight concrete floor'. Change the values of the parameters as follows. 
- Roughness: MediumRough
- Thickness: 0.1
- Conductivity: 2.31
- Density: 2322
- Specific Heat: 832
- Thermal Absorptance: 0.9
- Solar Absorptance: 0.7
- Visible Asorptance: 0.7

5. Your floor construction should look at follows:
```{image} ../_static/shoebox4/shoe4_28.png
:width: 100%
:align: center
```

## Edit window construction
1. In the Constructions tab. Search for 'window'. Click on the result 'Window_U_0.363_SHGC_North_0.359'. Change the name to 'window'.
```{image} ../_static/shoebox4/shoe4_15.png
:width: 100%
:align: center
```
<br/><br/>

2. Go to the Materials tab. Search for 'window'. Click on 'Window Material Simple Glazing System 1'. Change the name to 'glazing 1'. Make sure the material has the same property as shown.
```{image} ../_static/shoebox4/shoe4_16.png
:width: 100%
:align: center
```

## Assign construction to the surfaces
1. Go to the Spaces tab. In the Spaces window click on the Surfaces tab.
```{image} ../_static/shoebox4/shoe4_17.png
:width: 100%
:align: center
```
<br/><br/>

2. At the right window click on 'My Model'. Search for 'wall' and 'roof' at the right window. Then drag and drop the wall construction to all the Wall surface type and roof to the Roof Ceiling surface type
```{image} ../_static/shoebox4/shoe4_18.png
:width: 100%
:align: center
```
<br/><br/>

3. Click on the Subsurfaces tab. Check that the window subsurface has the right construction as shown below.
```{image} ../_static/shoebox4/shoe4_19.png
:width: 100%
:align: center
```

## Add measure 
1. Download the .zip file of the common Measures from <a href="https://github.com/NREL/openstudio-common-measures-gem/releases/tag/v0.11.1" target="_blank">here</a>. Unzip the zip file.

2. In the OpenStudio Application. Go to the Measures tab. Click on the 'my' icon at the bottom right of the right window. A folder window will pop out once you click it. This is the directory where you store all your Measures.
```{image} ../_static/shoebox4/shoe4_22.png
:width: 100%
:align: center
```
<br/><br/>

3. Unzip the common Measures zip file you downloaded. Go to openstudio-common-measures-gem-0.11.1 -> lib -> measures -> openstudio_results. Copy and paste the folder 'openstudio_results' into the my measure directory.
```{image} ../_static/shoebox4/shoe4_23.png
:width: 100%
:align: center
```
<br/><br/>

4. Click on 'Sync Project Measures with Library' -> Update. You should now be able to see the OpenStudio Results with a My infront of it.
```{image} ../_static/shoebox4/shoe4_24.png
:width: 100%
:align: center
```
<br/><br/>

5. Apply the OpenStudio Results measure by dragging and dropping it to the Reporting Measures.
```{image} ../_static/shoebox4/shoe4_25.png
:width: 100%
:align: center
```
<br/><br/>

6. Click on the Openstudio Results measure. Choose SI unit for the input.
```{image} ../_static/shoebox4/shoe4_26.png
:width: 100%
:align: center
```

## Run the simulation 
1. Go to Simulation Settings tab and check the simulation settings is as follows.
```{image} ../_static/shoebox4/shoe4_20.png
:width: 50%
:align: center
```
<br/><br/>

2. Go to Run Simulations tab and click on Run to start the simulation.
```{image} ../_static/shoebox4/shoe4_21.png
:width: 50%
:align: center
```
<br/><br/>

3. Go to the result section and look at the results of the simulation and choose OpenStudio Results to look at the simulation results.
```{image} ../_static/shoebox4/shoe4_27.png
:width: 100%
:align: center
```