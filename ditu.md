# 支持WEB、Android、IOS的地图解决方案
### 方案架构
##### 1. 在线解决方案  
![在线解决方案](./ditu/d1.png)  
优点：可以实时更新底图、POI，利用服务端进行路径查找  
缺点：需要网络支持，服务端有流量压力
##### 2. 离线解决方案  
![离线解决方案](./ditu/d2.png)  
优点：不需网络支持，图片显示迅速  
缺点：更新地图时需要下载整个离线地图包
##### 3. 混合解决方案  
![混合解决方案](./ditu/d3.png)  
优点：图片显示迅速，减轻服务端压力。可以实时更新POI，利用服务端进行路径查找  
缺点：实现复杂度高

### 工具链
##### GIS工具集
1. [OpenGeo Suite](http://boundlessgeo.com/solutions/opengeo-suite/download/)  
功能：包含PostGIS, GeoServer, GeoWebCache, OpenLayers, 和 QGIS

##### 地图准备  
1. [QGIS](http://www.qgis.org/) ![QGIS](http://www.qgis.org/en/_static/logo.png)  
功能：导入、导出、编辑.shp,postgis,geotiff,geojson,dxf等多种GIS文件,给普通图片配准到地理坐标
教程：[http://www.qgistutorials.com/en/](http://www.qgistutorials.com/en/)  

2. [DraftSight](http://www.3ds.com/products-services/draftsight/download-draftsight/)  
功能：编辑CAD文件

3. [SketchUp](http://www.sketchup.com/)  
功能：从CAD文件生成3D视图

##### 地图服务
1. [GeoServer](http://geoserver.org/display/GEOS/Stableop)  
功能：地图服务发布。作为war放入Tomcat或Jetty即可使用。可发布geotiff,.shp,POSTGIS等多种GIS数据为地图。通过openlayer或QGIS浏览。

2. [GeoWebCache](http://geowebcache.org)  
功能：缓存地图瓦片，提高性能。已内置在最新版GeoServer中。

3. [TileStream](https://github.com/mapbox/tilestream‎)  
功能：把.mbtile文件发布为地图服务

##### 离线地图打包
1. [TileMill](https://www.mapbox.com/tilemill/‎)  
功能：将geotiff,geojson,csv,shp,postgis等文件美化、打包为.mbtile瓦片地图文件

2. [mbutil](https://github.com/mapbox/mbutil)  
功能：将.mbtile文件分解为图片和json文件

##### 地图浏览
1. [Leaflet](http://leafletjs.com/)  
2. [openlayers](http://openlayers.org/)
