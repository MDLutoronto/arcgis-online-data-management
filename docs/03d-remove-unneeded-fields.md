---
title: Reduce layer complexity by removing unneeded fields  # Title of the page, which will be displayed in the navigation and the browser title.
layout: page  # Layout type, usually 'page' for standard pages.
nav_order: 3 # Order in the navigation menu.
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
can simplify it by removing the ones you don't need.

Deleting excess fields will save space on the
server and have the added benefit of giving you cleaner, more organized data
to work with. This can be done in desktop GIS software before you upload the
data, or it can be done directly in ArcGIS Online.

### Removing unneeded fields in ArcGIS Pro

Example: This layer of world country boundaries (downloaded from
<a href="https://www.naturalearthdata.com/" target="_blank">
Natural Earth</a>) has 170 fields - that's a lot! It may be, however, that you
only need a few of these fields for your work. Here's how you can remove the
ones you don't need. (As in the rest of
this guide, the steps below are shown using ArcGIS Pro, but the process is
similar in QGIS.)

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