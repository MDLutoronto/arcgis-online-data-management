---
title: Reduce a layer by subsetting  # Title of the page, which will be displayed in the navigation and the browser title.
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

## Subsetting data

As an alternative to clipping, you can query a subset of features from your
spatial layer to upload.

<b>
Jump to:
<a href="#subsetting-in-arcgis-pro">ArcGIS Pro instructions</a> |
<a href="#subsetting-in-qgis">QGIS instructions</a> |
<a href="#subsetting-in-arcgis-online">ArcGIS Online instructions</a> |
</b>

### Subsetting in ArcGIS Pro

See our <b><a href="/arcgis-pro-extracting-geographic-features-from-larger-dataset/"
target="_blank">Extracting the geographic features you need from a larger dataset in
ArcGIS Pro</a></b> to learn how to subset data in Pro.

### Subsetting in QGIS

• Open <b>QGIS</b> and load the layer you'd like to extract a subset of features from.

<a href='{{ '/assets/images/qgis-layer-to-subset.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-layer-to-subset.png' | relative_url }}' alt="
Layer to subset in QGIS" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Right-click the layer name in the <b>Layers panel</b> and choose <b>Open
attribute table</b>.

<a href='{{ '/assets/images/qgis-open-attribute-table.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-open-attribute-table.png' | relative_url }}' alt="
Right-click layer -> Open attribute table" width='70%' style="border: 3px solid #888888;" />
</a>

• Click the <b>Select by expression</b> button.

<a href='{{ '/assets/images/qgis-select-by-expression.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-select-by-expression.png' | relative_url }}' alt="
Attribute table -> Select by expression" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• <b>Build a query</b> to select your features of interest (more information on
queries in QGIS can be found
<a href = "https://docs.qgis.org/latest/en/docs/user_manual/expressions/expression.html" target="_blank">
in the official documentation.</a>). Click <b>Select features</b>, then click
<b>Close</b>.

<a href='{{ '/assets/images/qgis-selection-query.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-selection-query.png' | relative_url }}' alt='
QGIS selection expression - in this example, "PRUID" = 12' width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Result: selected features will be <b>highlighted in yellow</b> on the map canvas, and the
count of selected features will be displayed in the QGIS status bar.

<a href='{{ '/assets/images/qgis-selected-features.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-selected-features.png' | relative_url }}' alt='
Display of selected features in QGIS.' width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Right-click the layer name again and choose <b>Export -> Save Selected
Features As...</b>

<a href='{{ '/assets/images/save-selected-features-as.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/save-selected-features-as.png' | relative_url }}' alt='
Export -> Save selected features as' width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Save the output to your computer as an <b>Esri Shapefile</b>. Click <b>OK</b>.

<a href='{{ '/assets/images/save-as-shapefile.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/save-as-shapefile.png' | relative_url }}' alt='
Save as shapefile' width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• You can now zip (compress) the output shapefile and upload it to ArcGIS Online. More
information on this is in
<a href="https://doc.arcgis.com/en/arcgis-online/reference/shapefiles.htm" target="_blank">Esri's official documentation.</a>

### Subsetting in ArcGIS Online

As with clipping data, we recommend doing this in desktop GIS software
<i>before</i> uploading the layer to ArcGIS Online. However, if you don't have
that option, here is how you can achieve the same result using ArcGIS Online:

• Log in to ArcGIS Online and open the large layer in the Map Viewer.

<a href='{{ '/assets/images/large-layer-map-viewer.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/large-layer-map-viewer.png' | relative_url }}' alt="
Large layer in the Map Viewer" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• From the Analysis tools, open the <b>Find by Attributes and Location</b> tool.

<a href='{{ '/assets/images/find-by-attributes-and-locations-tool.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/find-by-attributes-and-locations-tool.png' | relative_url }}' alt="
Analysis tools -> Find by Attributes and Location" width='60%' style="border: 3px solid #888888;" />
</a>

• Click <b>Build new query</b>.

<a href='{{ '/assets/images/build-new-query.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/build-new-query.png' | relative_url }}' alt="
Build new query" width='60%' style="border: 3px solid #888888;" />
</a>

• Choose <b>Attribute expression</b>. Click <b>Next</b>.

<a href='{{ '/assets/images/attribute-expression.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/attribute-expression.png' | relative_url }}' alt="
Attribute expression" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Construct a query to define your features of interest. Click <b>Add</b>.

<a href='{{ '/assets/images/attribute-query-builder.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/attribute-query-builder.png' | relative_url }}' alt="
Create a query and click Add" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Give the output layer a descriptive name. Click <b>Run</b>.

<a href='{{ '/assets/images/find-by-attributes-and-locations-parameters.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/find-by-attributes-and-locations-parameters.png' | relative_url }}' alt="
Find by attributes and location parameters" width='60%' style="border: 3px solid #888888;" />
</a>

• The tool should output a new layer containing only the queried features.

<a href='{{ '/assets/images/subset-layer-result.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/subset-layer-result.png' | relative_url }}' alt="
Find by attributes and location parameters" width='100%' height='100%' style="border: 3px solid #888888;" />
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
