# Multi-Zone Part 2: Garage Zone
## Setting Garage Zone
1. Wire the Item of the Garage to a new HB Room from Solid. Label it “Garage.” Bring up a HB Apply Load Values in order to assign a program to the garage. Set conditioned to True. 
```{image} ../_static/multizone/multizone3_1.1.png
:width: 100%
:align: center
```
<br/><br/>

2. From the BldgPrograms, Warehouse is the closest option to a garage. Read the list of warehouse programs. Use a List Item and Number Slider to select a specific one that applies. Create a Panel with the warehouse program (shortcut: right-click on the output and “Copy Data Only” to paste onto a panel) and wire it to ApplyLoads. 
```{image} ../_static/multizone/multizone3_2.5.png
:width: 100%
:align: center
```
<br/><br/>

3. Most residential garages are wood-framed, and given the house is a post 2019 modern-build, so should the garage. 
```{image} ../_static/multizone/multizone3_3.1.png
:width: 100%
:align: center
```
<br/><br/>

4. Since this model only has a house and garage, it is easy to create two panels and separately assign construction sets. However, for more complex models with multiple rooms that have the same set or bldgprogram, you can use a Relay component to wire more efficiently.  
```{image} ../_static/multizone/multizone3_4.1.png
:width: 100%
:align: center
```
<br/><br/>

## Solve Adjacencies for Multi-Zones
5. Disconnect IdealAir from AddSubface and add the components boxed in red. HB Solve Adjacencies (SolveAdj) is used since we have a series of HB Rooms that are adjacent and/or share matching faces. 
```{image} ../_static/multizone/multizone3_5.1.png
:width: 100%
:align: center
```
<br/><br/>

## Set Adiabatic for Multi-Zones
In this model, we will assume there is limited to no heat transfer between the house and the garage. This is due to the fact that most garages are typically constructed well with proper insulation such that it significantly slows heat exchange. 

6. With this in mind, set Adiabatic to True. An adiabatic process, in thermodynamics, is when no heat is transferred in or out of a system such that Q = 0.


## Check Multi-Zones
7. Check whether the zones are properly assigned by bringing up a HB Label Rooms which automatically labels the zones in the Rhino viewport. For the Aperture and Shade components, add the new respective window and roof geometries from the garage model. You may need to select all of the geometries again, including from the house model. 
```{image} ../_static/multizone/multizone3_6.1.png
:width: 100%
:align: center
```
<br/><br/>
