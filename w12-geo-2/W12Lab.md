# Playing with an SVG map

- [Flowing Data: How to Make a US County Thematic Map Using Free Tools](http://flowingdata.com/2009/11/12/how-to-make-a-us-county-thematic-map-using-free-tools/)


# Using D3.js to create a choropleth map. 


# Using Leaflet to draw geographical heatmaps

## Mapbox

[Mapbox](https://www.mapbox.com) is a mapping platform. You can use it for developing mobile or web apps, or use it to create geo-visualizations. Create an account, create a project, and play with it. You can display maps in different styles, in different locations, and in different zoom levels. When you click "save", it saves the current view (style, location, zoom level) as the default for your app. For heatmaps, black map works well. 

In "Project" tap, you can see your `map ID`. Copy the code in the `Embed` section somewhere, you can see the following code:

    share.html?access_token=.....'></iframe>

Copy the .... part (the `access token`). 

## Leaflet

Now you can use the mapbox tiles with the [Leaflet, which is an open-source JavaScript library for mobile-friendly interactive maps](http://leafletjs.com). By using the following pages, draw a heatmap of Walmart stores. 

- [Wal-Mart Stores](https://www.google.com/fusiontables/DataSource?docid=1ag3Z3Uwp_hWiHeiBRqGrS_HzEtwUjeVh4d4ZAnI#rows:id=1): `File` -> `Download`
- [Leaflet Quick start guide](http://leafletjs.com/examples/quick-start.html)
- [A tiny, simple and fast heatmap plugin for Leaflet.](https://github.com/Leaflet/Leaflet.heat) - you don't need to download from this page. Use the following template. 

Here is an HTML template:

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width">
<title>Walmart Heatmap</title>

<link rel="stylesheet" href="http://cdn.leafletjs.com/leaflet/v0.7.7/leaflet.css" />

<style type="text/css" media="screen">
#map { height: 800px; }  
</style>

</head>

<body>

<div id="map"></div>

<script src="http://cdn.leafletjs.com/leaflet/v0.7.7/leaflet.js"></script>
<script src="http://leaflet.github.io/Leaflet.heat/dist/leaflet-heat.js"></script>
<script src="walmart.js"></script>  <!-- put your data into data.js -->

<script>

//  put your code here. 

</script>

</body>
</html>

```

You can get something like this: 

![Walmart heatmap](https://raw.githubusercontent.com/yy/dviz-course/master/w12-geo-2/walmart.png)