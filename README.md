# SRS
SRS is a registry of spatial reference systems and transformations used by Intrepid products.
It is a snap shot of our standard "proj" directory, common to Intrepid/Geomodeller and Jetstream.
We are deprecating supplying this information with our installers, instead, asking users to get the latest from this GitHub site.

# History
This started with the early adoption of the so-called ERMapper projection/Datum pairs.
Subsequentially,POSC and UKOA came on the scene, followed by EPSG.
The dominant GIS software packages also started to make up methods to cover this same functional requirement.
As a result, Intrepid Geophysics supports most variants, and has set up methods to map equivalence across the variants.
This cross-table lives in a couple of places, but notably the "cs.csv", which is a flat table with mapping from POSC to ERmapper
and to PRJ  ie posc_code,posc_name,erm_name,prj

The list of supported datums that links POSC, PRJ and ERMapper, MapInfo formats is datum.csv

The list of supported projections in ERMapper format is proj.csv

The list of supported ellipsoids in ERMapper format is ellipsoid.csv

The list of supported coordinate systems that links POSC, PRJ and ERMapper formats is cs.csv

There is a sub-directory for gdal, which also contains a mapping table, ecw_cs.wkt, and this has the common name, followed by the PROJCS convention block structure.

MapInfo mapping is also important, for historic purposes, as they also came up with their own methods. If, for any reason, we did not get the MapInfo internal magic number right, we set it to 0. You can simply edit this to the correct number, if you know it.

## Installation
Download and unzip into a temporary directory, then replace the content in proj/ directory under <intrepid_root>/extras or <geomodeller_root>/extras with the latest version. 

(c) 2017-2019 Intrepid Geophysics
