# Workflow

This workflow is written so it can be followed in QGIS with public data and documented assumptions.

## 1. Prepare the project

- Start a new QGIS project.
- Set the project CRS to a projected coordinate system appropriate for local mapping.
- Create folders for raw data, processed layers, and exports.
- Record source dates and license notes before analysis starts.

## 2. Load reference data

- Add the administrative boundary for the Huntsville study area.
- Add OpenStreetMap roads, buildings, and points of interest.
- Add transportation or airport context layers if they help orient the map.
- Add an optional basemap only as a visual reference for checking alignment.

## 3. Add the public facility layer

- Import the public facility point layer from a public directory or open-data portal.
- Review the attribute table for category, name, address, and source fields.
- Standardize field names if the source schema is inconsistent.
- Keep the source layer unchanged and create a cleaned copy if needed.

## 4. Organize the layer tree

- Group administrative layers together.
- Group transportation and OSM context layers together.
- Group facility layers together.
- Keep annotation and export layers separate from analysis layers.

## 5. Style the map

- Draw context layers first so they stay visually quiet.
- Use category-based symbols for facilities.
- Limit the palette so the map reads quickly.
- Keep text labels selective and scale-aware.
- Use transparency where a layer is supportive rather than primary.

## 6. Build the layout

- Add a clear title and subtitle.
- Add a legend that matches the final layer order.
- Add a scale bar and projection note if useful.
- Add source text that names the public datasets.
- Add a date note if the data is time-sensitive.

## 7. Review before export

- Zoom to the target scale and inspect feature placement.
- Check for missing labels, duplicate points, and cluttered overlaps.
- Confirm that the map does not overstate precision or completeness.
- Export to PDF and PNG for portfolio use.

## 8. Archive the working notes

- Save the final QGIS project file.
- Keep the source notes with the exported map.
- Record any limitations that affect interpretation.
