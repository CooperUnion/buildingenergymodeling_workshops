# Multi-Zone Part 3: Energy Simulation and Visualization of Results
## Generate Peak Heating and Cooling Plots for Multiple-Zones 
1. Reference this section of the Grasshopper.
```{image} ../_static/multizone/multizone4_1.1.png
:width: 100%
:align: center
```
<br/><br/>

2. Add a List Item and Slider to choose to view between generating a house peak plot or a garage peak plot. Connect the hb_objs from Border Shades to the L input of the List Item component.
```{image} ../_static/multizone/multizone4_2.png
:width: 100%
:align: center
```
<br/><br/>

3. These should be the results. On the left is house, on the right is garage. 
```{image} ../_static/multizone/multizone4_3.png
:width: 100%
:align: center
```
<br/><br/>

## Alternative Method: Evaluating Peak Loads Per Zone
4. Use HB Read HVAC Sizing (ReadHVAC) to evaluate the peak loads per zone. Connect a panel to the zone_names to see how the values appear on the panels connected to zone_peak_cool and zone_peak_heat.
```{image} ../_static/multizone/multizone4_4.png
:width: 100%
:align: center
```
<br/><br/>

## Generate 8760 Plot and Monthly Loads Plot for Multi-Zones
5. Use this area.
```{image} ../_static/multizone/multizone4_5.1.png
:width: 100%
:align: center
```
<br/><br/>

6. Recreate these components (HB Color Rooms) and connections below. For the Number slider, change to integer-type and set range from 0 to 1, referring to the two zones: house and garage.
```{image} ../_static/multizone/multizone4_6.png
:width: 100%
:align: center
```
<br/><br/>

7. Connections to L input of List Item component and _data of HB Color Rooms (ColorRooms) are to the cooling output of HB Read Room Energy Results. The _rooms_model input of HB Color Rooms is connected to model output of HB Model.
```{image} ../_static/multizone/multizone4_5.png
:width: 100%
:align: center
```
<br/><br/>

## Visualization of Results
8. Reference location of the generated plots.
```{image} ../_static/multizone/multizone4_7.png
:width: 100%
:align: center
```
<br/><br/>

9. Peek the bottom of the 8760 Plot. It provides information about what the contents of the plot are comprised of. Since our data was connected to cooling, the type indicates it contains Zone Ideal Loads Supply Air Total Cooling Energy. The System tells us which zone we are looking at, in this case, the house.
```{image} ../_static/multizone/multizone4_8.png
:width: 100%
:align: center
```
<br/><br/>

10. Move the slider to switch to the other zone and watch the 8760 plot change. Check the details of type and System again.
```{image} ../_static/multizone/multizone4_9.png
:width: 100%
:align: center
```
<br/><br/>

11. Disconnect the cooling output from List Item and HB Color Rooms. Try visualizing heating for the house and garage zones. 
```{image} ../_static/multizone/multizone4_12.png
:width: 100%
:align: center
```
<br/><br/>

```{image} ../_static/multizone/multizone4_11.png
:width: 100%
:align: center
```
<br/><br/>

12. View the Rhino Model from Top View. Notice how the zones for the house and garage are colored. The HB Color Rooms (ColorRooms) component breaks down the total EUI per Zone/Room. 
```{image} ../_static/multizone/multizone4_10.png
:width: 100%
:align: center
```
<br/><br/>
