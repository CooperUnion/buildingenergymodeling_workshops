# Multi-Zone-Part 1: 

## Setting Multiple Zones
Bring up a Brep component. Right click on the Brep component to reveal a dropdown and select "Set Multiple Breps."
```{image} ../_static/multizone/multizone2_1.png
:width: 100%
:align: center
```
<br/><br/>

In Rhino, select the closed polysurfaces you wish to be your desired zones. Then press Enter when done.
```{image} ../_static/multizone/multizone2_2.png
:width: 100%
:align: center
```
<br/><br/>

The zones referenced in the Brep will show up red. Check if the Brep is set by clicking on the Brep (turns green), hovering mouse over Brep (list of referenced Breps), or clicking on "Manage Brep collection."
```{image} ../_static/multizone/multizone2_3.2.png
:width: 100%
:align: center
```
<br/><br/>

Connect the Brep to a new component called "HB Intersect Solids." For multi-zone/room energy models, this is a must have. It takes in a list of HB Rooms closed Breps (polysurfaces) and recognizes any and all shared faces between the rooms. Attach a "Boolean Toggle" as a way to run the component. Set to True. Turn the preview off on "IntSolid" for better visualization in the next steps.
```{image} ../_static/multizone/multizone2_4.png
:width: 100%
:align: center
```
<br/><br/>

Bring up a "List Item" and "Number Slider." Select both to copy and paste another set. 
```{image} ../_static/multizone/multizone2_5.png
:width: 100%
:align: center
```
<br/><br/>

Right-click on the slider and set the slider type to Integers. The values of the slider can be adjusted using the min and max. In this case, the sliders are used to choose between multiple rooms. This model contains a house and a garage so the default 0 and 1 is okay. For models with more than 2 rooms, adjust the bounds accordingly. Do the same for the other set.
```{image} ../_static/multizone/multizone2_5.3.png
:width: 100%
:align: center
```
<br/><br/>

Connect the Index to the “i” input of the Item component. Slide the Index to 0. Do the same to the other set but slide to 1. These represent the two different rooms in the Rhino model. Then, wire the IntSolid’s output “int_rooms” to the “L” inputs of the two Item’s. To wire from the same output, hold down Shift key and drag to the input.
```{image} ../_static/multizone/multizone2_6.png
:width: 100%
:align: center
```
<br/><br/>

Check if the rooms/zones are properly defined by clicking on each Item. The output of the Item is a Brep or a geometry which can be connected to other components’ inputs. Wire the Brep of the house to the _geometry input of "Incident Radiation" like in [5.2.6](##5.2.6.-Set-Analysis-Period-for-Summer-Design-Day)
```{image} ../_static/multizone/multizone2_7.2.png
:width: 100%
:align: center
```
<br/><br/>

Connect the House Brep (Top Item) back to the HB RoomSolid from earlier. Remember the hold down Shift key when wiring from the same output. It is also a good habit to name the room because complex models will have multiple different rooms for different purposes.
```{image} ../_static/multizone/multizone2_8.png
:width: 100%
:align: center
```
<br/><br/>
