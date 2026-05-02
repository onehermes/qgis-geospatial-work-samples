# Huntsville Public Facilities Map - QGIS Workflow Sample

This sample describes a reproducible QGIS workflow for building a public-facilities reference map with open data. It is written as a work sample to show analysis thinking, cartographic judgment, and documentation discipline.

## Objective

Produce a clear city-context map that shows public facilities against transportation and administrative reference layers. The deliverable should be easy to reproduce in QGIS and should not rely on proprietary datasets.

## Dataset types

- OpenStreetMap roads, buildings, and points of interest
- Public facility locations from an open municipal, county, state, or other public directory
- Administrative boundaries for the study area
- Airport or transportation context layers
- Optional basemap or aerial reference for visual checking only

## QGIS workflow steps

1. Set the project CRS to a projected coordinate system suitable for distance-aware mapping.
2. Load the boundary layer and clip or zoom to the Huntsville study area.
3. Add OpenStreetMap reference layers for roads, buildings, and points of interest.
4. Add the public facility layer and normalize names, categories, and address fields.
5. Filter to the features that belong in the map and keep the raw data untouched.
6. Symbolize context layers first, then facilities, then labels and annotation.
7. Build a layout with title, legend, scale bar, data sources, and projection note.
8. Export a PDF and image preview for portfolio use.

## Layer organization

Keep raw data separate from derived layers, then group the QGIS layer panel by purpose:

- Administrative boundary
- Transportation context
- Public facilities
- Labels and annotation
- Export or layout outputs

Example naming pattern:

- `admin_boundary`
- `ref_roads_osm`
- `ref_buildings_osm`
- `facilities_public`
- `layout_map_export`

## Symbology choices

- Roads: light gray, thin lines, low visual priority
- Buildings: muted fill with transparency so the map does not look heavy
- Facilities: categorized symbols by facility type with a limited color palette
- Administrative boundary: stronger outline to anchor the study area
- Airport or transportation context: distinct but subdued so it remains contextual
- Labels: only the most relevant features, with scale-dependent visibility

## Expected output map

The expected output is a clean portfolio map that shows the study area, public facilities, and supporting context in a readable composition. The map should include a title, legend, scale bar, north arrow if useful, and a source note that identifies the public datasets used.

## Quality checks

- Confirm that all layers use the same projected CRS
- Check geometry validity before styling or exporting
- Verify that facility names, categories, and addresses are complete enough for the map purpose
- Review label collisions and feature overlaps at the intended map scale
- Confirm that the legend matches the visible symbols
- Confirm that the source note and date notes are present in the layout
- Make sure the map does not imply more precision than the source data provides

## Limitations

- Open data completeness varies by area and update cycle
- OpenStreetMap coverage can differ across neighborhoods and feature types
- Public facility status, names, and locations can change after export
- The map is a documentation sample, not an authoritative operational dataset
- It should not be treated as emergency-response or legal-record evidence

## Related files

- [Workflow details](workflow.md)
- [Data-source notes](data-sources.md)
- [Map preview placeholder](outputs/placeholder-map-preview.md)
