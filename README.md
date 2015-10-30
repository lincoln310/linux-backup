# linux-backup

* emacs install
* ** $ sudo apt-get install build-essential
* ** $ sudo apt-get build-dep emacs24
* ** ./configure
* ** make
* ** make install

* post
* ** sudo apt-get install postgresql-9.
* ** suoo apt-get install postgresql-9.?-postgis-2.
* 

* table gis extension
* \c to table
* -- Enable PostGIS (includes raster)
* ** CREATE EXTENSION postgis;
* ** -- Enable Topology
* ** CREATE EXTENSION postgis_topology;
* ** -- Enable PostGIS Advanced 3D 
* ** -- and other geoprocessing algorithms
* ** CREATE EXTENSION postgis_sfcgal;
* ** -- fuzzy matching needed for Tiger
* ** CREATE EXTENSION fuzzystrmatch;
* ** -- rule based standardizer
* ** CREATE EXTENSION address_standardizer;
* ** -- example rule data set
* ** CREATE EXTENSION address_standardizer_data_us;
* ** -- Enable US Tiger Geocoder
* ** CREATE EXTENSION postgis_tiger_geocoder;
* 
* update data from .osm to postgis:
* ** osm2pgsql -U tsinghua -d location -H 127.0.0.1 -s -S default.style -W -a mapfile.osm
* ** default.style is in the osm2pgsql directory (github source)
* ** -a : append/update 
* ** -c : create; use this instead of -a at the first time
* ** mapfile.osm is the target.
* ** -U : username
* ** -d : database
* ** -H : host
* ** -W : password
