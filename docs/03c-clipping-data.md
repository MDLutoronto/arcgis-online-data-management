---
title: Reduce a layer by clipping  # Title of the page, which will be displayed in the navigation and the browser title.
layout: page  # Layout type, usually 'page' for standard pages.
nav_order: 2  # Order in the navigation menu.
parent: Managing feature storage
grand_parent: ArcGIS Online data management
created_date: 2026-05-29 # Date when the page was created. Should be in YYYY-MM-DD format.
staff:  # Optional: Nested list of staff members associated with the page.
maintainer:
  - name: Cole White # PLACEHOLDER: Replace with actual maintainer's name.
    link: https://library.utoronto.ca/staff/cole-white  # link is optional

---

## Clipping data

<figure>
<img src='{{ '/assets/images/clip-tool-graphic.gif' | relative_url }}' alt="
Example of subsetting spatial data by clipping" width='70%' style="border: 3px solid #888888;" />
<figcaption>Image source: <a href="https://commons.wikimedia.org/wiki/File:Example_of_Clip_Tool_process.gif"
target="_blank">Wikimedia Commons</a>. <a href="https://creativecommons.org/licenses/by-sa/4.0/deed.en"
target="_blank">CC-BY-SA 4.0</a>.</figcaption>
</figure>

You may be working with a spatial layer that is much more geographically 
expansive than your study area. In this case, you can <b>clip or subset</b> the layer to your
area of interest using ArcGIS Pro or QGIS before adding it to ArcGIS Online.
If your layer is already uploaded, there are tools in ArcGIS Online that can
do this as well.

<b>Example:</b> This Statistics Canada layer (downloaded from
<a href="https://www12.statcan.gc.ca/census-recensement/2021/geo/sip-pis/boundary-limites/index2021-eng.cfm?year=21"
target="_blank">this page</a>), displays all census dissemination areas within
Canada. It will consume about 500 MB (0.5 GB) of feature storage if uploaded to
ArcGIS Online. However, if you only need to work with 
(for example) Nova
Scotia's dissemination areas, this will only account for about 20 MB of
feature storage. <b>By clipping or subsetting the data, you can save space by
only uploading what you actually need.</b>

<a href='{{ '/assets/images/lda.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/lda.png' | relative_url }}' alt="Canada
census dissemination area polygons" width='100%' height='100%'  style="border:
3px solid #888888;" />
</a>

The steps below outline how to clip a data layer using ArcGIS Pro, QGIS, and
ArcGIS Online.

<b>
Jump to: 
<a href="#clipping-data-in-arcgis-pro">ArcGIS Pro instructions</a> |
<a href="#clipping-data-in-qgis">QGIS instructions</a> |
<a href="#clipping-data-in-arcgis-online">ArcGIS Online instructions</a>
</b>

### Clipping data in ArcGIS Pro

• <b>Follow the steps in our <a href="https://mdlutoronto.github.io/clipping-vector-data-in-arcgis-pro/"
target="_blank">Clipping vector data in ArcGIS Pro</a> tutorial.</b>

• Once you've created a clipped layer, it can be uploaded to ArcGIS Online by
right-clicking its
name in the Contents pane and choosing <b>Sharing -> Share as web layer</b>.
(Alternatively, save the layer as a
<a href="https://doc.arcgis.com/en/arcgis-online/reference/shapefiles.htm" target="_blank">shapefile</a>, zip/compress it,
and upload the zip to ArcGIS Online).

<a href='{{ '/assets/images/share-as-web-layer.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/share-as-web-layer.png' | relative_url }}' alt="
Share as web layer" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

### Clipping data in QGIS

• MDL has a separate tutorial for this too.
<b>Follow the steps <a href="https://mdlutoronto.github.io/clipping-vector-data-in-qgis/"
target="_blank">here</a>.</b>

• After performing the clip, <b>zip (compress) the output shapefile</b> and <b>upload</b> it to ArcGIS Online.
More information on this is in
<a href="https://doc.arcgis.com/en/arcgis-online/reference/shapefiles.htm" target="_blank">
Esri's official documentation.</a>

### Clipping data in ArcGIS Online
We recommend using the desktop options described above to clip or otherwise preprocess
your data. However, if your large data layer has already been uploaded to
ArcGIS Online, or if you are unable to access QGIS or ArcGIS Pro, you can perform
the clip in ArcGIS Online itself. After the data has been clipped, you will
<b>delete the original layer</b> and keep only the output of the clip operation.

Here is how you can do this:

• Log in to ArcGIS Online. Open the large layer in the <b>Map Viewer</b>.
Optionally add a clip layer representing your study area.

<a href='{{ '/assets/images/clip-data-map-viewer.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/clip-data-map-viewer.png' | relative_url }}' alt="
Open the large layer in the Map Viewer" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Open <b>Overlay Layers</b> from the Analysis tools.

<a href='{{ '/assets/images/overlay-layers-tool.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/overlay-layers-tool.png' | relative_url }}' alt="
The Overlay Layers tool" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Specify the large layer as the <b>Input features</b>. If you have a layer 
defining the area you'd like to clip, use this for the <b>Overlay features</b>, or click the pencil 
icon to draw an area of interest. Leave the <b>Overlay type</b> as
<b>Intersect</b>. Give the <b>Result layer</b> a descriptive name and click
<b>Run</b>.

<a href='{{ '/assets/images/overlay-layers-parameters.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/overlay-layers-parameters.png' | relative_url }}' alt="
The Overlay Layers tool" width='60%' style="border: 3px solid #888888;" />
</a>

• The Overlay Layers tool will output a <b>new, clipped layer.</b>

<a href='{{ '/assets/images/overlay-layers-output.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/overlay-layers-output.png' | relative_url }}' alt="
Overlay layers output in Map Viewer" width='60%' style="border: 3px solid #888888;" />
</a>

• Next, you will need to <b>delete the original layer</b>. Find the layer in your
content and open its Item Details page. Click the <b>Settings</b> tab.

<a href='{{ '/assets/images/large-layer-item-details.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/large-layer-item-details.png' | relative_url }}' alt="
ArcGIS Online item details page" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Click the <b>Delete</b> button.

<a href='{{ '/assets/images/delete-item-arcgis-online.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/delete-item-arcgis-online.png' | relative_url }}' alt="
ArcGIS Online item details page" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Click the <b>Show more</b> button.

<a href='{{ '/assets/images/show-more-button-arcgis-online.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/show-more-button-arcgis-online.png' | relative_url }}' alt="
ArcGIS Online item details page" width='60%' style="border: 3px solid #888888;" />
</a>

• Click <b>Delete permanently (cannot be undone)</b>. The layer will be removed
from UofT's ArcGIS Online instance and space will be freed up.

<a href='{{ '/assets/images/delete-permanently.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/delete-permanently.png' | relative_url }}' alt="
ArcGIS Online item details page" width='60%' style="border: 3px solid #888888;" />
</a>
