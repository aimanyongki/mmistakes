
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

![image-title-here](https://github.com/aimanyongki/remotesensing/blob/master/_posts/imagelayer.JPG?raw=true)


Obtaining imagery based on their item id


```python
l8_views = gis.content.get('4ca13f0e4e29403fa68c46d188c4be73')
l8_views
```
![image-title-here](https://github.com/aimanyongki/remotesensing/blob/master/_posts/imagelayer2.JPG?raw=true)

Accessing ```ImageryLayer``` from Imagery Layer items
