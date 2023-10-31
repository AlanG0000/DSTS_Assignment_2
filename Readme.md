DSTS Assignment 2
This project consists of the following files:
1. onpremises.ipynb
2. oncloud.ipynb
3. A tableau dashboard was made for this project which is available on the following link: https://public.tableau.com/app/profile/alan.gaugler/viz/DSTS_2/Delays?publish=yes

The dataset used for this project is a zip file of 60 zip files. Each of these 60 zip files contain flight data of US domestics flight for each month in the 5 year period from January 2014 to December 2018. Included are the following files:
1. A CSV file containing all the flight information in the US for a one-month period. This will contain several hundred thousand rows for each flight and 109 variables. Many of these variables are partially or mostly empty.
2. A ‘readme.html’ file which consists of the field names and a brief description of them.
The flight data for this project was made available at the following site. Permissions will be required to access it. The entire dataset is 1.5 GB in size, so it cannot be uploaded here.
https://ucstaff-my.sharepoint.com/:f:/g/personal/ibrahim_radwan_canberra_edu_au/Er0nVreXmihEmtMz5qC5kVIB81-ugSusExPYdcyQTglfLg?e=bNO312
Similar data can be collected at the Bureau of Transportation Statistics at the following link:
https://www.transtats.bts.gov/

The ‘onpremises.ipynb’ file can be downloaded from this repository and run on any personal computer with a notebook installed. This file was run and modified on Jupyterlab in the Anaconda environment in Windows 11 but can be run in any other notebook environment.
To run it, the following packages must be installed in your environment.
* Pathlib
* Zipfile
* Pandas
* Numpy
* Matplotlib
* Seaborn
Other libraries must also be imported. These are part of the Python installation and will be imported upon executing the code.

Running the code is straightforward.
Place the code in your desired working directory and confirm the working directory is set to where the code is placed. 
A subfolder called ‘zipped_flight_data’ needs to be created. 
All the zip files for each month (described above) need to be placed within this folder. 
Executing this program will create a new sub folder ‘flight_data’ in the working directory and place all the unzipped CSV files into this folder as well as one unzipped ‘readme.html’ file. 
Three files will be created from this program and placed into the working directory.
1. ‘combined_files.csv’ – This consists of the 20 most important variables for modelling for this dataset which is filtered for the 9 busiest origination and destination airports and the 5 most popular airlines.
2. 'combined_csv_v1.csv' – This is a modification of the dataset and the file ‘combined_files.csv’ in which all the categorical features are one-hot encoded, so it consists of many more columns. 
3. 'combined_csv_v2.csv' – This is similar to 'combined_csv_v1.csv', however the weather data for each date at the airport has been added. Collecting this weather data is described below.

Weather data must be downloaded from the following site:
https://www.ncei.noaa.gov/access/services/data/v1?dataset=daily-summaries&stations=USW00023174,USW00012960,USW00003017,USW00094846,USW00013874,USW00023234,USW00003927,USW00023183,USW00013881&dataTypes=AWND,PRCP,SNOW,SNWD,TAVG,TMIN,TMAX&startDate=2014-01-01&endDate=2018-12-31.
This consists of weather data from the weather stations nearest to the 9 busiest airports during the period of the flight data. In this case January 2014 to December 2018. If you are running this program for a different period of time, please collect the weather data for the appropriate period and site locations from the same website.
This describes the instructions for running this code on other machines. It should be very simple to execute.
 


