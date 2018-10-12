# Dealing with Data
GIS work is roughly 90% data cleaning and 10% mapping. Even when you have data, you could run into issues when using a GIS tool, like Mapbox, to display your data. Sometimes these issues arise because of the tool’s limitations. As a mapper, it's up to you to ask the following:

- What are the best set of tools to achieve my goal?
- How can I manipulate my data to fit this tool without too much compromise?

Working with users across topic and skill level, I’ve fielded an array of different types of geodata questions. Here's a few of the biggest issues users run into and some solutions I help them work through.

## I have really big data.
At Mapbox, we have internal APIs that upload your data and convert it to vector tiles, or MBTiles. During this process, data that is too large is subject to simplification. To avoid data simplification, here are some common strategies I recommend.

- **Clean your data.** If you see your data’s features have unnecessary properties, cut them out. While it doesn’t seem like much, if you have a GeoJSON with thousands of lines, and you’re able to cut out just a couple properties from each of the features, you’ll see a significant increase in memory.
- **Simplify your data.** While there are cases for very granular data, if most of your data is at a macro scale, it’s likely not one of those granular cases. As a mapper, it’s your judgement call of how intensely you should simplify your data. This is also known as tolerance. At Mapbox, we implement the Douglas-Peuker algorithm to simplify data and improve performance of GeoJSON data.
![simplification image](https://c1.staticflickr.com/9/8216/28486171002_f282ce64c4_b.jpg)

- **Change how your tool registers the data.** Markers are commonly added to maps, but they’d added by creating HTML elements. This becomes an issue when you have thousands of markers, because you have thousands of HTML elements on your map. When you notice a significant lag, it’s a good time to ask how your tool best deals with large point data. In Mapbox’s case, points can be represented as circles, SVG icon symbols and markers. Simpler output will be more performant. For large point data, you should consider having your data represented as points instead of icons or markers.
- **Split your sources.** You can split your GeoJSON source into two or three parts, effectively doubling or tripling your ability to load and render more data. Tools like [geojsplit](https://www.npmjs.com/package/geojsplit) make the process of breaking up GeoJSON sources manageable. Once the data has been divided, each source can be added to the map using addSource() and addLayer(). If you’re interested, check out a [practical example](http://bl.ocks.org/ryanbaumann/04c442906638e27db9da243f29195592/33e8d3520feecf0912f489689ca4a5c01bdfcbfc) of how to add a split source to a map. Please note that source splitting will not do much to increase performance on mobile browsers.
- **Tile on a server.** The easiest way to do this is to upload the data to Mapbox via the Uploads API. If your data exceeds the upload limit or you are interested in further optimizing your data, consider checking out our [Manage large data files for Mapbox Studio with Tippecanoe guide](https://www.mapbox.com/help/large-data-tippecanoe/) for tips on ways to reduce the file size.


## I can’t see my data at every zoom level.
- **Understanding the collision algorithm.** Each feature on a map has a collision box surrounding it. The collision algorithm checks to see if the boxes are colliding and, if so, how how much overlap there is. It then decides at what zoom level data appears so that features aren’t colliding and decreasing legibility. I recommend using a tool called Tippecanoe to adjust the zoom level of data.
- **Understanding the relationship between zoom level and geographic distance.** Each zoom level’s scale is exponentially different and should be an important factor when considering the appropriate zoom level for your data. This is important with data like contour lines. Contour lines appear at z9 with an interval of 500 meters. Because z9 is still fairly zoomed out, if you reduce the interval the lines will become very close together and difficult to read.

## What do I do with it?
This is where the 10% mapping comes in! It's good to have an idea (or even better a visual) of what you want your map to look like and some key functionality. Keep in mind the constraints of the tools you're using and be pragmatic. To get you started, here’s a few types of maps and ways to can work with data:

- [Heatmap](https://www.mapbox.com/mapbox-gl-js/example/heatmap-layer/)
- [Cluster](https://www.mapbox.com/mapbox-gl-js/example/cluster/)
- [Choropleth](https://www.mapbox.com/mapbox-gl-js/example/updating-choropleth/)
- [Marker](https://www.mapbox.com/mapbox-gl-js/example/custom-marker-icons/)
- [Line](https://www.mapbox.com/mapbox-gl-js/example/line-gradient/)

In this repo, you'll find a lot of different data. Here's a quick rundown of __what__ there is, but __how__ to map this data is up to you.
- Earthquake data from USGS
- iNaturalist is crowdsourced data of species spottings around the Bay area
- Indoor map data is ready for [extrusions](https://www.mapbox.com/mapbox-gl-js/example/3d-extrusion-floorplan/)
- landsat.tif is satellite imagery
- Michael Brown tweets are a collection of hastagged tweets around the time of Brown's death
- SF evictions and tech shuttle also has some census data split by SF tracts
- US states has the data for the 50 strategies

## Some good reads
- [Hundreds of Thousands of Polygons Rendered on the Fly](https://blog.mapbox.com/hundreds-of-thousands-of-polygons-rendered-on-the-fly-9eb0b81b64f3)
- [Strategies to Effectively Display Large Amounts of Data in Web Apps](https://www.esri.com/arcgis-blog/products/arcgis-online/mapping/strategies-to-effectively-display-large-amounts-of-data-in-web-apps/)
