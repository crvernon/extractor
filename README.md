# extractor
Code for extracting a subset of building data using target features in another shapefile.

## Usage
```python

# input files
buildings_shp_file = '<path to file with filename and extension>'
target_shp_file = '<path to file with filename and extension>'
existing_shp_file = '<path to file with filename and extension>'
output_directory = '<path to directory>'

# offset in map units
x_offset = 1000
y_offset = 1000

# choose to write outputs
write_outputs = True

# which method to use for extracting the buildings data
subset_method = 'sjoin'

# run it and return a geopandas dataframe
result_gdf = workflow(buildings_shp_file=buildings_shp_file,
                        target_shp_file=target_shp_file,
                        existing_shp_file=existing_shp_file,
                        output_directory=output_directory,
                        x_offset=x_offset,
                        y_offset=y_offset,
                        write_outputs=write_outputs,
                        subset_method=subset_method)
```
