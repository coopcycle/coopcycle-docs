---
layout: default
title: Zones
parent: Deliveries
redirect_from:
  - /en/tutorials/zones.html
---

# Zones

<div class="alert mt-3 alert-info" role="alert">
Here you can upload a <code>.geojson</code> file containing a perimeter which will mark the delivery area.
</div>

## Creating a `.geojson` file

This is how you create the delivery zone or perimeter by using any software that allows the creation of a **polgyone** and saving or exporting a `.geojson` file.

1. Go to the online software [geojson.io](https://geojson.io/)
2. Zoom in to the specific area you want to create a perimeter around.
3. Select the **polygone** ![](/assets/images/polygoonIconGeoJsonDotIo.png) tool on the right-hand side vertical bar.
4. Once the tool is selected, click once anywhere you want, move your cursor to the next area on the map and click again. This will form a straight line between those first two pins, keep going until you reach the first pin you created and click right on it for the polygone (zone or perimeter) to form. 

    <span class="badge badge-info">TIP:</span><span> To move around the map whilst drawing the polygone, simply hold left-click whilst moving the map, unhold the left-click and continue drawing the polygone.</span>

5. Once you've finished creating the zone, hover over the **Save** button on the top-left corner and select **GeoJSON**.
6. This will download the `.geojson` file.
   
## Upload the `.geojson` file

1. On the Zones main page click on <span class="badge badge-secondary">File</span> and select the `.geojson` file.
2. Click on <span class="badge badge-primary">Send</span> to upload the file to the platform.
3. Once uploaded, on the Zones main page a preview map of the zone will be displayed. 

Below is a GIF example on how to use the geojson.io software.

---

![Create a polygone on geojson dot io]({{ "/assets/images/createAPolygoneZone.gif" | absolute_url }})
