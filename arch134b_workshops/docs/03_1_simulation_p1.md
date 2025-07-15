# Loads and EUI Simulation

## Model to OSM component
Recreate the components and connections as shown below. Leave youreself some space in the canvas for future components. Note the toggle component is left as false and connected to both write and run. Leaving this toggle as false will prevent early simulation runs which take a few seconds to load. 

```{image} ../_static/sim1/sim1_1.png
:width: 100%
:align: center
```
<br/><br/>

## Simulation Parameters components
Continue recreating the components and connections shown in the images step-by-step.
```{image} ../_static/sim1/sim1_2.png
:width: 100%
:align: center
```
<br/><br/>

## Room Energy Result
Note the several outputs of the "HB Model to OSM" component. We will use the sql output the most in future modules. Think of this as the main simulation data. There is a ton of data contained here. We will route this vast data to other components to preform operations on and visualize specific parts of the data.

```{image} ../_static/sim1/sim1_3.png
:width: 100%
:align: center
```
<br/><br/>

## Monthly Load Balance Visualization
Connect the model output of "HB Model" to _rooms_model input of "HB Thermal Load Balance" (LoadBalance). 
```{image} ../_static/sim1/sim1_4.png
:width: 100%
:align: center
```
<br/><br/>

## Legend Parameters
```{image} ../_static/sim1/sim1_5.png
:width: 100%
:align: center
```
<br/><br/>

## Load Balance Plot
This is the load balance plot which should be generated in your Rhino viewport. To see this plot, it may be helpful to open a new "Top" Viewport, maximize it, and zoom out a bit.

```{image} ../_static/sim1/sim1_6.png
:width: 100%
:align: center
```
<br/><br/>

This plot shows the heat gains and losses colored by source for each month. Notice that the heat gains cancel out the heat losses. This means by the end of each month we finish at the same temperature we started. We see that more energy is used for "Heating" than "Cooling". This represents the required active heating and cooling that would be preformed by an HVAC system. Notice the "Infiltration" source in teal. Read more about that here: https://en.wikipedia.org/wiki/Infiltration_(HVAC)

## Heating and Cooling Loads Visualization
The "TimeOp" component takes both heating and cooling data from EnergyResult as inputs to _data.

```{image} ../_static/sim1/sim1_7.png
:width: 100%
:align: center
```
<br/><br/>

## Dry Bulb Temp Visualization
Create a new monthly chart with an appropriate base_pt _. Connect the dry_bulb_temperature output of your ImportEPW component to the _data input of your new monthly chart. Another view of this configuration is shown in the next image.

```{image} ../_static/sim1/sim1_8.png
:width: 100%
:align: center
```
<br/><br/>

## Double-check Canvas
This is what your plot generation logic should look like.

```{image} ../_static/sim1/sim1_9.png
:width: 100%
:align: center
```
<br/><br/>

## Monthly Heating and Cooling Loads Plot with Temperature
This is what your second and third generated plots should look like. The top shows average daily temperatures by month. The bottom shows heating and cooling loads for each month. We have higher heating loads in the winter and higher cooling loads in the summer. 

Consider the results. Does this align with what you would expect?

```{image} ../_static/sim1/sim1_10.png
:width: 100%
:align: center
```
<br/><br/>

## Finding Construction and Program Sets
Explore the drop down menus to find an appropriate construction set. For our case study, we are in Van Nuys, California which is in Climate Zone 3 (**add reference**). We can choose a newer vintage to start, assuming the home was built recently.

```{image} ../_static/sim1/sim1_11.png
:width: 100%
:align: center
```
<br/><br/>

Here is another reference image including the HB panel where you can drag and drop many of these components from.

```{image} ../_static/sim1/sim1_12.png
:width: 100%
:align: center
```
<br/><br/>

## Connect Sets to Room Definition
We can copy and paste the program and construction set values into a panel for accesibility. Then we can connect these panels to our main workflows. This leaves, the drop down menus free to explore without triggering a new simulation accidentally.

```{image} ../_static/sim1/sim1_13.png
:width: 100%
:align: center
```
<br/><br/>

## Compare EUI by Source for Different Vintages
Try recording your simulation EUI with your vintage of choice in a menu. Then change the vintage, ensuring these sets are reflected in the panels attatched  to your main workflow. Compare the EUI side by side. Do your results align with your expectations? 

```{image} ../_static/sim1/sim1_14.png
:width: 100%
:align: center
```
<br/><br/>
