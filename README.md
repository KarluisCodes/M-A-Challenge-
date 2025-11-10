# 10th edition PwC M&A Challenge 2025
A dynamic platform for students to develop and expand their skills in tackling real-world business tasks designed to test and enhance their business acumen. Participants will work on an M&A case, focusing on key aspects of energy transition, and provide insights on better managing this transition to generate long-term value for clients.

## Repower Energy Development Corporation 
The company assigned to the group is <b> Repower Energy Development Corporation, </b> a Philippine renewable energy company focused on developing run-of-river hydropower projects. As a wholly-owned subsidiary of Pure Energy Holdings Corporation, REDC utilizes a "clustered approach" to share infrastructure and reduce costs for its hydropower plants

## Dataset 

1. PSE Philippines
   - This dataset was gathered through webscrapping PSE accredited hydropowered companies. 
2. River Dataset
   - This dataset was gathered through publicly sourced geospatial and Philippine waterway datasets. Sources specifically from:
     | Dataset | Description | Format | Purpose |
     |---------|-------------|--------|---------|
     |OSM Hydrography | OpenStreetMap of Philippine rivers and streams | GeoJSON / Shapefile | Provides the base geometrics of all Philippine listed river lines and streams|
     |Philippine GIS Catchments | Catchment boundaries and location data | Shapefile | Provides the physical basin metrics such as the <b> area, slope, and elevation </b> which is useful to determine its usability for Hydropowered projects. |
     | Philippine National Hydrological Model Dataset | Modeling dataset used to determine long-term average runoff by province. | CSV | Provides hydrologic runoff used to estimate discharge and hydropower. Helps determine energy per stream and river. |

## Estimated Hydropower 
In the River_dataset there is a column with `Status` which is a categorical label derived from the HPI score, summarizing overall hydropower suitability. Below is how it was computed: 

$$
P = \rho g Q H \eta
$$

where:

- \( \rho = 1000 \, \text{kg/m}^3 \) — water density  
- \( g = 9.81 \, \text{m/s}^2 \) — gravitational acceleration  
- \( Q \) — discharge (m³/s)  
- \( H \) — catchment relief (m)  
- \( \eta = 0.75 \) — assumed efficiency factor
     
