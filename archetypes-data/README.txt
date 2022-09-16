
/shp: 
	Africa national shapefile, from "/Volumes/GoogleDrive/My Drive/itn_cube/input_data/general/shapefiles/Africa.shp"


Directories with input data:
/unscaled: 
	Covariates without rescaling to fit between zero and one, *and* without subsetting to only those pixels with malaria transmission. From "v2_era5_climate".
/rescaled: 
	Covariates with rescaling to fit between zero and one, *but* without subsetting to only those pixels with malaria transmission. From "v3_era5_climate_rescaled".
/rescaled_and_bounded: 
	Covariates with rescaling to fit between zero and one, *and* subsetting to only those pixels with malaria transmission. From "v4_era5_bounded_transmission".

Within each of these are three files:
- mask.tif: raster that acts as a template, ands subsets the covariates to the appropriate pixels.
- svd_rotations.csv: SVD outputs to use in clustering
- covariate_ids.RData: original covariate values by pixel. Generated specifically for this project from the original svd_output.rdata files.