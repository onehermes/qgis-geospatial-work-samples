# AI-Generated QGIS Output Review

## Fake AI-generated GIS instruction example

> Open QGIS, load a basemap, and draw a 5-mile buffer around the selected site. Use the buffer to show the service area and intersect it with nearby facilities to prove coverage. Export the map once it looks clear.

## Review

This answer is directionally useful, but it is not ready to follow as written.

1. CRS and projection guidance are missing.
   Distance work needs a projected CRS, or the buffer units may be wrong.

2. Data sources are unclear.
   The instruction does not say where the site, facilities, or boundary layers come from.

3. Buffer units are ambiguous.
   A 5-mile buffer is not actionable unless the QGIS units and CRS are specified.

4. Validation steps are missing.
   There is no geometry check, no attribute review, and no verification that the layers align.

5. The result is overstated.
   A straight-line buffer does not prove real service coverage.

6. Limitations are not stated.
   The answer should note that network access, barriers, and field conditions are not modeled.

## Improved version

1. Set the QGIS project CRS to a projected coordinate system suitable for local distance work.
2. Load the site point, boundary layer, public facility layer, and road layer from documented public sources.
3. Confirm each layer's geometry and attribute fields before analysis.
4. Create buffers around the site at 1, 3, and 5 miles, using the project CRS units or documented conversions.
5. Intersect the buffer zones with roads, neighborhoods, and facilities to summarize nearby features.
6. Review the map for alignment, duplicates, missing data, and labeling issues.
7. Export the map with a source note and a limitation statement that explains that buffer rings are proximity zones, not network travel-time service areas.

This is the version I would be comfortable using as a portfolio-quality GIS workflow note.
