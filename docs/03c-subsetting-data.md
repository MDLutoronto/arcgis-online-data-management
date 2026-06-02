---
title: Reduce a layer's spatial extent by subsetting  # Title of the page, which will be displayed in the navigation and the browser title.
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
spatial layer to upload. Workflows for ArcGIS Pro and ArcGIS Online are below
(the steps are very similar in QGIS).

### Subsetting in ArcGIS Pro

• Open the layer's <b>attribute table</b> by right-clicking on
it in the Contents pane and choosing <b>Attribute table</b>.

<a href='{{ '/assets/images/show-attribute-table.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/show-attribute-table.png' | relative_url }}' alt="
Show the attribute table" width='70%' style="border: 3px solid #888888;" />
</a>

• Click <b>Select by attributes</b>

<a href='{{ '/assets/images/select-by-attributes.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/select-by-attributes.png' | relative_url }}' alt="
Select by attributes" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Query the relevant features. Click <b>OK</b>. The features will be selected.
In this example, features have been queried according to a categorical value
(PRUID 12 means Nova Scotia in this dataset). You might also try querying
features by size - for example, maybe you're only interested in polygons above
or below a particular area threshold, or lines within a certain distance range.

<a href='{{ '/assets/images/query-features.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/query-features.png' | relative_url }}' alt="
Query data" width='70%' style="border: 3px solid #888888;" />
</a>

• Right-click the layer name in the Contents pane. Choose <b>Data -> Export
features</b>.

<a href='{{ '/assets/images/data-export-features.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/data-export-features.png' | relative_url }}' alt="
Data -> Export features" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Make sure that the <b>Use the selected records</b> option is toggled on, and click
<b>OK</b>.

<a href='{{ '/assets/images/use-selected-records.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/use-selected-records.png' | relative_url }}' alt="
Use the selected records" width='70%' style="border: 3px solid #888888;" />
</a>

• This will result in a new layer containing only the previously selected
features. It can now be added to ArcGIS Online.

<a href='{{ '/assets/images/subsetted-layer.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/subsetted-layer.png' | relative_url }}' alt="
New subset layer" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

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
