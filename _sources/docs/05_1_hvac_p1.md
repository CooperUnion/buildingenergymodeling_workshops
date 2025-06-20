# Evaluating HVAC Systems Part 1

## Packaged gas furnace and AC unit
1. Open your shoebox with shade model from the [previous workshop](04_psvdgn.md#evaluating-passive-hvac-design-strategies) in Openstudio.
```{image} ../_static/hvac1/hvac1_1.png
:width: 100%
:align: center
```
<br/><br/>

2. Run a simulation. This will serve as the baseline.
```{image} ../_static/hvac1/hvac1_2.png
:width: 100%
:align: center
```
<br/><br/>

3. Save the osmod file as 'shoebox_gas_ac.osm'.
```{image} ../_static/hvac1/hvac1_3.png
:width: 100%
:align: center
```
<br/><br/>

4. Go to HVAC systems. Click on the green '+' icon. Choose the first HVAC system on the list 'packaged rooftop unit'.
```{image} ../_static/hvac1/hvac1_4.png
:width: 100%
:align: center
```
<br/><br/>

5. On the window on the right. Search for 'thermal'. Drag and drop the 'Space_tzone' onto the Drag from library box on the HVAC network.
```{image} ../_static/hvac1/hvac1_5.png
:width: 100%
:align: center
```
<br/><br/>

6. Now let's take a look at the Layout of the HVAC system. It uses a DX cooling coil, which is similar to an air-conditioning unit. If you click on the coil you can see it has a Rated COP of 3. It means that with 1 unit of electricity, it can move 3 units of heat for cooling. We will keep the rest of ther parameters as default.
```{image} ../_static/hvac1/hvac1_6.png
:width: 100%
:align: center
```
<br/><br/>


7. It uses a gas furnace as its heating coil. Click on the heating coil and you can see the Gas Burner Efficiency (it is essentially the AFUE) is 0.8. Change the 'Fuel Type' to 'Natural Gas'.
```{image} ../_static/hvac1/hvac1_7.png
:width: 100%
:align: center
```
<br/><br/>

8. The system also has fresh air intake.
```{image} ../_static/hvac1/hvac1_8.png
:width: 100%
:align: center
```
<br/><br/>

9. It is a very simple system with fresh air intake. It has a constant air flow fan and supply. The system is going to operate once the zone temperature is below/above heating/cooling setpoint and cools the zone air temperature to meet the setpoint temperature. Run the simulation.
```{image} ../_static/hvac1/hvac1_9.png
:width: 100%
:align: center
```
<br/><br/>

10. Open the baseline simulation and compare the two results side by side. You will realise 'shoebox_gas_ac.osm' uses more energy. You can also see that the cooling energy consumption is lower while the heating is higher. Why is that so?
```{image} ../_static/hvac1/hvac1_10.png
:width: 100%
:align: center
```
<br/><br/>

11. The reason is a gas furnace was used for heating. The AFUE is 0.8 as a result more energy is used for heating. The AC has a rated COP of 3, as a result the cooling energy is much lower than ideal air load. Ideal air loads has no system, it is the actual thermal load that needs to be removed.

## Packaged heat pump
1. Save the file as 'shoebox_heat_pump.osm'. 
```{image} ../_static/hvac1/hvac1_11.png
:width: 100%
:align: center
```
<br/><br/>

2. Remove the 'Packaged Rooftop Air Conditioner'. In the HVAC systems tab. Click on the 'x' icon.
```{image} ../_static/hvac1/hvac1_12.png
:width: 100%
:align: center
```
<br/><br/>

3. Add 'Packaged Rooftop Heat Pump'.
```{image} ../_static/hvac1/hvac1_13.png
:width: 100%
:align: center
```
<br/><br/>

4. The system is very similar to the previous system. The main difference is for heating. Heating is now done with heat pump with a complimentary electric heating coil. The cooling and heating coil has a Rated COP of 3 and 5. The electric heating coil has an efficiency of 1.0. That means all input electricity to the electric coil heater becomes heat. Add the thermal zone to the system layout as shown in step 5 of the [previous section](#packaged-gas-furnace-and-ac-unit). 
```{image} ../_static/hvac1/hvac1_14.png
:width: 100%
:align: center
```
<br/><br/>

5. Run the simulation as shown in step 9 of the [previous section](#packaged-gas-furnace-and-ac-unit). Compare the results with the previous 'shoebox_gas_ac.osm'. You can see that the HVAC energy consumption has an overall reduction of 2.3x. Heat pump is a more efficienct way of heating and cooling. If coupled with renewable electricity it will drastically reduce emissions as compared to combustion-based heating systems. 
```{image} ../_static/hvac1/hvac1_15.png
:width: 100%
:align: center
```
<br/><br/>

## Remove fresh air intake
1. Save the file as 'shoebox_heat_pump_no_fresh.osm'. 

2. In the HVAC systems tab. Select the 'Packaged Rooftop Heat Pump'. 'AirLoopHVAC:OutdoorAirSystem' and click on 'x' to delete the fresh air intake.
```{image} ../_static/hvac1/hvac1_16.png
:width: 100%
:align: center
```
<br/><br/>

3. Once you deleted the fresh air intake. The layout should look like this.
```{image} ../_static/hvac1/hvac1_17.png
:width: 100%
:align: center
```
<br/><br/>

4. You can run the simulation again and see how did that affected the HVAC energy consumption. By removing the fresh air intake. The HVAC energy consumption reduce by ~9x. Conditioning fresh air intake is very energy intensive as compared to just recirculating air. However from our experience with Covid-19, it is clear that ventilation is a life and death matter!!
```{image} ../_static/hvac1/hvac1_18.png
:width: 100%
:align: center
```
