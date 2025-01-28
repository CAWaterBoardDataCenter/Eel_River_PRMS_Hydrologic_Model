The Precipitation Runoff Modeling System (PRMS) is a spatially distributed physical-based model that uses terrain (i.e., elevation and slope), vegetation/land use, and meteorological data to simulate hydrological processes of a watershed, such as surface and groundwater flow, evapotranspiration, soil moisture dynamics, and streamflow. Inputs for PRMS include precipitation in the form of rain and snow, minimum and maximum temperature, and short-wave solar radiation. A watershed model domain in PRMS is represented by a grid that consists of square shaped cells that are more technically known as hydrologic response units (HRUs). An HRU is designated as either land, lake, swale, or inactive. Each HRU holds hydrologic and physical inputs, such as surface elevation, slope, and aspect; vegetation type and cover; land use; distribution of precipitation, temperature, and solar radiation; soil morphology and geology; and flow direction. The Eel River PRMS Model was developed with a 300m x 300m (HRU size) model grid resolution and was calibrated to provide unimpaired modeled flow estimates. The model has a total of 121 subbasins and a model start and end time from 10/1/1981 to 03/31/2022, respectively. The GIS subfolder of this GitHub repository has a geopackage with boundary conditions and model feature class layers. The following is a reference guide for the feature class layers within the geopackage. 

Eel_River_pour_points
	Points at the outlets of modeled subbasins 

Eel_River_gages
	Gages identified in the watershed

Eel_River_model_grid
	300m x 300m model grid that holds all Hydrologic Response Units (HRUs). Attributes include:
		-HRU_TYPE – This is the model active/inactive attribute. 0 means inactive. 1 means active. Query the model grid in GIS to only show the active HRUs.
		-SUB_BASIN – Subbasin_ID. Associated with the model output csv discussed in the section below.
		-SUB_DOWN – Immediate downstream subbasin 

Eel_River_model_subbasins
	Model grid dissolved into subbasins. Attributes include:
		-SUB_BASIN – This is the subbasin ID. Associated with the model output csv produced by the model runs discussed below.
		-SUB_DOWN – Immediate downstream subbasin

Eel_River_watershed_boundary
	Watershed boundary shapefile 

The coordinate system is in projected coordinate system NAD 1983 UTM Zone 10N (EPSG: 26910).


The Eel River PRMS Model was calibrated with an emphasis on spring recession and dry season baseflows.

Running the Eel River Model:
-Navigate to the PRMS subfolder and follow the directions outlined in READ_ME_1.txt to execute the model and simulate daily optimized unimpaired modeled flows by subbasin. Results from an executed model run are already included in this subfolder in the form of model output csv files.