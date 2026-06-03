---
title: Reduce layer complexity by simplifying geometry  # Title of the page, which will be displayed in the navigation and the browser title.
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

## Reduce a layer's complexity by simplifying its geometry

If your dataset is more <b>geometrically complex</b> (i.e., its features are very detailed
and contain many vertices) than what your project requires, you can <b>simplify
its geometry</b> in desktop GIS software before sharing it to ArcGIS Online.

Example: This layer (downloaded from the
<a href="https://data.grandriver.ca/downloads-geospatial.html" target="_blank">
Grand River Conservation website</a>) shows
wetland areas within Ontario's Grand River watershed. The polygon boundaries
have been precisely delineated. If you're performing an analysis of wetlands
where this precision matters, you may need this extra detail. But if that extra
precision isn't needed, you can save space by <b>generalizing</b> the features.

<b>
Jump to: 
<a href='#simplifying-geometry-in-arcgis-pro'>ArcGIS Pro instructions</a> |
<a href='#simplifying-geometry-in-qgis'>QGIS instructions</a>
</b>

### Simplifying geometry in ArcGIS Pro

• Open the <b>Simplify Polygon</b> (or Simplify Line if working with a line
layer) geoprocessing tool.

<a href='{{ '/assets/images/simplify-polygon-tool-pro.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/simplify-polygon-tool-pro.png' | relative_url }}' alt="
Simplify Polygon tool." width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• Specify the layer to be simplified as the <b>Input features</b>. The other
parameters will vary based on the nature of your data and your project's goals. You may want to 
experiment until you get an output that's a good trade off between simplifying
the layer and retaining the spatial information you need. In this example, <b>critical points</b> are
prioritized, features are generalized within a <b>100-metre tolerance</b>, and <b>features
smaller than 50,000m² are removed</b>. Once you've specified your parameters,
click the <b>Run</b> button.

<a href='{{ '/assets/images/simplify-polygon-parameters.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/simplify-polygon-parameters.png' | relative_url }}' alt="
Simplify Polygon tool parameters." width='60%' style="border: 3px solid #888888;" />
</a>

• The result will be a new layer with <b>simplified geometry</b>. When uploaded
to ArcGIS Online, its feature storage usage will be reduced (in this
example, the layer's feature storage usage was reduced by about 85%)!

<b>Before</b>:

<a href='{{ '/assets/images/simplify-before.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/simplify-before.png' | relative_url }}' alt="
Layer before simplification" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

<b>After</b>:

<a href='{{ '/assets/images/simplify-after-critical-points.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/simplify-after-critical-points.png' | relative_url }}' alt="
Layer after simplification (retain critical points)" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

Note: If you would like to retain the <b>curvature</b> of features for cartographic purposes
(i.e., you want something that looks nicer than the jagged polygons in the
output shown above), select <b>Retain critical bends (Wang-Müller)</b> for the
Simplification Algorithm parameter of the tool. This won't reduce the file size
as dramatically, but can still make a big difference.

More information on the 
Simplify Polygon tool and its parameters are available on its 
<a href="https://doc.esri.com/en/arcgis-pro/latest/tool-reference/cartography/simplify-polygon.html?tabs=dialog"
target="_blank">documentation page</a>.

You may also want to try some of the other tools available in ArcGIS Pro's
<b>Generalization toolset</b>. You can learn more about them 
<a href="https://doc.esri.com/en/arcgis-pro/latest/tool-reference/cartography/an-overview-of-the-generalization-toolset.html"
target="_blank">here</a>.

### Simplifying geometry in QGIS
• Open QGIS and load your layer.

<a href='{{ '/assets/images/layer-to-smooth-in-qgis.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/layer-to-smooth-in-qgis.png' | relative_url }}' alt="
Layer to simplify in QGIS" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• From the <b>Processing Toolbox</b> open the <b>Vector geometry -> Simplify</b>
tool.

<a href='{{ '/assets/images/qgis-simplify-tool.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-simplify-tool.png' | relative_url }}' alt="
Processing Toolbox -> Vector geometry -> Simplify" width='70%' style="border: 3px solid #888888;" />
</a>

• Select your layer as the <b>Input layer</b>, and save the <b>simplified output</b>
to your filesystem as a <b>shapefile</b>. You can experiment with different values
for the <b>Simplification method</b> and <b>Tolerance</b> parameters until
you arrive at something that's a good trade-off between reducing the layer's
complexity and retaining the information you need. Click <b>Run</b>.

<a href='{{ '/assets/images/qgis-simplify-tool-params.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-simplify-tool-params.png' | relative_url }}' alt="
Processing Toolbox -> Vector geometry -> Simplify" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

• The result will be a geometrically simplified layer. When uploaded to
ArcGIS Online, it will use less storage space (in this example, feature
storage consumption was reduced by 85%).

<b>Before</b>:

<a href='{{ '/assets/images/qgis-simplify-before.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-simplify-before.png' | relative_url }}' alt="
Layer before simplification" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

<b>After</b>:

<a href='{{ '/assets/images/qgis-simplify-after.png' | relative_url }}' target="_blank">
<img src='{{ '/assets/images/qgis-simplify-after.png' | relative_url }}' alt="
Layer after simplification" width='100%' height='100%' style="border: 3px solid #888888;" />
</a>

If you'd like to try some simplification tools with more options, we recommend
the <a href="https://plugins.qgis.org/plugins/geo_sim_processing/"
target="_blank">Geo Simplification plugin</a> for QGIS.

To further simplify
your results, you might additionally want to query and delete the smallest features from
the layer (see <a href='{{ '/03c-subsetting-data/#subsetting-in-qgis' | relative_url }}' target="_blank">Subsetting data in QGIS</a>).