
# How to use arcgis in python

## Installation
```python
conda install -c esri arcgis
```

## Test installation


```python
from arcgis.gis import GIS

my_gis = GIS()
m = my_gis.map()
m
```
![image-title-here](https://github.com/aimanyongki/remotesensing/blob/master/_posts/test_arcgis.jpg?raw=true)

## Working with imagery
set item type to: ```Imagery Layer```
```python
import arcgis
from arcgis.gis import GIS
from IPython.display import display

gis = GIS()
```
```
items = gis.content.search("Landsat 8 Views", item_type="Imagery Layer", max_items=3)
```

```python
for item in items:
    display(item)
```


<div class="item_container" style="height: auto; overflow: hidden; border: 1px solid #cfcfcf; border-radius: 2px; background: #f6fafa; line-height: 1.21429em; padding: 10px;">
                    <div class="item_left" style="width: 210px; float: left;">
                       <a href='https://www.arcgis.com/home/item.html?id=a7412d0c33be4de698ad981c8ba471e6' target='_blank'>
                        <img src='https://www.arcgis.com/sharing/rest//content/items/a7412d0c33be4de698ad981c8ba471e6/info/thumbnail/ago_downloaded.jpg' class="itemThumbnail">
                       </a>
                    </div>

                    <div class="item_right"     style="float: none; width: auto; overflow: hidden;">
                        <a href='https://www.arcgis.com/home/item.html?id=a7412d0c33be4de698ad981c8ba471e6' target='_blank'><b>Pansharpened Landsat</b>
                        </a>
                        <br/>Landsat pansharpened and multitemporal 15m imagery rendered on-the-fly as Natural Color with DRA for visualization and analysis. This imagery layer is sourced from the Landsat on AWS collections and is updated daily with new imagery.<img src='https://www.arcgis.com/home/js/jsapi/esri/css/images/item_type_icons/imagery16.png' style="vertical-align:middle;">Imagery Layer by esri
                        <br/>Last Modified: September 05, 2019
                        <br/>0 comments, 75,480 views
                    </div>
                </div>
                



<div class="item_container" style="height: auto; overflow: hidden; border: 1px solid #cfcfcf; border-radius: 2px; background: #f6fafa; line-height: 1.21429em; padding: 10px;">
                    <div class="item_left" style="width: 210px; float: left;">
                       <a href='https://www.arcgis.com/home/item.html?id=6b003010cbe64d5d8fd3ce00332593bf' target='_blank'>
                        <img src='https://www.arcgis.com/sharing/rest//content/items/6b003010cbe64d5d8fd3ce00332593bf/info/thumbnail/ago_downloaded.jpg' class="itemThumbnail">
                       </a>
                    </div>

                    <div class="item_right"     style="float: none; width: auto; overflow: hidden;">
                        <a href='https://www.arcgis.com/home/item.html?id=6b003010cbe64d5d8fd3ce00332593bf' target='_blank'><b>Panchromatic Landsat</b>
                        </a>
                        <br/>Landsat panchromatic and multitemporal 15m imagery with on-the-fly renderings and indices for visualization and analysis. The Landsat 8 imagery in this layer is updated daily and is directly sourced from the Landsat on AWS collection.<img src='https://www.arcgis.com/home/js/jsapi/esri/css/images/item_type_icons/imagery16.png' style="vertical-align:middle;">Imagery Layer by esri
                        <br/>Last Modified: September 05, 2019
                        <br/>0 comments, 35,492 views
                    </div>
                </div>
                



<div class="item_container" style="height: auto; overflow: hidden; border: 1px solid #cfcfcf; border-radius: 2px; background: #f6fafa; line-height: 1.21429em; padding: 10px;">
                    <div class="item_left" style="width: 210px; float: left;">
                       <a href='https://www.arcgis.com/home/item.html?id=c34fd380d16f40a7bb7995ac4d7ab8de' target='_blank'>
                        <img src='https://www.arcgis.com/sharing/rest//content/items/c34fd380d16f40a7bb7995ac4d7ab8de/info/thumbnail/ago_downloaded.jpg' class="itemThumbnail">
                       </a>
                    </div>

                    <div class="item_right"     style="float: none; width: auto; overflow: hidden;">
                        <a href='https://www.arcgis.com/home/item.html?id=c34fd380d16f40a7bb7995ac4d7ab8de' target='_blank'><b>Landsat 8 Pansharpened</b>
                        </a>
                        <br/>Landsat 8 pansharpened and multitemporal imagery rendered on-the-fly as Natural Color with DRA for visualization and analysis. The imagery in this layer is updated daily and is directly sourced from the Landsat on AWS collection.<img src='https://www.arcgis.com/home/js/jsapi/esri/css/images/item_type_icons/imagery16.png' style="vertical-align:middle;">Imagery Layer by esri
                        <br/>Last Modified: September 05, 2019
                        <br/>1 comments, 127,933 views
                    </div>
                </div>
                


Obtaining imagery based on their item id


```python
l8_views = gis.content.get('4ca13f0e4e29403fa68c46d188c4be73')
l8_views
```




<div class="item_container" style="height: auto; overflow: hidden; border: 1px solid #cfcfcf; border-radius: 2px; background: #f6fafa; line-height: 1.21429em; padding: 10px;">
                    <div class="item_left" style="width: 210px; float: left;">
                       <a href='https://www.arcgis.com/home/item.html?id=4ca13f0e4e29403fa68c46d188c4be73' target='_blank'>
                        <img src='https://www.arcgis.com/sharing/rest//content/items/4ca13f0e4e29403fa68c46d188c4be73/info/thumbnail/ago_downloaded.png' class="itemThumbnail">
                       </a>
                    </div>

                    <div class="item_right"     style="float: none; width: auto; overflow: hidden;">
                        <a href='https://www.arcgis.com/home/item.html?id=4ca13f0e4e29403fa68c46d188c4be73' target='_blank'><b>Landsat 8 Views</b>
                        </a>
                        <br/>Landsat 8 multispectral and multitemporal imagery with on-the-fly renderings and indices for visualization and analysis. The imagery in this layer is updated daily and is directly sourced from the Landsat on AWS collection.<img src='https://www.arcgis.com/home/js/jsapi/esri/css/images/item_type_icons/imagery16.png' style="vertical-align:middle;">Imagery Layer by esri
                        <br/>Last Modified: September 05, 2019
                        <br/>0 comments, 163,030 views
                    </div>
                </div>
                



Accessing ```ImageryLayer``` from Imagery Layer items
