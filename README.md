# Seattle Weather

In this project, data science will be used to understand whether it rains more in Seattle, WA or St. Louis, MO.

## Data Source

Two data sets, `seattle_rain.csv` and `stl_rain.csv`, will be used to look at the daily precipitation in each city from 2017 to 2022. They are from NOAA's [Climate Data Online Search](https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND) tool.

## Data Preparation

Several steps were taken to prepare the data:
- The date columns were converted to pandas datetime objects.
- St. Louis measurements that were not from the airport station, and measurements from before 2018 were removed.
- The measurements from each city were combined into a single "tidy" data frame.
- The columns were renamed to follow best practices and improve clarity.
- Missing values from Seattle's data set were identified and imputed.
- Additional columns were created from derived data: `month`, `day_of_year`, and `precipitation_rolling` (a rolling average of precipitation measurements for each city)

The prepared data as well as the notebook used for data preparation are available in this repository as `clean_seattle_stl_weather.csv` and `seattle_weather_data_preparation.ipynb`.

## Data Analysis

The data analysis was done in the `seattle_weather_data_analysis.ipynb` notebook, which is available in this repository. Several questions were explored:
-  Which city, by month, has the most overall rain? (sum, daily average, either way)
-  Which city, by month, has the most days with no rain?
-  Which city, by month, has the "rainiest" rainy days?
