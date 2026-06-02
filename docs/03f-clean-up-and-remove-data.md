---
title: Clean up and remove unused data   # Title of the page, which will be displayed in the navigation and the browser title.
layout: page  # Layout type, usually 'page' for standard pages.
nav_order: 5 # Order in the navigation menu.
parent: Managing feature storage
grand_parent: ArcGIS Online data management
created_date: 2026-05-29 # Date when the page was created. Should be in YYYY-MM-DD format.
staff:  # Optional: Nested list of staff members associated with the page.
maintainer:
  - name: Cole White # PLACEHOLDER: Replace with actual maintainer's name.
    link: https://library.utoronto.ca/staff/cole-white  # link is optional

---

## Clean up and remove unused data
As a best practice, regularly review your ArcGIS Online content and remove
anything you don't need, <i>especially</i> if it's a large feature layer.

We also encourage you to <b>offload</b> spatial data layers once you're done
with them. If you no longer need to work with or display the data in ArcGIS
Online, <b>export</b> it and save a copy to your local device, OneDrive, or 
another safe location, then <b>delete the hosted layer</b> from ArcGIS Online. 

## Exporting data from ArcGIS Online
• Navigate to the <b>Item Details</b> page of the layer you'd like to archive.
Click the <b>Export Data</b> and choose a file format (shapefile is often
a good general purpose choice for spatial data).

<a href='{{ '/assets/images/item-details-export.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/item-details-export.png' | relative_url }}' alt="
Item details -> Export data -> Export to shapefile" width='100%' height='100%'
style="border: 3px solid #888888;" />
</a>

• Specify a name and folder for the exported item, and click <b>Export</b>.
This may take some time depending on the size of the file.

<a href='{{ '/assets/images/export-data-options.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/export-data-options.png' | relative_url }}' alt="
Export data options" width='70%' style="border: 3px solid #888888;" />
</a>

• When the export has completed, you will be taken to the Item Details page
of the exported item. Click the <b>Download</b> button. The file will be
saved to your device.

<a href='{{ '/assets/images/download-item.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/download-item.png' | relative_url }}' alt="
Download the exported item" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• After the download has completed, <b>delete</b> the exported item by
clicking the Settings tab and then the <b>Delete</b> button.

<a href='{{ '/assets/images/delete-exported-item.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/delete-exported-item.png' | relative_url }}' alt="
Delete the exported item from ArcGIS Online" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Navigate to the <b>original hosted feature layer</b> and delete that too.

<a href='{{ '/assets/images/delete-feature-layer.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/delete-feature-layer.png' | relative_url }}' alt="
Delete the exported item from ArcGIS Online" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

You've now freed up space on ArcGIS Online, and you've saved a <b>local copy</b>
 of your spatial layer that you can keep as an archive. You can also work with
 the local copy in ArcGIS Pro or QGIS and re-upload it to ArcGIS Online if needed.

