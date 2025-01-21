The Eel River PRMS Model was calibrated to provide unimpaired modeled flow estimates at a subbasin scale and has a model run time from October 1, 1981 to March 31, 2022. Files generally needed for a PRMS model to run include a control file, data file, parameter file, model executable, and batch file. Executing the model per the directions outlined in this read me will produce daily flows for the entire time period.

The control file is called 'eel_river_control.control' 
The data file is called 'eel_river_data.data'
The parameter file is called: 'eel_river_param.params'
			 
The model executable is in the bin folder of the GitHub repository.
The batch file is called 'run.bat'

Directions on how to run the model:
Download and extract the GitHub repository, preferably directly to your C drive. Navigate to the PRMS subfolder. Run the model by double clicking on 'run.bat.' A prompt will show up and the model will take some time to execute. Once the model is finished executing, it will produce two CSVs, eel_subbasins.sub_cfs.csv and eel_subbasins.sub_inq.csv. In each csv, the column headers include Date followed by Subbasin IDs. Unimpaired modeled flow estimates for each subbasin are reported in daily average cubic feet per second (cfs).

eel_subbasins.sub_cfs.csv is the cumulative subbasin flow at the outlet of each subbasin. 
eel_subbasins.sub_inq.csv is the individual subbasin flow contribution for each subbasin. 


PRMS is open-sourced, publicly available, and  maintained by the United States Geological Survey (USGS). PRMS is well documented by Markstrom, Regan, and others (2008) from the USGS. The model documentation, manual, software releases, and updated notes and tables from new releases can be found at the following URL:
https://www.usgs.gov/software/precipitation-runoff-modeling-system-prms
