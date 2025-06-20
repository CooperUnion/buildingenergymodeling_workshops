# Shoebox Model-Part 3: OpenStudio Model Schedules

## Convert IFC to OpenStudio Model
1. In FreeCAD go to the ArchEng Workbench. Make sure you have installed the workbench by following the [getting started guide](02_shoebox.md#install-the-architecture-engineering-workbench)

2. Click on the ifc2osmod button. Specify your ifc file and where you want to store your osmod file. Then click on 'Convert to osmod'.
```{image} ../_static/shoebox3/shoe3_22.png
:width: 100%
:align: center
```
<br/><br/>

3. Once the conversion is done. A window will pop up telling you where is the osmod file.
```{image} ../_static/shoebox3/shoe3_23.png
:width: 100%
:align: center
```
<br/><br/>


##  Specify the weatherfile
1. Open the shoebox.osm file with openstudio. Go to File -> Open and choose shoebox.osm.
```{image} ../_static/shoebox3/shoe3_1.png
:width: 100%
:align: center
```
<br/><br/>

2. Check the geometry tab to make sure everything is imported.
```{image} ../_static/shoebox3/shoe3_2.png
:width: 100%
:align: center
```
<br/><br/>

3. We will simulate the shoebox model in New York City. Download the weatherfile <a href="https://climate.onebuilding.org/WMO_Region_4_North_and_Central_America/USA_United_States_of_America/NY_New_York/USA_NY_New.York-Downtown.Manhattan.Heli.720553_TMYx.2009-2023.zip" target="_blank">here</a>. 
    - You can get updated weatherfiles around the world <a href="https://climate.onebuilding.org/" target="_blank">here</a>.
    - Download and unzip the folder.

4. Go to the Site tab and set the weatherfile as shown below.
```{image} ../_static/shoebox3/shoe3_3.png
:width: 100%
:align: center
```
<br/><br/>
5. Set the design day information by clicking on Import From DDY.
```{image} ../_static/shoebox3/shoe3_4.png
:width: 100%
:align: center
```

## Specify the schedules of the loads
1. Go to the Spaces tab and click on the Airflow. Under the Design Specification Outdoor Air enter 4 Outdoor Air Flow Air Changes per Hour
```{image} ../_static/shoebox3/shoe3_5.png
:width: 100%
:align: center
```
<br/><br/>

2. Go to the Loads tab. On the right window click on the Library tab, in the search bar type in 'Office Work Occ'. Drag and drop the Office Work Occ schedule onto the People Definition 1 schedule parameter as shown below. Make sure the mouse shows a '+' sign before you release the drag.
```{image} ../_static/shoebox3/shoe3_6.png
:width: 100%
:align: center
```
<br/><br/>

3. Do the same for Activity Schedule -> Office Activity, Lights -> Office Bldg Light, Electric Equipment -> Office Bldg Equip. 
```{image} ../_static/shoebox3/shoe3_8.png
:width: 100%
:align: center
```
<br/><br/>

4. Go to the Schedules tab. In the schedules window click on the Schedules tab. Click on the Office Bldg Equip schedule and click on the Default.
```{image} ../_static/shoebox3/shoe3_9.png
:width: 100%
:align: center
```
<br/><br/>

5. We can see on the middle window the line shows the schedule of a default day. You can double click on the line to cut a segment. Pull horizontal line up or down to adjust the schedule value, you can also type in the value. Pull the vertical line to adjust the timing.
```{image} ../_static/shoebox3/shoe3_10.png
:width: 100%
:align: center
```
<br/><br/>

6. On the right calendar window. We can see that the days colored in light blue are assigned the Default schedule. The purple colored days are assigned Priority 1 and dark blue are assigned Priority 2.  
```{image} ../_static/shoebox3/shoe3_11.png
:width: 100%
:align: center
```
<br/><br/>

7. Click on the Priority 1 schedule. You can see that the schedule is for the whole year and only apply to Sundays.
```{image} ../_static/shoebox3/shoe3_12.png
:width: 100%
:align: center
```

## Cooling thermostats schedules
1. Go to the 'Thermal Zones' tab. We only have one zone in this model. The 'Cooling Thermostat Schedule' and 'Heating Thermostat Schedule' are empty. So we need to create a schedule for it.
```{image} ../_static/shoebox3/shoe3_13.png
:width: 100%
:align: center
```
<br/><br/>

2. Go to the 'Schedules' tab. Click on 'Schedules' in the window. Click on the '+' button at the bottom. A window will pop up. At the 'Schedule Type' parameter choose 'Temperature'. There are many temperature schedule, choose the last one that has a lower limit of 0degC and upper limit of 100degC.
```{image} ../_static/shoebox3/shoe3_14.png
:width: 100%
:align: center
```
<br/><br/>

3. Change the name of the schedule to 'cooling setpoint'. Click on the Default. Double click on the schedule line to create a cut as shown below. Pull it and place it at 8am.
```{image} ../_static/shoebox3/shoe3_15.png
:width: 100%
:align: center
```
<br/><br/>

4. Double click on the line again to create another cut at 18:00. Hover on the first segment and input the value 50.
```{image} ../_static/shoebox3/shoe3_16.png
:width: 100%
:align: center
```
<br/><br/>

5. Hover on the second segment and put in value 25 degC. Hover on the third segment and put in 50 degC. This schedule means the HVAC will cool the space to 25C from 8:00 to 18:00. From 0:00 to 8:00 and 18:00 to 24:00, it will turn on cooling only if the air temperature rise above 50degC, which will not happen. It is essentially setting cooling to not turn on.
```{image} ../_static/shoebox3/shoe3_17.png
:width: 100%
:align: center
```
<br/><br/>


6. Click on the 'Run Period Profiles +'. Make a New Profile Based on: 'Default Day Schedule' and click Add. A 'Priority 1' schedule tab will appear.  
```{image} ../_static/shoebox3/shoe3_18.png
:width: 100%
:align: center
```
<br/><br/>

7. Click on 'Priority 1' schedule. Apply to Saturday and Sunday. Click on the 2nd segment and enter the value 50. Double click on the cut lines to remove them.
```{image} ../_static/shoebox3/shoe3_19.png
:width: 100%
:align: center
```
<br/><br/>

8. Repeat steps 2-7 to create a 'heating setpoint' schedule. For heating, from 0:00-8:00 set to 18degC, from 8:00-18:00 set to 24degC, and 18:00-24:00 set to 18degC. For Priority 1 the saturday and sunday schedule, set it to 18 degC.
```{image} ../_static/shoebox3/shoe3_20.png
:width: 100%
:align: center
```
<br/><br/>

9. Go to Thermal Zones tab. Assign the cooling setpoint schedule to the Cooling Thermostat Schedule and heating setpoint schedule to Heating Thermostat Schedule. Tick the Turn On Ideal Air Loads.
```{image} ../_static/shoebox3/shoe3_21.png
:width: 100%
:align: center
```
<br/><br/>

10. Next we will move on to define the construction of the building envelope. 
