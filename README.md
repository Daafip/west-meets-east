# Analysis for the book west meets east

This is the code to analyse data from the [NOAA NCEI](https://www.ncei.noaa.gov/) for the book east meets west:

Daily Precipitation data is downloaded in [`Download data.ipynb`](https://github.com/Daafip/west-meets-east/blob/main/Download%20data.ipynb) from [www.ncei.noaa.gov](https://www.ncei.noaa.gov/data/cmorph-high-resolution-global-precipitation-estimates/). This takes quite some time and downloads all the specified years: in this case 1998-2022. Note a seperate path might be required with little to no spacing: *....not ideal but thats just how wget works `¯\_(ツ)_/¯`*.

These seperate files can then be combine in [`Combine_nc_files.ipynb`](https://github.com/Daafip/west-meets-east/blob/main/Combine_nc_files.ipynb) to make a single, larger netcdf file.

These files are then read in [`Read_nc_Files.ipynb`](https://github.com/Daafip/west-meets-east/blob/main/Read_nc_Files.ipynb) which is where the bulk of the analysis takes place, commented as much a possible amongst the code there. 

My preference is jupyter lab for analysis, packages needed are mainly `pandas` and `xarray`, though some of the geospatial packages are also useful. An example environment is given `requirements.yaml` which can be installed using `conda create --name <env> --file requirementd.yaml` in the [anaconda promt](https://anaconda.org/anaconda/conda)

