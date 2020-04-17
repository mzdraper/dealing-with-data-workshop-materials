# Mapbox Workshop

# Introduction to Digital Mapping

- [The slides](https://docs.google.com/presentation/d/1m513PQLsJZbSbn82OZaTP2yZHq6U3zacYLE9pWCNYNg/edit?usp=sharing)
- [The map](https://jsbin.com/rukijotacu/1/edit?html,output)

# Resources

## Mapbox Resources
| Resource                                  | Description/link                                                                                                                           |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Dealing with common uploading errors      | https://docs.mapbox.com/help/troubleshooting/uploads/                                                                                      |
| All Mapbox Tutorials                      | https://docs.mapbox.com/help/tutorials/                                                                                                    |
| Suggest trying Choropleth tutorials 1 & 2 | https://docs.mapbox.com/help/tutorials/choropleth-studio-gl-pt-1/<br><br>https://docs.mapbox.com/help/tutorials/choropleth-studio-gl-pt-2/ |
| GL-JS Documentation                       | https://docs.mapbox.com/mapbox-gl-js/api/                                                                                                  |
| How-to video library                      | https://www.mapbox.com/videos/                                                                                                             |




----------
## Introduction to GIS/Web Mapping

**Online classes**

- Penn State e-learning: [Introduction to GIS](http://- https://www.e-education.psu.edu/geog453/node/637)
- Penn State e- learning: [Web Mapping](https://www.e-education.psu.edu/geog585/node/508)
- University of Oregon: [Web Mapping](https://github.com/jakobzhao/geog371)
- UC Davis/Coursera: [Introduction to GIS fundamentals](https://www.coursera.org/learn/gis)
- Udemy: [QGIS instruction](https://www.udemy.com/topic/qgis/)
[](https://github.com/jakobzhao/geog371)
**Esri** free resources (may need to sign up for an account, but these are free):

- https://www.esri.com/training/catalog/57660c89bb54adb30c94541c/get-started-with-arcmap/
- https://www.esri.com/training/catalog/5b733dab8659c25ea7013f8e/arcmap-fundamentals/

**QGIS** training materials:

- https://docs.qgis.org/3.4/en/docs/training_manual/index.html
- https://www.youtube.com/channel/UCxs7cfMwzgGZhtUuwhny4-Q


----------
## Other Useful Tools


- Data Merger: https://funkeinteraktiv.github.io/geo-data-merger/
- Batch geocoding: https://geocode.localfocus.nl/
- Picking a color scale for scientific graphics: https://betterfigures.org/2015/06/23/picking-a-colour-scale-for-scientific-graphics/amp/?__twitter_impression=true
- Color advice for maps: http://colorbrewer2.org/
- Quick, simple tool for creating, viewing, and sharing maps: http://geojson.io/#map=2/20.0/0.0
- Image color picker: https://imagecolorpicker.com/
- Make a map style by dropping an image on the map with Cartogram: https://apps.mapbox.com/cartogram/#13.01/40.7251/-74.0051


----------
## Where to find data?
****
Jeremy Singer-Vine from Buzzfeed has an ongoing list of datasets: https://docs.google.com/spreadsheets/d/1wZhPLMCHKJvwOkP4juclhjFgqIY8fQFMemwKL2c64vk/edit#gid=0

**Local/Regional**

- Lots of cities have made their data available to the public (e.g. Oakland https://data.oaklandnet.com/, New York City https://opendata.cityofnewyork.us/)
- California state data portal https://data.ca.gov/
- California public health data https://hillcrestadvisory.com/2019/01/20/california-data-sources/
- Cal Fire: https://frap.fire.ca.gov/mapping/gis-data/

**Federal Government**

- OpenData.gov https://www.data.gov/
- Spatial Data Repository http://spatialdata.dhsprogram.com/home/
- Census Bureau https://www.census.gov/data.html
- NASA https://data.nasa.gov/
- NOAA https://data.noaa.gov/datasetsearch/, https://www.ncdc.noaa.gov/cdo-web/
- USGS https://data.usgs.gov/datacatalog/#fq=dataType%3A(collection%20OR%20non-collection)&q=*%3A,* https://www.usgs.gov/core-science-systems/national-geospatial-program/national-map, https://www.usgs.gov/products/data-and-tools/data-and-tools-topics
- https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html
- GeoMac (USGS) https://www.geomac.gov/
- USAID DHS Data: https://dhsprogram.com/data/available-datasets.cfm
- CDC: https://data.cdc.gov/

**Other**

- IPUMS Data (census data - US & international): https://usa.ipums.org/usa/data.shtml, https://international.ipums.org/international/
- WHO Data (this is free/public and they have a lot more than what is advertised on their data portal): https://www.who.int/gho/database/en/
- World Bank: https://datacatalog.worldbank.org/
- Harvard Geospatial Library http://hgl.harvard.edu:8080/opengeoportal/
- Global Forest Watch http://data.globalforestwatch.org/

## Dealing with data
GIS is roughly 90% data cleaning and 10% mapping. Check out the data folder of this repo for more information about common data issues and example datasets.

## Using Turf.js
Turf.js is an open source JavaScript library for advanced geospatial analysis. In the examples folder, you'll see a couple of examples that use Turf.js with Mapbox GL JS to display and analyze data.
- [Turf.js documentation](http://turfjs.org/)
- [Turf.js source code](https://github.com/Turfjs/turf)

## Programmatically working with Mapbox
If you're familiar with Python, I recommend checking out Mapbox's python CLI: https://github.com/mapbox/mapbox-cli-py.

The Mapbox web services APIs allow for programmatic access to Mapbox tools and services. Use these APIs to retrieve information about your account, upload and change resources, and use core Mapbox tools. To get started, check out the documentation:
- [Maps Services APIs](https://www.mapbox.com/api-documentation/#maps)
- [Geocoding API](https://www.mapbox.com/api-documentation/#geocoding)
- [Directions API](https://www.mapbox.com/api-documentation/#directions)

## Some cool examples to get you started
- [San Francisco 3D Lidar Extrusions](https://bl.ocks.org/ryanbaumann/2f66eecfe687338a1c2331003e7ec950)
- [Use Turf.js to measure how far a line travels through a polygon](https://bl.ocks.org/danswick/4a282503825358125b06)
- [Mapventure](https://bl.ocks.org/danswick/266d8642eb898d476aac)
- [Add a Scale](https://bl.ocks.org/malwoodsantoro/194e596647e9eca12720ec340b7283c1)
- [Minimap](https://bl.ocks.org/mzdraper/0adb47c10da050b5f6b8b1b5c4548afe)
