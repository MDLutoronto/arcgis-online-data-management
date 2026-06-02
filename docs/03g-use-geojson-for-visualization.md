---
title: Use GeoJSON for simple visualization   # Title of the page, which will be displayed in the navigation and the browser title.
layout: page  # Layout type, usually 'page' for standard pages.
nav_order: 6  # Order in the navigation menu.
parent: Managing feature storage
grand_parent: ArcGIS Online data management
created_date: 2026-05-29 # Date when the page was created. Should be in YYYY-MM-DD format.
staff:  # Optional: Nested list of staff members associated with the page.
maintainer:
  - name: Cole White # PLACEHOLDER: Replace with actual maintainer's name.
    link: https://library.utoronto.ca/staff/cole-white  # link is optional

---

## Use GeoJSON for simple visualization

Hosted feature layers are a special file format that supports ArcGIS Online's
editing and analysis tools. If you only need to <b>visualize</b> your data,
consider using <b>GeoJSON</b> (a lightweight spatial data format often
used on the Web) instead.

You can export data in GeoJSON format from
ArcGIS Pro. Alternatively, if your data is already in ArcGIS Online, you can
convert it there and then delete your original hosted feature layer.

### Creating a GeoJSON file in ArcGIS Pro

• Load your data layer into ArcGIS Pro. Search for <b>Features to JSON</b>
in the Geoprocessing Toolbox.

<a href='{{ '/assets/images/features-to-json.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/features-to-json.png' | relative_url }}' alt="
ArcGIS Pro Features to JSON tool" width='100%' height='100%'
style="border: 3px solid #888888;" />
</a>

• Open the Features to JSON tool. Specify your spatial layer as the <b>Input
Features</b>. Save the file to your computer. Check the <b>Output to
GeoJSON</b> and <b>Project to WGS84</b> boxes. Click <b>Run</b>.

<a href='{{ '/assets/images/features-to-json-params.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/features-to-json-params.png' | relative_url }}' alt="
ArcGIS Pro Features to JSON tool parameters" width='60%'
style="border: 3px solid #888888;" />
</a>

• The tool should output a <b>.geojson</b> file to your computer's filesystem.
Make sure the file is <b>under 100 MB</b> - that's the maximum size ArcGIS Online
will support for GeoJSON.

<a href='{{ '/assets/images/geojson-output.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/geojson-output.png' | relative_url }}' alt="
GeoJSON output file in Windows Explorer" width='100%' height='100%'
style="border: 3px solid #888888;" />
</a>

• <b>Log in to ArcGIS Online</b> and visit your <b>Content</b> section.

<a href='{{ '/assets/images/arcgis-online-content.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/arcgis-online-content.png' | relative_url }}' alt="
ArcGIS Online -> Content -> My Content" width='100%' height='100%'
style="border: 3px solid #888888;" />
</a>

• Click the <b>New Item</b> button.

<a href='{{ '/assets/images/content-new-item.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/content-new-item.png' | relative_url }}' alt="
New item" width='100%' height='100%'
style="border: 3px solid #888888;" />
</a>

• Choose <b>Your Device</b>.

<a href='{{ '/assets/images/new-item-your-device.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/new-item-your-device.png' | relative_url }}' alt="
New Item -> Your Device" width='100%' height='100%'
style="border: 3px solid #888888;" />
</a>

• Navigate to your GeoJSON file, select it, and click <b>Open</b>.

<a href='{{ '/assets/images/select-geojson-file.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/select-geojson-file.png' | relative_url }}' alt="
Open the GeoJSON file to upload it" width='100%' height='100%'
style="border: 3px solid #888888;" />
</a>

• <b><u>This is the important part:</u></b> click the <b>second option</b> shown here to add the
GeoJSON data <b>without creating a hosted feature layer</b>. Click
<b>Next</b>.

<a href='{{ '/assets/images/geojson-only.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/geojson-only.png' | relative_url }}' alt="
GeoJSON only - do not create a hosted feature layer" width='100%' height='100%'
style="border: 3px solid #888888;" />
</a>

• Give the new item a name, and optionally input other metadata. Click <b>
Save</b>.

<a href='{{ '/assets/images/new-item-details.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/new-item-details.png' | relative_url }}' alt="
GeoJSON only - do not create a hosted feature layer" width='100%' height='100%'
style="border: 3px solid #888888;" />
</a>

• You'll now be shown the <b>Item Details page</b> for the new GeoJSON layer. From
here, it can be added to your ArcGIS Online projects and visualized in the
Map Viewer.

<a href='{{ '/assets/images/geojson-item-details-page.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/geojson-item-details-page.png' | relative_url }}' alt="
GeoJSON Item Details page" width='100%' height='100%'
style="border: 3px solid #888888;" />
</a>

### Creating a GeoJSON file in ArcGIS Online
• Log in to ArcGIS Online. Navigate to the <b>Item Details page</b> of the hosted feature layer you'd like
converted to GeoJSON.

<a href='{{ '/assets/images/item-details-page.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/item-details-page.png' | relative_url }}' alt="
Item details page of the hosted feature layer" width='100%' height='100%'
style="border: 3px solid #888888;" />
</a>

• Choose <b>Export data -> Export to GeoJSON</b> from the pane on the right of the
page.

<a href='{{ '/assets/images/export-to-geojson.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/export-to-geojson.png' | relative_url }}' alt="
Export to GeoJSON" width='100%' height='100%'
style="border: 3px solid #888888;" />
</a>

• Give the GeoJSON file a descriptive name. Optionally fill in the
other metadata fields. Click <b>Export</b>. (The process might take some time,
depending on the size of the dataset.)

<a href='{{ '/assets/images/export-to-geojson-arcgis-online.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/export-to-geojson-arcgis-online.png' | relative_url }}' alt="
Export to GeoJSON" width='70%' style="border: 3px solid #888888;" />
</a>

• When the export has completed, you'll be brought to the <b>Item Details page</b>
for the new GeoJSON layer. You can now add this layer to your projects and
visualize it in the Map Viewer.

<a href='{{ '/assets/images/new-geojson-layer.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/new-geojson-layer.png' | relative_url }}' alt="
Item details page of the new GeoJSON layer" width='70%' style="border: 3px solid #888888;" />
</a>

• Now you'll need to <b>delete the original hosted feature layer</b>. To do this,
navigate back to its Item Details page and click <b>Settings</b>

<a href='{{ '/assets/images/item-details-settings.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/item-details-settings.png' | relative_url }}' alt="
Item details -> Settings" width='70%' style="border: 3px solid #888888;" />
</a>

• Click the <b>Delete Item</b> button.

<a href='{{ '/assets/images/delete-item-arcgis-online-2.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/delete-item-arcgis-online-2.png' | relative_url }}' alt="
Item details -> Settings" width='70%' style="border: 3px solid #888888;" />
</a>

• Click <b>Show More</b>.

<a href='{{ '/assets/images/show-more.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/show-more.png' | relative_url }}' alt="
Delete item -> Show More" width='70%' style="border: 3px solid #888888;" />
</a>

• Click <b>Delete permanently (cannot be undone).</b>

<a href='{{ '/assets/images/delete-permanently-2.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/delete-permanently-2.png' | relative_url }}' alt="
Delete item -> Show More -> Delete permanently" width='70%' style="border: 3px solid #888888;" />
</a>