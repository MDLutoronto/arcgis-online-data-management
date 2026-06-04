---
title: Reduce layer complexity by removing unneeded fields  # Title of the page, which will be displayed in the navigation and the browser title.
layout: page  # Layout type, usually 'page' for standard pages.
nav_order: 4 # Order in the navigation menu.
parent: Managing feature storage
grand_parent: ArcGIS Online data management
created_date: 2026-05-29 # Date when the page was created. Should be in YYYY-MM-DD format.
staff:  # Optional: Nested list of staff members associated with the page.
maintainer:
  - name: Cole White # PLACEHOLDER: Replace with actual maintainer's name.
    link: https://library.utoronto.ca/staff/cole-white  # link is optional

---

## Reduce a layer's complexity by removing unneeded fields

If your spatial dataset has a large number of unnecessary fields (columns), you
can simplify it by <b>removing the ones you don't need</b>.

Deleting excess fields will save space on the
server and have the added benefit of giving you cleaner, more organized data
to work with. This can be done in desktop GIS software before you upload the
data, or it can be done directly in ArcGIS Online.

<b>
Jump to:
<a href="#removing-unneeded-fields-in-arcgis-pro">ArcGIS Pro instructions</a> |
<a href="#removing-unneeded-fields-in-qgis">QGIS instructions</a> |
<a href="#removing-unneeded-fields-in-arcgis-online">ArcGIS Online instructions</a>
</b>

### Removing unneeded fields in ArcGIS Pro

Example: This layer of world country boundaries (downloaded from
<a href="https://www.naturalearthdata.com/" target="_blank">
Natural Earth</a>) has 170 fields - that's a lot! It may be, however, that you
only need a few of these fields for your work. Here's how you can remove the
ones you don't need.

<a href='{{ '/assets/images/countries-layer.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/countries-layer.png' | relative_url }}' alt="
Open the Map Viewer." width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Right-click the layer in the Contents pane and choose <b>Data Design ->
Fields</b>.

<a href='{{ '/assets/images/data-design-fields.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/data-design-fields.png' | relative_url }}' alt="
Data Design -> Fields" width='70%' style="border: 3px solid #888888;" />
</a>

• <b>Select</b> the fields you'd like to remove by left-clicking on their rows
(Shift-click or Control-click to select multiple items).

<a href='{{ '/assets/images/select-fields.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/select-fields.png' | relative_url }}' alt="
Select fields" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Right-click on any of the selected rows and choose <b>Delete</b>.

<a href='{{ '/assets/images/delete-rows.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/delete-rows.png' | relative_url }}' alt="
Delete fields" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Click the <b>Save</b> button on the ribbon to commit the changes.

<a href='{{ '/assets/images/save-field-edits.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/save-field-edits.png' | relative_url }}' alt="
Save field edits" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• You now have a dataset with a much smaller attribute table. From here, you
can share it as a web layer directly from Pro to ArcGIS Online, or upload
it as a shapefile.

<a href='{{ '/assets/images/simplified-attribute-table.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/simplified-attribute-table.png' | relative_url }}' alt="
Spatial layer with simplified attribute table" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

### Removing unneeded fields in QGIS
• Open QGIS and load your layer.

<a href='{{ '/assets/images/qgis-ne-layer.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-ne-layer.png' | relative_url }}' alt="
Natural Earth countries layer in QGIS" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• <b>Right-click (or Control-click on MacOS)</b> the layer name in the Layers Panel and
choose <b>Properties</b>.

<a href='{{ '/assets/images/qgis-layer-properties.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-layer-properties.png' | relative_url }}' alt="
Right-click layer -> Properties" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Click the <b>Fields</b> tab.

<a href='{{ '/assets/images/qgis-properties-fields.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-properties-fields.png' | relative_url }}' alt="
Properties -> Fields" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Click the <b>Pencil button</b> to enable editing of fields.

<a href='{{ '/assets/images/qgis-fields-edit-button.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-fields-edit-button.png' | relative_url }}' alt="
QGIS field edit button" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• <b>Select</b> the fields you'd like to remove by left-clicking them (Shift-click
to select multiple.)

<a href='{{ '/assets/images/qgis-selected-fields.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-selected-fields.png' | relative_url }}' alt="
Select fields to delete" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Click the <b>Delete field</b> button.

<a href='{{ '/assets/images/qgis-delete-field-button.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-delete-field-button.png' | relative_url }}' alt="
Delete field button" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• All of the fields you'd selected will be removed. Click the <b>Save</b>
button.

<a href='{{ '/assets/images/qgis-field-edit-save.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-field-edit-save.png' | relative_url }}' alt="
Save field edits" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Click the <b>Pencil button</b> again to toggle off edit mode. Click <b>OK</b>.

<a href='{{ '/assets/images/qgis-field-edit-toggle.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-field-edit-toggle.png' | relative_url }}' alt="
Toggle off edit mode" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• You can now zip (compress) a shapefile of your layer and upload it to ArcGIS Online.
More information on this is in
<a href="https://doc.arcgis.com/en/arcgis-online/reference/shapefiles.htm" target="_blank">
Esri's official documentation.</a>

### Removing unneeded fields in ArcGIS Online

• Log in to ArcGIS Online and navigate to the <b>Item Details page</b> of your
hosted feature layer.

<a href='{{ '/assets/images/item-details-delete-field.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/item-details-delete-field.png' | relative_url }}' alt="
Item details page in ArcGIS Online" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Click the <b>Data</b> tab.

<a href='{{ '/assets/images/item-details-data-tab.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/item-details-data-tab.png' | relative_url }}' alt="
Item details page - data tab" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Click <b>Fields</b>.

<a href='{{ '/assets/images/data-fields.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/data-fields.png' | relative_url }}' alt="
Item details -> Data -> Fields" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Check the fields you wish to remove.

<a href='{{ '/assets/images/check-fields-to-delete.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/check-fields-to-delete.png' | relative_url }}' alt="
Check fields to delete" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Click the <b>Delete</b> button at the top right of the screen.

<a href='{{ '/assets/images/arcgis-online-delete-fields.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/arcgis-online-delete-fields.png' | relative_url }}' alt="
Click delete button" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Click the red <b>Delete fields</b> button to confirm that you actually want to do
this.

<a href='{{ '/assets/images/delete-fields-button.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/delete-fields-button.png' | relative_url }}' alt="
Click delete button" width='60%' style="border: 3px solid #888888;" />
</a>

• You should now have a feature layer with a reduced number of fields.

<a href='{{ '/assets/images/simplified-fields-arcgis-online.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/simplified-fields-arcgis-online.png' | relative_url }}' alt="
Click delete button" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>