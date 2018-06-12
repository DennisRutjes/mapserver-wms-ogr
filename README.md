# Natura2000 example

## Introduction
This is a example implementation of our [Docker base image](https://github.com/PDOK/mapserver-wms-ogr). It contains a mapfile natura2000.map and a geopackage natura2000.gpkg containing the vector data.

## Usage
```
git clone https://github.com/PDOK/mapserver-wms-ogr.git
cd /mapserver-wms-ogr
git checkout natura2000-example
```

```
docker build -t natura2000-example .
```

```
docker run -d -p 80:80 --name natura2000-service natura2000-example
```

Check if it works: http://localhost/natura2000/wms?request=getcapabilities&service=wms&version=1.3.0 should return an getcapabilities document. Loading the http://localhost/natura2000/wms in QGIS or ARCGIS should give access to the map data.

![getcapabilities](/img/getcapabilities-natura2000.jpg)
