
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
items = gis.content.search("Landsat 8 Views", item_type="Imagery Layer", max_items=2)

