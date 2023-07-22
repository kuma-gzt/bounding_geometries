#Bounding Geometries v0.1

**Bounding Geometries** is a plugin for QGIS that will calculate four types of minimum bounding geometries, namely: bounding box, oriented minimum bounding box, minimal enclosing circle and convex hull.

Installation
------------
Use the QGIS plugin manager or unzip the downloaded bounding_geometries.zip from the QGIS [plugin repository](http://plugins.qgis.org/plugins/bounding_geometries) into your plugins directory.

Usage
-----
* Click on ![icon](icon.png) to launch the plugin
* Select the layer containing the polygons
* Select the boundary geometries you need/want. A new **in-memory** layer called *Bounding Geometries* will be created holding the geometries
* The plugin will calculate the selected geometries for all the polygons in the layer

![dialog](resources/dialog.png)

Bounding Geometries Graphical Description
--------------------------- 
**Bounding Box**

![bounding_box](resources/bounding_box.png)

**Oriented Minimum Bounding Box**

![oriented_minimum_bounding_box](resources/oriented_minimum_bounding_box.png)

**Minimal Enclosing Circle**

![minimal_enclosing_circle](resources/minimal_enclosing_circle.png)

**Convex Hull**

![convex_hull](resources/convex_hull.png)

Multipart Polygons
------------------
The plugin works on multipart polygons: 

![multipart_polygon](resources/multipart_polygon.png)

Unvalid Geometry Polygons
------------------
If a polygon is not geometrically valid (after the [GEOS](https://libgeos.org/) library), the plugin will skip it and continue with the rest of polygons. Note that the plugin won't crash if such event happens, but a warning message will be displayed:

![invalid_polygon](resources/invalid_polygon.png)

Spatial Reference
-----------------
The plugin will calculate the bounding geometries for projected and non-projected coordinate systems.
