## Columns Overview - Analysis Dataset
| Column Name | Type | Description | Definition | 
|-------------|------|-------------|------------|
| name | text | river and stream name | Geographical representation of each river and stream located in the Philippines. |
| waterway | text | either `river` or `stream` | Determines whether it is a large river or just a stream. | 
| Region / Province / City_Muni | text | boundaries covered by each river or stream | Location of each river or stream. |
| Catchment | text | Catchment basin name | Which watershed or drainage the river,stream belongs to. | 
| Catch_area (km²) | numeric | Catchment area | Determines how big is the drainage basin feeding this river. Which is useful in determining usability. |
| Relief_m (m) | numeric | Catchment relief (elevation difference) | Determines how steep is the terrain from top to bottom. | 
| Runoff_mm (mm/yr) | numeric | Annual runoff from PNHMD | Determines how much rainwater flows off per year on average. |
| Flow_m3s (m³/s) | numeric | Estimated discharge | Determines how much water flows through the river per second. |
| Power_MW (MW) | numeric | Theoretical hydropower potential | Determines how much power could be generated in theory. | 
| HPI (0–100) | numeric | Hydropower Potential Index | Combined score for suitability; higher = better. | 
| Status | text | HPI Qualitative classification | Determines whether a specific river or stream is `Excellent`, `Good`, `Moderate`, or `Poor`. |
| geometry / geometry_wkt | geometry / text | River geometry (LINESTRING or MULTILINESTRING) | The actual line of the river drawn on the map. | 
