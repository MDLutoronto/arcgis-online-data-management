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

<img src='{{ '/assets/images/arcgis-pro-logo.png' | relative_url }}' alt="
ArcGIS Pro logo" width='60%' />

<b>See our <a href="/arcgis-pro-extracting-geographic-features-from-larger-dataset/"
target="_blank">Extracting the geographic features you need from a larger dataset in
ArcGIS Pro</a> tutorial to learn how to subset data in Pro.</b>

• Once you've created
a subset layer, you can use ArcGIS Pro's <a href="https://doc.esri.com/en/arcgis-pro/latest/help/sharing/overview/introduction-to-sharing-web-layers.html"
target="_blank">Share as web layer functionality</a> to
add it to ArcGIS Online, or 
<a href="https://doc.arcgis.com/en/arcgis-online/reference/shapefiles.htm" target="_blank">
upload a zipped shapefile</a> to the platform.

### Subsetting in QGIS

<img src='{{ '/assets/images/qgis-logo.png' | relative_url }}' alt="
ArcGIS Pro logo" width='60%' />

<b>We also have a tutorial on <a href="/qgis-extracting-geographic-features-from-larger-dataset/"
target="_blank">Extracting the geographic features you need from a larger dataset in
QGIS</a></b>.

• Once you've extracted a subset of your dataset by following these steps,
you can save the output as a zipped shapefile and <a href="https://doc.arcgis.com/en/arcgis-online/reference/shapefiles.htm" target="_blank">upload it to your
ArcGIS Online content</a>.

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
