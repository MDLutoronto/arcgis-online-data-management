---
title: Managing credits   # Title of the page, which will be displayed in the navigation and the browser title.
layout: page  # Layout type, usually 'page' for standard pages.
nav_order: 5  # Order in the navigation menu.
parent: ArcGIS Online data management
created_date: 2026-06-02 # Date when the page was created. Should be in YYYY-MM-DD format.
staff:  # Optional: Nested list of staff members associated with the page.
has_children: False
maintainer:
  - name: Cole White # PLACEHOLDER: Replace with actual maintainer's name.
    link: https://library.utoronto.ca/staff/cole-white  # link is optional

---

# Managing credits

As with feature storage, we encourage you to use credits thoughtfully. If you're
finding that you're using a lot of credits, here are some strategies and workarounds that may
help.

This isn't a comprehensive list, as there can often be many different
ways to solve a problem in GIS. If you have any questions, let us know.

## Use desktop GIS software for geoprocessing

The analysis tools in the ArcGIS Online Map Viewer consume credits. Basic
operations on smaller datasets generally use a very small number of credits and
pose no issue.
However, operations on larger datasets may consume hundreds or thousands of
credits. <b>If you're performing very intensive analyses, we recommend using
ArcGIS Pro or QGIS instead of ArcGIS Online</b>. These desktop applications also
have better file management functionality that will be to your benefit in
undertaking more complex projects.

### Geocoding and network analysis with ArcGIS Pro and StreetMap Premium

In the case of <b>geocoding</b> and <b>network analysis</b>, just using ArcGIS Pro isn't 
enough to circumvent the credit usage issue. By default, these operations will
query Esri's servers in the same way that the Map Viewer tools do, thereby
consuming credits from your account.

<b>If your project requires either of these in significant quantity, and your
study area is within North America</b>, we recommend using Esri's <b>StreetMap
Premium</b>. StreetMap Premium is a licensed data product compatible with
ArcGIS Pro. It includes downloadable network datasets
(for network analysis) and locators (for geocoding), neither of which will consume
credits.

If you think StreetMap Premium would be helpful for your work, please
<a href="https://mdl.library.utoronto.ca/about/contact-form" target="_blank">
contact the Map and Data Library</a> to request a license and a download link.

### Free geocoding with Nominatim

<a href="https://nominatim.org/" target="_blank">Nominatim</a> is a free
geocoding engine that uses OpenStreetMap data to find
locations. You can access it by writing code (in Python, for example), or in
QGIS using the <a href="https://michaelminn.com/linux/mmqgis/" target="_blank">
MMQGIS plugin</a>. There are some API limits in place, so you may
not be able to geocode a large dataset all in one go. Additionally, because
OpenStreetMap data is crowdsourced, you may find data availability varies by
region.



