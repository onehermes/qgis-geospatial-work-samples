# Workflow

This workflow shows how I would build and review a buffer-based accessibility concept in QGIS.

## 1. Select the analysis point

- Choose a point of interest with a clear purpose.
- Verify that the point is correctly geocoded or manually placed.
- Record the source and date for the point layer.

## 2. Set the spatial reference

- Use a projected CRS before measuring distance.
- Keep all analysis layers in the same CRS or reproject them consistently.
- Document the CRS so the buffer units are unambiguous.

## 3. Create the buffer zones

- Run the Buffer tool for 1 mile, 3 miles, and 5 miles.
- Convert the distances to the project units when the CRS is not already in miles or feet.
- Decide whether the result should be nested buffers or separate rings.
- If separate bands are needed, use Difference or a similar overlay step to create non-overlapping zones.

## 4. Compare surrounding layers

- Intersect the buffer zones with roads, neighborhoods, or public facility layers.
- Use Select by Location if a simpler inclusion check is sufficient.
- Summarize the features inside each zone if the goal is a quick accessibility screen.

## 5. Review the result

- Inspect the geometry of the buffer rings.
- Check that the map extent shows the relevant context.
- Make sure the legend reflects the layer structure and the chosen distances.
- Add a note that explains the analysis is straight-line proximity, not network service area.

## 6. Export and document

- Export the map to PDF or PNG.
- Save the QGIS project file.
- Keep the source notes and the CRS note with the export.
- Record limitations in the project README or layout notes.
