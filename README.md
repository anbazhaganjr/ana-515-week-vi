# U.S. Storm Event Analysis - 1985

## Overview

This project analyzes storm events in the United States for the year 1985 using data from NOAA's Storm Events Database. The dataset includes major weather-related storm events, including start and end dates, locations, associated deaths, injuries, property damage, and other characteristics. The analysis aims to understand the distribution and characteristics of these events across different states, regions, and seasons.

## Access the analysis
You can view the full analysis [here](https://anbazhaganjr.github.io/ana-515-week-vi/storm-event-analysis.html)

## Data Source

The data used in this analysis is sourced from the [NOAA Storm Events Database](https://www1.ncdc.noaa.gov/pub/data/swdi/stormevents/csvfiles/).

## Project Structure

- **storm-event-analysis.Rmd**: The main R Markdown file containing the analysis code and visualizations.
- **merged_data.csv**: The processed and merged data file is saved for further inspection and use.

## Analysis Steps

1. **Data Download and Preparation**:

   - The storm events data for the year 1985 is downloaded and saved locally.
   - The data is limited to specific columns of interest and filtered to include only events listed by county FIPS codes.

2. **Data Cleaning and Transformation**:

   - State and county names are converted to title cases.
   - State and county FIPS codes are padded with "0" to ensure consistency.
   - A unified FIPS column is created by merging state and county FIPS codes.
   - Column names are converted to lowercase for consistency.

3. **Data Integration**:

   - Additional state information (area and region) is merged with the storm events data.
   - The number of events per state is calculated and merged with the state information.

4. **Visualizations**:
   - **Bar Plot**: Shows the total number of storm events in 1985 by region.
   - **Box Plot**: Displays the distribution of storm events by region.
   - **Histogram**: Illustrates the distribution of the number of events.
   - **Scatter Plot**: Visualizes the number of events by state area.
   - **Heatmap**: Shows the number of storm events by state and month.
   - **Seasonal Analysis**: Analyzes the number of storm events by season.
   - **Line Plot**: Depicts the number of storm events over time by month.

## Key Analysis

- **Highest Storm Activity**: The Midwest and South regions had the highest storm events.
- **Seasonal Peaks**: Summer experienced the most storm events, with a notable peak in June.
- **State Variability**: States in the South showed significant variability in storm event counts.
- **Outliers**: Some states exhibited significantly higher numbers of storm events, indicating potential areas for further investigation.

## How to Use

1. **Requirements**:

   - R (version 4.0 or higher)
   - R Packages: `httr`, `rvest`, `dplyr`, `stringr`, `tidyr`, `ggplot2`, `DT`, `knitr`, `kableExtra`

2. **Running the Analysis**:
   - Open the `storm-event-analysis.Rmd` file in RStudio or any other R Markdown editor.
   - Knit the document to generate the HTML report, which includes the analysis and visualizations.

## Citations

- NOAA National Centers for Environmental Information, Storm Events Database. Available at: [NOAA Storm Events Database](https://www1.ncdc.noaa.gov/pub/data/swdi/stormevents/csvfiles/)

## License

This project is licensed under the MIT License. See the LICENSE file for details.
