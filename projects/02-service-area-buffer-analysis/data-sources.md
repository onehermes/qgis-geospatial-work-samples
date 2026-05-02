# Data Sources

This sample can be reproduced with public or open data as long as the source lineage is recorded clearly.

| Dataset type | Example source(s) | Use in the sample | Notes |
| --- | --- | --- | --- |
| Point of interest | Public directory, open-data portal, or manually curated open source | Center point for the buffers | Verify that the point location is current and accurate |
| Road or street network | OpenStreetMap or a public transportation GIS layer | Context for accessibility discussion | Straight-line buffers do not model route choice or travel time |
| Neighborhood or administrative boundaries | Local government boundary data or Census-style boundaries | Helps interpret coverage by area | Use a projected CRS for distance-based work |
| Public facility points | Municipal or county open data | Comparison layer for location coverage | Check the update date and whether all categories are included |
| Optional land-use or parcel data | Public GIS open-data portal | Adds context for planning discussions | Do not overstate what the layer proves without a clear method |

## Documentation notes

- Record the CRS and distance units used for the buffers.
- Record the download date and source name for each layer.
- Keep raw and derived layers separate.
- Note when a layer is approximate or incomplete.
