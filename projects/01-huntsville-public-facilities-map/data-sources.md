# Data Sources

The goal of this sample is to show clear lineage, not to lock the workflow to one exact download path.

| Dataset type | Example source(s) | Use in the sample | Notes |
| --- | --- | --- | --- |
| OpenStreetMap roads, buildings, and points of interest | QuickOSM in QGIS, Geofabrik extracts, or another OSM-based source | Context, reference, and feature extraction | Coverage and feature detail vary by area and update cycle |
| Public facility locations | Municipal, county, state, or other public open-data portal | Primary point layer for the map | Verify license, update date, and coordinate accuracy |
| Administrative boundaries | Local government boundary data or Census-style boundary files | Study area extent and clipping | Use a projected CRS for mapping and analysis |
| Airport or transportation context | Public transportation GIS layers or OSM context features | Helps orient the map and show nearby infrastructure | Keep as context rather than as a claim about service coverage |
| Optional basemap or imagery | Public basemap services or open imagery | Visual validation only | Do not rely on it as the authoritative source for boundaries |

## Documentation notes

- Record the source name, download date, and license for every layer.
- Keep raw downloads separate from cleaned or clipped layers.
- Note when a source is incomplete or approximate.
- Avoid combining layers without documenting how they were transformed.
