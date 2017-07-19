# conda special setup details

October 2016: osgeo was removed from the old package channel - install as:

	conda install -c conda-forge gdal 

Create python environment using the following:

	conda create -n py34_mpl_gdal
	source activate py34_mpl_gdal
	conda install -c conda-forge python=3.4 gdal matplotlib ipython
	python -c "import matplotlib.pyplot"
	conda install -c conda-forge geopandas
	conda install -c conda-forge seaborn
	conda install -c menpo opencv3=3.1.0

See the issue I put up on github here: [https://github.com/ContinuumIO/anaconda-issues/issues/1166](https://github.com/ContinuumIO/anaconda-issues/issues/1166)



## Couldn;t get this to work

conda create -n py34_test_geo
source activate py34_test_geo
conda install -c conda-forge python=3.4 gdal 

conda install -c conda-forge python=3.4 matplotlib ipython
conda install -c conda-forge python=3.4 ipython georaster

python -c "import matplotlib.pyplot"
python -c "import georaster as geo"

conda install -c conda-forge geopandas
conda install -c conda-forge seaborn
conda install -c anaconda scikit-image=0.12.3

python -c "import cv2"


