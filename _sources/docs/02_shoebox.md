# Shoebox Model

A shoebox model is a simplified, usually rectangular building used for pre-design to early design performance evaluation. With a simplified model, you can adjust different architectural parameters, e.g. windows size, constructions orientation, to understand how the performance changes with these adjustments. In this tutorial, we will model a 5m x 5m x 5m box in FreeCAD and perform an ideal air load simulation using Openstudio. 

## FreeCAD
1. Install FreeCAD==1.0.0. Follow the instructions here according to you OS <a href="https://www.freecad.org/downloads.php" target="_blank">here</a>.

2. Open FreeCAD. At the startup screen you can choose any of the themes. The tutorial series will use the FreeCAD classic theme.
```{image} ../_static/start/start1.png
:width: 100%
:align: center
```
<br/><br/>
3. In the next screen, under the New File section choose the BIM/Architecture workbench. 
```{image} ../_static/start/start2.png
:width: 100%
:align: center
```
<br/><br/>
4. Right click on your screen and choose your navigation style. The tutorial series uses the blender navigation style.
```{image} ../_static/start/start3.png
:width: 100%
:align: center
```
<br/><br/>
5. Go to the menu on top Edit -> Preferences ... -> Draft -> Grid and snapping. We are using FreeCAD for architecture modeling. We will change the grid spacing to 1000mm.
```{image} ../_static/start/start4.png
:width: 100%
:align: center
```
<br/><br/>
6. Turn on the Grid Snap and Snap Dimension snapping toggle on the BIM workbench as shown below.
```{image} ../_static/start/start5.png
:width: 100%
:align: center
```
<br/><br/>
7. In the BIM workbench, click on the Manage Ifc Properties icon. In the window you will be able to see a file path to put custom Psets csv.
```{image} ../_static/start/start6.png
:width: 100%
:align: center
```
<br/><br/>

8. Download the <a href="https://github.com/chenkianwee/ifc2osmod_gendgn_egs/archive/refs/heads/main.zip" target="_blank">zip file</a>. Unzip the file. Go to csv -> CustomPsets.csv, copy and paste this file into the file path shown in the previous step.
- for windows users, your file path is probably something like this 'C:\\Users\some_user_name\AppData\Roaming\FreeCAD\BIM'. If you go to the path you will not be able to see the 'AppData' as it is a hidden folder. You would want to turn on you 'Hidden items' in order for you to find the 'AppData' as shown in the image below.
- if the 'BIM' folder is not there create a new folder called 'BIM' and copy and paste the csv file into the folder.
```{image} ../_static/start/start17.png
:width: 100%
:align: center
```
<br/><br/>

9. Change the Start up workbench to BIM. Go to Edit -> Preferences -> Workbenches -> Available Workbenches
```{image} ../_static/start/start7.png
:width: 100%
:align: center
```
<br/><br/>

### Install the Architecture Engineering Workbench
1. In FreeCAD go to Edit -> Preferences.
```{image} ../_static/start/start8.png
:width: 100%
:align: center
```
<br/><br/>

2. In the preferences window select Addon Manager -> Addon manager options. Under the Custom repositories click on the '+' sign. Fill in the following details and press apply:
```
- Repository URL: https://github.com/chenkianwee/ArchEng_Workbench
- Branch: master
```
```{image} ../_static/start/start9.png
:width: 100%
:align: center
```
<br/><br/>

3. Go to Tools -> Addon manager.
```{image} ../_static/start/start10.png
:width: 100%
:align: center
```
<br/><br/>

4. In the Addon manager window. For the Filter parameter, change it to Workbench, Not installed. In the search bar search for 'archeng'. You should be able to see the ArchEng Workbench.
```{image} ../_static/start/start11.png
:width: 100%
:align: center
```
<br/><br/>

5. Install the workbench. After installation you will be asked to restart FreeCAD.
```{image} ../_static/start/start12.png
:width: 100%
:align: center
```
<br/><br/>

6. Once you restart FreeCAD. Go to the workbench dropdown list and choose ArchEng workbench. Then click on the InstallDependencies button.
```{image} ../_static/start/start13.png
:width: 100%
:align: center
```
<br/><br/>

7. You will be asked to install the dependencies. Click on Yes.
```{image} ../_static/start/start14.png
:width: 100%
:align: center
```
<br/><br/>

8. This will take some time. Wait for ~5mins, depending on the speed of your computer and internet connection (you must be connected to the internet). Once done, a message will pop up telling you to restart FreeCAD. Manually close FreeCAD and open it again.
```{image} ../_static/start/start15.png
:width: 100%
:align: center
```
<br/><br/>

9. Once restarted, go to the ArchEng workbench and click on ifc2osmod. You should see a window pop up. You have successfully installed the workbench. Close the window and move on to next section of this guide.
```{image} ../_static/start/start16.png
:width: 100%
:align: center
```
<br/><br/>

## OpenStudio Application for simulation and GIMP and Inkscape for visualization
1. Install OpenStudio Application==1.8.0 <a href="https://github.com/openstudiocoalition/OpenStudioApplication/releases/tag/v1.8.0" target="_blank">here</a>. Follow the instructions here according to your OS <a href="https://openstudiocoalition.org/getting_started/getting_started/" target="_blank">here</a>

2. Install Inkscape==1.4 <a href="https://inkscape.org/release/inkscape-1.4/" target="_blank">here</a> for doing vector illustration and Gimp==3.0.0 <a href="https://www.gimp.org/downloads/" target="_blank">here</a> for working with raster images.
