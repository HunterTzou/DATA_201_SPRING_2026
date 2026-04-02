ZIPCODES Shapefile – File Reference
=====================================

This folder contains the official Montgomery County zip code boundary files
obtained from the Montgomery County open data portal. These files are used
to filter and validate zip codes in the food inspection dataset and to
enable geographic (choropleth) mapping of inspection and compliance data.

-------------------------------------
FILE DESCRIPTIONS
-------------------------------------

ZIPCODES.shp
  The main shapefile containing the polygon geometry (boundary shapes) for
  each zip code in Montgomery County. This is the primary file used by GIS
  tools and geopandas to draw and analyze geographic boundaries.

ZIPCODES.shx
  The shape index file. Required companion to ZIPCODES.shp — it allows
  software to quickly locate and access individual records within the .shp
  file. Must be present in the same directory as the .shp file.

ZIPCODES.dbf
  The attribute table stored in dBASE format. Contains the data associated
  with each zip code polygon (e.g., zip code number, place name). Can be
  read independently with pandas or simpledbf to extract the official list
  of Montgomery County zip codes without loading the full geometry.

ZIPCODES.prj
  The projection file. Defines the coordinate reference system (CRS) used
  by the shapefile (e.g., WGS84, NAD83). Required for accurate spatial
  operations and for aligning the boundaries with other geographic datasets
  such as latitude/longitude coordinates from the inspection data.

ZIPCODES.cpg
  The code page file. Specifies the character encoding used in the .dbf
  attribute table (typically UTF-8 or ISO-8859-1). Ensures text fields
  like place names display correctly.

ZIPCODES.sbn
  A spatial index file used by Esri software (e.g., ArcGIS) to speed up
  spatial queries. Not required for use with geopandas or QGIS, but
  included for completeness.

ZIPCODES.sbx
  The companion index file to ZIPCODES.sbn. Also Esri-specific and not
  required for use with geopandas or QGIS.

-------------------------------------
USAGE NOTES
-------------------------------------

To use these files in Google Colab with geopandas, the following files
must all be present in the same directory:
  - ZIPCODES.shp
  - ZIPCODES.shx
  - ZIPCODES.dbf
  - ZIPCODES.prj (recommended)

The .sbn, .sbx, and .cpg files are optional for Python-based workflows.

-------------------------------------
SOURCE
-------------------------------------

Montgomery County, Maryland Open Data Portal
https://www.montgomerycountymd.gov
