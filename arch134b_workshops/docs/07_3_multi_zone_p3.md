# Multi-Zone Part 3:
## Generate Peak Load Monthly Charts for Multiple-Zones 
1. Reference this section of the Grasshopper.
```{image} ../_static/multizone/multizone4_1.1.png
:width: 100%
:align: center
```
<br/><br/>

2. Add a List Item and Slider to choose to view between generating a house monthly chart or a garage monthly chart. Connect the hb_objs from Border Shades to the L input of the List Item component.
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
4. Use HB Read Zone Sizing (ReadZSZ) to evaluate the peak loads per zone. Connect a panel to the zone_names to see how the values appear on the panels connected to zone_peak_cool and zone_peak_heat.
```{image} ../_static/multizone/multizone4_4.png
:width: 100%
:align: center
```
<br/><br/>

## Generate 8760 Maps
