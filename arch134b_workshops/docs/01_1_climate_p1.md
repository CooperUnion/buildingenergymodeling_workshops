# Climate Analysis Part 1: Visualizing Weather Data with CBE Clima Tool

## Get weather file
1. Go to <a href="https://climate.onebuilding.org/" target="_blank">climate.onebuilding.org</a>. Go to North-Central America-Region 4 -> North America USA - United States of America.
```{image} ../_static/clima1/clima1_1.png
:width: 100%
:align: center
```
<br/><br/>

2. At the United States page. We will use 'ctrl+f' to search for 'manhattan'. It is the 13/14 search as shown below. Click on the link and download it.
```{image} ../_static/clima1/clima1_2.png
:width: 100%
:align: center
```
<br/><br/>

3. Unzip the file. You will see 7 files. We will only be using the data from the .epw file. Here is a brief description of the files.
- .clm: weather file for the simulation software ESP-r 
- .wea: weather file for the daylight simulation software daysim
- .PVSyst: weather file for the daylight simulation software PVsyst
- .ddy: design day file
- .rain: precipation data in m/hr if available
- .stat: energyplus weather statistics
```{image} ../_static/clima1/clima1_3.png
:width: 100%
:align: center
```

## Load weather file with CBE Clima Tool
1. Now we will go to the <a href="https://clima.cbe.berkeley.edu/" target="_blank">CBE Clima Tool</a>. At the page, click on 'Drag and Drop or Select an EPW file from your computer' and select the New York Manhattan file .epw file we downloaded.
```{image} ../_static/clima1/clima1_4.png
:width: 100%
:align: center
```
<br/><br/>

2. It will load the weather file as shown below.
```{image} ../_static/clima1/clima1_5.png
:width: 100%
:align: center
```
<br/><br/>

3. Go to the 'Climate Summary' tab. We can see a brief summary of the climate and the Köppen-Geiger climate classification. The <a href="https://en.wikipedia.org/wiki/K%C3%B6ppen_climate_classification#Overview" target="_blank">Köppen-Geiger climate classification</a> is a system that categorizes climates into 5 main groups based on temperature and precipitation patterns. New York is classified as Cfa, where C(Temperate), f(No dry season) and a(hot summer), which means it is a humid subtropical climate. 
```{image} ../_static/clima1/clima1_6.png
:width: 100%
:align: center
```
<br/><br/>

4. Scroll down and you will see the 'Heating and Cooling Degree Days' section. Adjust the HDD setpoint to 18 degC and CDD setpoint to 25 degC and press submit. Looking at the graph you will have a sense if the climate is a heating or cooling dominant climate. For the case of New York, it is obviously a heating dominant climate. 
- However it is important to note, CDD is not a good indication for how much cooling is required, as a majority of cooling is dehumidification which is not capture by the dry bulb temperature.
```{image} ../_static/clima1/clima1_7.png
:width: 100%
:align: center
```

## Temperature and humidity
1. Next we look at the 'Temperature and Humidity' tab. The Yearly Chart shows the temperature distribution throughout the year. You can click on the little book icon beside the chart to go to an explanation page. The grey band is the ASHRAE adaptive comfort band. If the temperatures fall within it, it means that 80%-90% of the occupants will feel comfortable at that temperature.
```{image} ../_static/clima1/clima1_8.png
:width: 100%
:align: center
```
<br/><br/>

2. You can zoom into the data by clicking and dragging on the graph as shown below.
```{image} ../_static/clima1/clima1_9.png
:width: 100%
:align: center
```
<br/><br/>

3. You can zoom out by clicking and dragging the bar below the graph. You can also reset the axes by clicking on the home icon. You can also turn on and off data by clicking on the legend.
```{image} ../_static/clima1/clima1_10.png
:width: 100%
:align: center
```
<br/><br/>

4. Next we look at the Daily Chart. It shows the condition of an average day of each month.
```{image} ../_static/clima1/clima1_11.png
:width: 100%
:align: center
```
<br/><br/>

5. Next we look at the Heatmap Chart. The x-axis is 365 days of the year and the y-axis is 24 hours of a day. The color represents the temperature.
```{image} ../_static/clima1/clima1_12.png
:width: 100%
:align: center
```

## Sun, wind, natural ventilation and outdoor comfort
1. In the Sun and Clouds tab. You will be able to see the sun path and the daily chart of the horizontal solar irradiation received. These information will be useful if you are thinking of deploying PV panels on your building.
```{image} ../_static/clima1/clima1_13.png
:width: 100%
:align: center
```
<br/><br/>

2. In the Wind tab. We can visualize both the wind speed and wind direction with the wind rose diagram. You can quickly see the predominant wind direction and magnitude of the wind speed.
```{image} ../_static/clima1/clima1_14.png
:width: 100%
:align: center
```
<br/><br/>

3. The Natural Ventilation tab allows the user to set a minimum and maximum air temperature range that is suitable for natural ventilation. Buildings can open windows and does not require HVAC. The above diagram, heat map shows when this condition is satisfied. The below diagram shows for each month what are the percentage of days the condition is satisfied. We can see that in New York, Spring and Autumn has very high natural ventilation potential if the range is between 10-24 degC.
```{image} ../_static/clima1/clima1_15.png
:width: 100%
:align: center
```
<br/><br/>

4. However, 10-24 degC feels like too big a range. Lets go back to Temperature and Humidity tab, and get the ASHRAE adaptive comfort 80% range, use the min and max temperature as the range for natural ventilation potential. The min = 17.4 degC and max = 24.4 degC.
```{image} ../_static/clima1/clima1_16.png
:width: 100%
:align: center
```
<br/><br/>

5. Now lets change the Natural Ventilation min/max to the ASHRAE adaptive comfort 80% band. The tool does not allow decimal place. So lets input 17 degC and 24degC. We can see the potential is reduced and the potential shifted to the summer season.
```{image} ../_static/clima1/clima1_17.png
:width: 100%
:align: center
```
<br/><br/>

6. Universal Thermal Climate Index (UTCI) is used for assessing Outdoor Thermal Comfort. Click on the Outdoor Thermal Comfort tab, looking at the UTCI thermal stress chart you can see when there is very high thermal stress outdoor. From May to Sep, high thermal stress is experience during day time. These are very useful information for designing outdoor spaces.
```{image} ../_static/clima1/clima1_18.png
:width: 100%
:align: center
```
<br/><br/>
