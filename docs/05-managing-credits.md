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
finding that your work is consuming a lot of credits, here's a 
noncomprehensive list of potentially helpful strategies and workarounds.


## Use desktop GIS software for geoprocessing

The analysis tools in the ArcGIS Online Map Viewer consume credits. Basic
operations on smaller datasets generally use a very small number of credits and
pose no issue.
However, operations on larger datasets, or workflows that require repeated
tool executions, may consume thousands of
credits. <b>If you're performing very intensive analyses, we recommend using
ArcGIS Pro or QGIS instead of ArcGIS Online</b>. These desktop applications also
have better file management functionality that will be to your benefit when
undertaking more complex projects.

## Notes on geocoding

<b>Geocoding</b> is the process of converting natural language street addresses to geographic
points. It works by applying a matching algorithm between your addresses (or other
types of locations, in some cases) and a database of known addresses and
their corresponding geographic locations. In GIS, this type of database is often
called a <b>locator</b>. A locator may take the form of a <b>cloud-based
service</b> that you query for information, or as <b>local data</b> on your
computer.

Cloud-based locators are the more convenient option, but often involve a fee (or
in the case of ArcGIS, credits), and there may be limitations on how much you
can use them. With local options, on the other hand, it can be quite challenging to find and compile comprehensive,
up-to-date street and address information. Additionally, the locator files may
be quite large, and the geocoding process can take considerable time on less
powerful computers.

### Geocoding in ArcGIS Pro - using offline locators

Unlike many other geoprocessing operations, <b>just using ArcGIS Pro instead of
ArcGIS Online for geocoding isn't enough to circumvent the credit usage
issue</b>. Unless otherwise configured, geocoding in Pro will still query Esri's
cloud-based locator to get geographic information from your addresses. This is
the exact same thing that the ArcGIS Online Map Viewer version of the tool does, and it will
still eat up credits from your account. Using a local, offline locator can
solve this problem. Here are some options for your consideration:

* <b>StreetMap Premium</b>: If your study area is within North America, we recommend using Esri's <b>StreetMap
Premium North America</b> as an alternative to their web-based geocoding service. StreetMap
Premium is a licensed data product
designed to work with ArcGIS Pro, and includes offline locators. If you think StreetMap Premium would be helpful for your work, please
<a href="https://mdl.library.utoronto.ca/about/contact-form" target="_blank">
contact the Map and Data Library</a> to request a license and a download link.

* <b>Open, downloadable locators</b>: <b>Free ArcGIS Pro locators</b> are available from the
<a href="https://github.com/Avdikas/open-arcgis-pro-offline-locators/"
target="_blank">Open ArcGIS Pro Offline Locators</a> project. These use
OpenStreetMap as a spatial backend, are downloadable by region, and are
already packaged as ArcGIS Pro-compatible files. However, you may find
that these locators are less sophisticated than official or commercial
offerings, and that your results may vary by region. (An an example, the
United Kingdom locator found locations for about 68% of an official Ordnance
Survey dataset of addresses in Inverness, Scotland.)

* <b>Create a custom locator</b>: Although it can require significant data preparation, it is possible to create
your own locator in ArcGIS Pro. More information about this is available
in their <a href="https://doc.esri.com/en/arcgis-pro/latest/help/data/geocoding/fundamentals-of-creating-a-locator.html" target="_blank">documentation</a>.

### Alternative web service geocoding options 

Outside of Esri's ecosystem, here are some <b>web-based geocoders</b> you may be
interested in:

<b><a href="https://nominatim.org/" target="_blank">Nominatim</a></b> is a <b>free
geocoding engine</b> that uses OpenStreetMap data to find
locations. You can access it by writing code (in Python, for example), or in
QGIS using the <a href="https://michaelminn.com/linux/mmqgis/" target="_blank">
MMQGIS plugin</a>. There are, however, some fairly strict API limits in place -
it's not designed for bulk geocoding (see their usage policy 
<a href="https://operations.osmfoundation.org/policies/nominatim/"
target="_blank">here</a>). Additionally, because
OpenStreetMap data is crowdsourced, you may find that the accuracy of your
geocoding output varies by region.

Alternatively, there are various commercial geocoding services that offer a
free tier. You might try <a href="https://www.geoapify.com/pricing/" target="_blank">
Geoapify</a>, <a href="https://opencagedata.com/pricing" target="_blank">
OpenCage</a>, or <a href="https://locationiq.com/" target="_blank">
LocationIQ</a> and see if their free versions meet your needs. After signing up
for one of these services, you will be able to generate an API key - a password
for accessing their data and performing geocoding.

## Notes on network analysis

<img src='{{ '/assets/images/network-analysis-graphic.png' | relative_url }}' alt="
Network analysis - shortest route between two points on a map" width='100%' height='100%' />

<b>Network analysis</b> in GIS models movement within connected spatial infrastructure - for example, determining the shortest driving route between two or more
locations. In ArcGIS Pro, the source of this information can be an
online <b>network data source</b>, or an offline <b>network dataset</b>. As
with geocoding, an online data source may be more convenient, but will generally
come with usage restrictions and costs (credits, in the case of ArcGIS). An
offline network dataset is more flexible, but you'll need to obtain or create
the (sometimes quite large and complex) input data.

Smaller analyses will not consume prohibitive amounts of credits. However,
if you're faced with a more intensive task, you may need to find an alternative
to Esri's cloud-based network analysis solver. Here's a non-comprehensive
list of options you might want to try:

* If your study area is within North America, we can provide you with <b>offline
network datasets</b> from Esri's <b>StreetMap Premium North America</b> product.
<a href="https://mdl.library.utoronto.ca/about/contact-form" target="_blank">
Contact the Map and Data Library</a> for more information.

* The <b><a href="https://root676.github.io/" target="_blank">QNEAT3</a>
plugin for QGIS</b> provides tools for generating shortest paths,
origin-destination matrices, service area polygons, and more. You will need,
however, to provide a street network layer as an input.

* If you are comfortable with Python (or would like to learn), the 
<b><a href="https://osmnx.readthedocs.io/en/stable/" target="_blank">OSMnx</a> and
<a href="https://networkx.org/en/" target="_blank">NetworkX</a> libraries</b> can be
used together to perform network analysis using OpenStreetMap data.





