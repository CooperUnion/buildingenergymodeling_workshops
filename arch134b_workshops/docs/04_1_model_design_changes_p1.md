# 8760 Models and Peak Loads

## Creating more 8760 visualizations
Recreate this block on your canvas. Explore connecting several RoomEnergyResult outputs to the _data input of Hourly Plot. Observe the generated plots. Use a LB Deconstruct Data (XData) component to see the header of the plots.

```{image} ../_static/hvac1/hvac1_1.png
:width: 100%
:align: center
```
<br/><br/>

## 8760 Plots
The image shows 8760 plots for heating, cooling, solar gain, and infiltration load. Do you notice any connections between the plots?

```{image} ../_static/hvac1/hvac1_2.png
:width: 100%
:align: center
```
<br/><br/>

## Calculating Peak Heating and Cooling Loads
Follow along recreating the components (HB Read HVAC Sizing) and connections shown.

```{image} ../_static/hvac1/hvac1_3.png
:width: 100%
:align: center
```
<br/><br/>

## Visualizing Peak Heating and Cooling Loads
```{image} ../_static/hvac1/hvac1_4.png
:width: 100%
:align: center
```
<br/><br/>

## Load Balances for Summer and Winter Design Days
```{image} ../_static/hvac1/hvac1_5.png
:width: 100%
:align: center
```
<br/><br/>

## Double check Grasshopper blocks
```{image} ../_static/hvac1/hvac1_6.png
:width: 100%
:align: center
```
<br/><br/>

## Peak Heating and Cooling Plots
The left side plots show the cooling and heating load on the hottest and coldest days of the year. The right side plots **double check that these plots have the right inputs and their interpretation**.

```{image} ../_static/hvac1/hvac1_7.png
:width: 100%
:align: center
```
<br/><br/>

## Set Heating and Cooling Setpoints
The heating setpoint determines at what temperature the active heating system turns on. The cooling setpoint determines at what temperature the active cooling system turns on. This replicates the logic and behgavior of a thermostat. A heating setpoint of 21 C and a cooling setpoint of 25 C is reasonable for human comfort.

```{image} ../_static/hvac1/hvac1_8.png
:width: 100%
:align: center
```
<br/><br/>

## Vary Setpoints and Compare Calculated Peak Loads
Note the peak heating and cooling loads for your chosen setpoints. Record them in a panel. Then change your setpoints and compare the calculated peak loads. How do they change? Does this align with your expectations?

```{image} ../_static/hvac1/hvac1_9.png
:width: 100%
:align: center
```
<br/><br/>
