# Environmental-DS-Project

## Environmental Problem

The environmental problem our group is examining is the expansion of the Sahara Desert due to desertification over the past several decades. This process is driven by climate change, declining rainfall, rising temperatures, and unsustainable land use, leading to soil degradation and loss of vegetation. As the desert expands, it threatens ecosystems and the livelihoods of people living in surrounding regions, particularly in the Sahel. 

For local communities, desertification is an immediate threat to food security, water access, and economic stability. Regional governments often frame the issue as a development and security concern, as environmental degradation can contribute to migration and political instability. International organizations and environmental groups tend to frame desertification as a global environmental challenge tied to climate change and biodiversity loss. Ongoing initiatives, such as the Great Green Wall, are possible solutions that address both environmental degradation and human well-being.


## Datasets

### MODIS/Terra+Aqua Land Cover Type Yearly L3 Global 500m SIN Grid V061 
Source: Nasa  
Access Link: [https://www.earthdata.nasa.gov/data/catalog/lpcloud-mcd12q1-061](https://www.earthdata.nasa.gov/data/catalog/lpcloud-mcd12q1-061)

For every year from 2001-2025 (ordinal), we have the following data:

| Variable        | Description | Data Type |
|-----------------|-------------|-----------|
| X  | Latitude | continuous |
| Y | Longitude | continuous |
| LC_Type1 | Land Cover Type 1: Annual International Geosphere-Biosphere Programme (IGBP) classification | nominal |
| LC_Type2 | Land Cover Type 2: Annual University of Maryland (UMD) classification | nominal |
| LC_Type3 | Land Cover Type 3: Annual Leaf Area Index (LAI) classification | nominal |

### MODIS/Terra Vegetation Indices Monthly L3 Global 1km SIN Grid V061 
Source: Nasa  
Access Link: [https://www.earthdata.nasa.gov/data/catalog/lpcloud-mod13a3-061](https://www.earthdata.nasa.gov/data/catalog/lpcloud-mod13a3-061)

For every year from 2001-2025 (ordinal), we have the following data:

| Variable        | Description | Data Type |
|-----------------|-------------|-----------|
| X  | Latitude | continuous |
| Y | Longitude | continuous |
| 1 km monthly EVI | 1 km monthly Enhanced Vegetation Index | continuous |
| 1 km monthly NDVI | 1 km monthly Normalized Difference Vegetation Index | continuous |
| 1 km monthly pixel reliability | Quality reliability of VI pixel | ordinal |

### MODIS/Terra Land Surface Temperature/Emissivity Monthly L3 Global 6km SIN Grid V061 
Source: Nasa  
Access Link: [https://www.earthdata.nasa.gov/data/catalog/lpcloud-mod11b3-061](https://www.earthdata.nasa.gov/data/catalog/lpcloud-mod11b3-061)

For every year from 2000-2025 (ordinal), we have the following data:

| Variable        | Description | Data Type |
|-----------------|-------------|-----------|
| X  | Latitude | continuous |
| Y | Longitude | continuous |
| LST_Day_6km | Day Land Surface Temperature | continuous |
| LST_Night_6km | Night Land Surface Temperature | continuous |
| Emis_31 | Band 31 emissivity useful for detecting shifts at desert margin | continuous |

## How to access data
Select one of the following NASA Earthdata links:

* [MCD12Q1 (Land Coverage Type)](https://www.earthdata.nasa.gov/data/catalog/lpcloud-mcd12q1-061)
* [MOD13A3 (Vegetation Indices)](https://www.earthdata.nasa.gov/data/catalog/lpcloud-mod13a3-061)
* [MOD11B3 (Temperature/Emissivity)](https://www.earthdata.nasa.gov/data/catalog/lpcloud-mod11b3-061)

Once on your chosen product page, you should find the __"Data Access"__ tab on the right side of the screen.

Look for the row labeled __"Earthdata Search"__ and click the __"Download"__ button. This will open the global Earthdata Search map interface.

In the top-left corner, underneath the main search bar, look for the __"Spatial"__ button.

Select __"Rectangle"__ from the drop-down menu.

Click and drag on the map to draw a box over your area of interest (e.g., the Senegal region). This filters the thousands of global files to only those covering your specific coordinates.

The matching files (granules) will appear in the sidebar.

Look for the __"Download All"__ button near the bottom-middle of the screen and click it.

A summary page will appear. Click the blue __"Download Data"__ button in the bottom-left corner to proceed to the final delivery options.

You will be presented with several tabs. Select the __"Download Files"__ tab.

 Press the __"Download Files"__ button.  Earthdata will prompt you to install their specialized download client.

Run the installer and authorize it with your Earthdata login. The software will create a folder in your designated directory and begin downloading the `.hdf` or `.tif` files.

To use these files in R for example, a library package like `terra` will be needed.
