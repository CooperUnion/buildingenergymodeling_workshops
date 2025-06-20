# Specifying Packaged HVAC Systems Part 1

## Get the required capacity 
1. Open your shoebox model from the [previous workshop](02_shoebox.md#shoebox-model) in Openstudio.
```{image} ../_static/spec1/spec1_1.png
:width: 100%
:align: center
```
<br/><br/>

2. Run the simulation. 
```{image} ../_static/spec1/spec1_2.png
:width: 100%
:align: center
```
<br/><br/>

3. Go to the 'District Cooling Peak Demand' and 'District Heating Water Peak Demain'. Identify the highest consumption. According to the graph below, the peak demand for cooling is 3.9kW and heating is 9kW. 
```{image} ../_static/spec1/spec1_3.png
:width: 100%
:align: center
```
<br/><br/>

4. Convert watts to BTU/hr and ton. 
```
P(BTU/hr) = 3.412141633 × P(W).
cooling BTU/hr = 3900 W x 3.412141633 = 13307 BTU/hr = 13 kBTU/hr
heating BTU/hr = 9000 W x 3.412141633 = 30709 BTU/hr = 31 kBTU/hr

cooling ton = 13 (kBTU/hr)/ 12 = 1.1 ton
heating ton = 31 (kBTU/hr)/ 12 = 2.6 ton
```

## Window units?
1. This is the heating and cooling capacity we are looking out for. We will search for our package unit at <a href="https://www.homedepot.com/b/Heating-Venting-Cooling/N-5yc1vZc4k8" target="_blank">home depot heating and cooling services</a>. Since our shoebox model is so small. Lets look at if we can get away with using a window unit for both heating and cooling.
```{image} ../_static/spec1/spec1_4.png
:width: 100%
:align: center
```
<br/><br/>

2. Our room is about medium size.
```{image} ../_static/spec1/spec1_5.png
:width: 100%
:align: center
```
<br/><br/>

3. A quick overview of the capacity. We need quite alot of heating and most window conditioner do not have heating or no sufficient heating.
```{image} ../_static/spec1/spec1_6.png
:width: 100%
:align: center
```
<br/><br/>

4. If you click on one of the option and look at the specification. You will see that most of the window units have no heating btu/hr rate.
```{image} ../_static/spec1/spec1_7.png
:width: 100%
:align: center
```
<br/><br/>


## Central air conditioning heat pump
1. Go to <a href="https://www.homedepot.com/b/Heating-Venting-Cooling/N-5yc1vZc4k8" target="_blank">home depot heating and cooling services</a>. Click on Central Air Conditioners.
```{image} ../_static/spec1/spec1_8.png
:width: 100%
:align: center
```
<br/><br/>

2. Click on the heat pump.
```{image} ../_static/spec1/spec1_9.png
:width: 100%
:align: center
```
<br/><br/>

3. I have selected the Best Seller MRCOOl unit that is 36 kBTU/hr as shown below.
```{image} ../_static/spec1/spec1_10.png
:width: 100%
:align: center
```
<br/><br/>

4. Click on the specifications. It satisfies both the heating and cooling capacity. Its cooling capacity is much higher than what is required. This means that when cooling, the machine is always running at partial load. It is inefficient.
```{image} ../_static/spec1/spec1_11.png
:width: 100%
:align: center
```

5. We can use this heat pump for heating and get a much smaller window units for cooling. As shown in the previous section.

6. My eventual selections are : 
- <a href="https://www.homedepot.com/p/MRCOOL-Universal-Series-Split-System-36-000-BTU-3-Ton-18-Seer-Heat-Pump-and-Air-Handler-230V-MDHP1836/327780345" target="_blank">central heat pump</a> 
- <a href="https://www.homedepot.com/p/LG-14-000-BTU-115V-Window-Air-Conditioner-Cools-700-sq-ft-with-Wi-Fi-Remote-Dehumidifier-and-in-White-LW1523ERSM/322847864" target="_blank">window unit</a>
- **When managing a project it is important to discuss with the HVAC engineer/contractor about the selection as they have more experience and knowledge.** The purpose of the exercise is to introduce you to the process and facilitate your discussion with the HVAC engineer/contractor.

7. Can you get a cheaper deal by selecting an electric furnace for heating and window unit for cooling?
