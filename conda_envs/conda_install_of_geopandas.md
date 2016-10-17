# To make an install of geopandas (a new env was made so downgrading things didn't cock anything up!)

conda create --name py27_extra --clone py27 # clone copnda env

# based on: https://github.com/geopandas/geopandas/issues/237

# need fiona with gdal < 2 (it's not yet compatible, although conda tries to install gdal 2)
conda install fiona "libgdal<2.0"
# basic dependencies -> this possibly needs to reinstall numpy to ensure it's the correct version that pandas needs (fiona downgrades numpy, leaving an already install pandas possibly broken)
conda install pandas matplotlib
# install shapely from ioos + its dependecies
conda install -c ioos shapely pyproj
# install geopandas and descarted from ioos without updating its dependencies -> tries to update fiona/pyproj -> see problems above
conda install -c ioos geopandas descartes --no-deps

conda install -c ioos geopandas


# see also...

http://geoffboeing.com/2014/09/using-geopandas-windows/