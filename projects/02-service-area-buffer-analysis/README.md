# Service Area / Buffer Analysis - Accessibility Concept Sample

This sample shows a reproducible QGIS workflow for a simple accessibility analysis built around concentric buffers. It is intentionally framed as a concept sample so the method and its limits are clear.

## Objective

Choose a point of interest, create 1-mile, 3-mile, and 5-mile buffer zones, and compare what falls inside each zone. The purpose is to demonstrate distance-based GIS thinking, not to claim a full travel-time service area.

## Dataset types

- A single point of interest, such as a facility, station, or public site
- Road or street context
- Neighborhood or administrative boundaries
- Public facility points for comparison
- Optional land-use or parcel layers if they help explain the setting

## QGIS tools used

- Project Properties for CRS selection
- Reproject Layer or on-the-fly projection handling
- Buffer
- Dissolve
- Intersection
- Clip
- Select by Location
- Field Calculator
- Layout Manager

## Step-by-step workflow

1. Choose the point of interest and confirm that its location is correct.
2. Set the project to a projected CRS so distance measurements are meaningful.
3. Create buffers at 1 mile, 3 miles, and 5 miles around the point.
4. If needed, convert the distances to the project units and document the conversion.
5. Dissolve or keep the buffers separate depending on whether the goal is nested zones or distinct bands.
6. Intersect the buffers with roads, neighborhoods, or public facility layers.
7. Summarize the features that fall inside each zone.
8. Style the map so the rings read clearly and the context layers remain subordinate.
9. Add a note that explains the analysis is proximity-based, not network-based.

## Interpretation

The smaller buffer represents the closest area of influence, while the larger buffers show progressively broader proximity. That can be useful for planning conversations, but it does not prove actual accessibility in the real world.

Straight-line buffers ignore barriers, route direction, traffic, sidewalk continuity, slope, and actual travel time. For a stronger accessibility analysis, a network service-area or isochrone workflow would be more appropriate.

## Quality checks

- Confirm that the project CRS is projected before measuring distance
- Confirm that the buffer distances match the CRS units
- Confirm that the point of interest is in the correct location
- Check that clipped or intersected layers still cover the intended study area
- Review results for duplicates, missing attributes, and geometry issues
- Avoid language that turns proximity into a claim about real service coverage

## Limitations

- Buffer zones are an approximation, not a travel network analysis
- Distance results depend on the chosen CRS and unit conversion
- Road access, pedestrian access, and physical barriers are not modeled
- Any counts or summaries are only as reliable as the input data

## Related files

- [Workflow details](workflow.md)
- [Data-source notes](data-sources.md)
- [Map preview placeholder](outputs/placeholder-map-preview.md)
