# Polydome

## Author & Date 

Jicheng Shi, December 2021.

## Brief Description 

CO2 and occupancy from an entire building, called Polydome. The time-series dataset is composed of continuous features. 

## Long Description 
Polydome is a freestanding $600 m^2$ single-zone building on the EPFL campus. It is regularly used for lectures/exams and accommodates up to 200 people.

In the Polydome, a roof-top heat pump, AERMEC RTY-04, serves as an HVAC system. It can execute ventilation (~2.4kW), heating (~6kW), and cooling (~4.6kW). The heat pump collects both the external air and the return air from the room side. When the heat pump is open, it keeps pumping the air to the room for ventilation. At the same time, it can heat or cool the air before pumping. The flow rate of the ventilation air is roughly constant.

Four air quality sensors are installed evenly at four corners. The sensor distribution can be found in Folder/zwave_overview.jpg. The people in the building are counted by Jicheng Shi, not by other advanced sensors. The reason is that we hope to quickly construct the occupancy measurement by CO2 levels with short-term data and without some complex sensors, e.g., cameras. But the manual counting leads to some errors. For example, on the night of Friday, 10-12-2021, the building should be occupied (maybe by a student party)  based on the CO2 levels. But I had already left. 

**When was it collected?** From December 6, 2021, to December 14, 2021.

**Sampling period**: 15 minutes.

## Folders/Files

:file_folder: **data**: contains the data files.

``raw_06-12-2021_14-12-2021.csv``: an original dataset from the local database

``raw_06-12-2021_14-12-2021.mat``: a structure ``exp`` in Matlab that contains the same data as the '.csv' file.

:file_folder: **docs**: contains some pictures to illustrate the system architecture.

## Measurements

``time_str`` \[GMT-1\]: date and time of the current measurements. Note it records the time of Europe/Zurich.

``time`` \[GMT-1\]: datenum(time_str) in Matlab. Note it records the time of Europe/Zurich.

``co2_1`` \[ppm\]: CO2 level measured by one air quality sensor

``co2_2`` \[ppm\]: CO2 level measured by one air quality sensor

``co2_3`` \[ppm\]: CO2 level measured by one air quality sensor

``co2_4`` \[ppm\]: CO2 level measured by one air quality sensor

``supply_flow`` \[*10m^3/h (this value should be multiplied by 10 when transformed to 'm^3/h' )]: the supply air flow rate of the heat pump on the room side.


