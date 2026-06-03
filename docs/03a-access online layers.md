---
title: Access online layers   # Title of the page, which will be displayed in the navigation and the browser title.
layout: page  # Layout type, usually 'page' for standard pages.
nav_order: 0  # Order in the navigation menu.
parent: Managing feature storage
grand_parent: ArcGIS Online data management
created_date: 2026-05-29 # Date when the page was created. Should be in YYYY-MM-DD format.
staff:  # Optional: Nested list of staff members associated with the page.
maintainer:
  - name: Cole White # PLACEHOLDER: Replace with actual maintainer's name.
    link: https://library.utoronto.ca/staff/cole-white  # link is optional

---

## Access online layers
You can avoid making unnecessary uploads (and the creation of new hosted feature
layers) by accessing data layers that others have already added to the ArcGIS
Online ecosystem.

In particular, the 
<a href="https://livingatlas.arcgis.com/en/home/" target="_blank">ArcGIS
Online Living Atlas</a>, Esri's curated collection of authoritative, free-to-use
spatial datasets is a good place to start looking.

<b>To search for and add Living Atlas layers to your own ArcGIS Online project:</b>

• Log in to ArcGIS Online. Click the <b>Map</b> tab to open the Map Viewer (or open
an existing web map that you own).

<a href='{{ '/assets/images/open-map-viewer.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/open-map-viewer.png' | relative_url }}' alt="
Open the Map Viewer." width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Click the <b>Add</b> button.

<a href='{{ '/assets/images/click-add-button.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/click-add-button.png' | relative_url }}' alt="
Click the Add button." width='100%' height='100%' style="border: 3px solid #888888;"  />
</a>

• Click the dropdown, and select <b>Living Atlas</b>

<a href='{{ '/assets/images/click-living-atlas.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/click-living-atlas.png' | relative_url }}' alt="
Click the Add button." width='100%' height='100%' style="border: 3px solid #888888;"  />
</a>

• Search for layers by name, Item ID, or owner. Click <b>Add</b> to add them
to your map.

<a href='{{ '/assets/images/add-to-map.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/add-to-map.png' | relative_url }}' alt="
Click the Add button." width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

You can also search within the <b>broader ArcGIS Online platform (not just
Living Atlas)</b> for reusable data, but make sure
it comes from an authoritative source.

If you know the ArcGIS Online username of a good source,
you can search for datasets they own using the 'owner:' flag.
For example, if you search within
ArcGIS Online with the query '<b>owner:landinformationontario</b>', all of 
<a href="https://geohub.lio.gov.on.ca" target="_blank">Geospatial
Ontario's</a> official datasets will be returned - no need to download and re-upload
them.

<a href='{{ '/assets/images/geospatial-ontario-search.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/geospatial-ontario-search.png' | relative_url }}' alt="
Browse layers -> owner:landinformationontario" width='100%' height='100%'  style="border: 3px solid #888888;" />
</a>

Additionally, it may be helpful to search within ArcGIS Online and apply a <b>filter</b> to return
<b>'authoritative' results only</b>. Example:

<a href='{{ '/assets/images/authoritative-search.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/authoritative-search.png' | relative_url }}' alt="
Filters -> Status -> Authoritative" width='100%' height='100%'  style="border: 3px solid #888888;" />
</a>

Note that some ArcGIS Online and Living Atlas layers might have certain
capabilities, such as exporting the layer to a new format, turned off.
Additionally, some of these layers may only display the features and not
allow access to the underlying attributes. You should check the metadata for
any other usage notes or licensing considerations.