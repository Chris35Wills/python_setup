# conda special setup details

October 2016: osgeo was removed from the old package channel - install as:

	conda install -c conda-forge gdal 

Create python environment using the following:

	conda create -n py34_mpl_gdal
	source activate py34_mpl_gdal
	conda install -c conda-forge python=3.4 gdal matplotlib ipython
	python -c "import matplotlib.pyplot"

See the issue I put up on github here: [https://github.com/ContinuumIO/anaconda-issues/issues/1166](https://github.com/ContinuumIO/anaconda-issues/issues/1166)