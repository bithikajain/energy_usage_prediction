
## Project Objective
The purpose of this project is to be able to predict energy comsumption for building based on four meter types: electricity, steam, hot water and chilled water.


### Methods Used
* Feature Engineering
* Gradient Boosting Decision Tree

### Technologies
* Python, matplotlib
* Pandas, jupyter
* Sklearn
* Seaborn
* LightGBM

![Energy usage](https://github.com/bithikajain/energy_usage_prediction/blob/master/images/REW_GLobalRenewableEnergyIsStatusPositive.png)

### Dataset description: 
We are given information of 1449 buildings, BUILDING_ID is a unique identifier across both the train and test datasets. 

**train_df** comprises of 20216100 observations and 4 characteristics.<BR />
   1. building_id - Foreign key for the building metadata.
   2. meter - The meter id code. Read as {0: electricity, 1: chilledwater, 2: steam, 3: hotwater}. Not every building has all meter types.
   3. timestamp - When the measurement was taken
   4. meter_reading - The target variable. Energy consumption in kWh (or equivalent). Note that this is real data with measurement error, which we expect will impose a baseline level of modeling error.
   
<BR />
Dependent variable:meter_reading depends on (independent variable) meter and time_stamp

**building_df** comprises of 1449 observations and 6 charecteristics <BR/>
   1. site_id - Foreign key for the weather files.
   2. building_id - Foreign key for training.csv
   3. primary_use - Indicator of the primary category of activities for the building based on EnergyStar property type definitions
   4. square_feet - Gross floor area of the building
   5. year_built - Year building was opened
   6. floor_count - Number of floors of the building
   
square_feet depends on the primary_use, year_built, floor_count

**weather_train** comprises of 139773 observations and 9 charecteristics <BR />

Weather data from a meteorological station as close as possible to the site.

1. site_id
2. air_temperature - Degrees Celsius
3. cloud_coverage - Portion of the sky covered in clouds, in oktas
4. dew_temperature - Degrees Celsius
5. precip_depth_1_hr - Millimeters
6. sea_level_pressure - Millibar/hectopascals
7. wind_direction - Compass direction (0-360)
8. wind_speed - Meters per second
