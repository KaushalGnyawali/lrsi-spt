# lrsi-spt
Landslide Resillient Slope Infrastructure - Spatial Planning Tool
Link:
https://arcg.is/1T59ie

For details about the research, please refer to and cite the following paper: 
Gnyawali, K., Dahal, K., Talchabhadel, R., & Nirandjan, S. (2023). Framework for rainfall-triggered landslide-prone critical infrastructure zonation. Science of The Total Environment, 162242.

The Google Earth Engine code is in GEE code files.
The rainfall indices, critical infrastructure spatial index and landslide susceptibility data layers are in LIMS_SPT_Layers.7z zipped package. 
For the landslide inventories, please contact the corresponding author: gnyawalikr@gmail.com.

The provided code is designed to perform landslide susceptibility mapping (LSM) using Earth Engine, Google's cloud-based platform for remote sensing and geospatial analysis. The code was written in JavaScript and uses the TAGEE library for terrain analysis.

### Setup
To use this code, you will need to have an Earth Engine account and have JavaScript API client libraries installed.

### Data Inputs
The code requires several data inputs:

- A shapefile or feature collection defining the study area boundary (boundary)
- A DEM raster image (demSRTM) obtained from the SRTM 30m dataset
- A raster image of rainfall data (rain) for the study area
- Two feature collections (slide and nslide) containing training data for landslides and non-landslides, respectively

### Processing Steps
- Loads the necessary libraries and data inputs
- Smooths the DEM with a Gaussian filter
- Performs terrain analysis on the DEM using TAGEE library
- Combines the terrain analysis results with rainfall data
- Divides the training data into two sets, for training and testing
- Samples the training data and selects the parameters
- Trains a random forest classifier on the selected parameters
- Calculates variable importance using the trained classifier
- Calculates LSM probability using the trained classifier
- Outputs a LSM probability raster in scale 0 to 1

### Outputs
The code outputs a LSM probability raster (probability) which can be visualized on a map. Additionally, the code produces a chart showing the variable importance of the parameters used in the LSM model.

### Usage
To use this code, you will need to modify the data inputs to match your study area and data. Once the code is executed, the LSM probability raster can be exported and used for further analysis or visualization.

### Disclaimer
This code is provided as-is and is intended for educational purposes only. Users should review and modify the code to ensure it is suitable for their specific needs and data.



