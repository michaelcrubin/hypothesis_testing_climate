
# Hypothesis Testing Documentation

## Introduction
This document provides an analysis of meteorological data sets containing rainfall measurements from five different points. The goal is to determine if there are statistically significant differences in the rain patterns between these points. The stations are located close to each other, with a few kilometers of distance between them.

## Documentation Access

### This Project:
[Hypothesis Testing Climate](https://michaelcrubin.github.io/documentations/hypothesis_testing_climate.html){:target="_blank"}

### Other Projects:
[Greedy Optimization](https://michaelcrubin.github.io/documentations/greedy_optimization.html)
[Interpolation Study](https://michaelcrubin.github.io/documentations/interpolation_study.html)
[Agronomic Spraying Climate](https://michaelcrubin.github.io/documentations/spray_climate.html)



## Libraries Used
The following libraries are imported in the code:
- ggplot2
- tidyverse
- data.table
- geosphere
- Metrics
- rmutil
- pathmapping
- lubridate
- knitr
- here

## Data Import
The code imports two CSV files containing rain data from different points. The files are read using the `read.table` function and stored in two data frames, `df1` and `df2`. The file paths are constructed using the `here` function from the `here` library.

## Data Preprocessing
The code performs various data preprocessing steps to prepare the data for analysis:

1. Transposing the `df1` data frame to convert rows to columns and add correct column headers.
2. Extracting the coordinates of the point of interest (`Point_0`) from the transposed data frame.
3. Removing unnecessary rows and columns from `df1` and `df2`.
4. Dropping rows with missing values (NA) from `df1` and `df2`.
5. Calculating the Euclidean and geographical distances from each point to `Point_0` using the coordinates.
6. Creating indexes for convenient slicing and managing the data.

## Map Plot
The code generates a map plot using the `ggplot2` library to visualize the station settings. The plot shows all stations as blue points and the point of interest (`Point_0`) as a red point. The title of the plot displays the total area covered by the stations in hectares and the distances in meters.

## Descriptive Statistics
Descriptive statistics are calculated for the rainfall data, including the sum, mean, and variance. The statistics are displayed in a table format.

## Hypothesis Testing
The code performs hypothesis testing to evaluate the differences between the rainfall measurements at different stations. The hypothesis being tested is that there are different microclimates within the area.

### Two-Sample T-Test
The code starts with a two-sample t-test between Station.3_01204052 and Station.2_0120593F, comparing the largest and smallest values. The test statistic, degrees of freedom, critical value, p-value, and decision are calculated. A confidence interval is also estimated.

## Results
The results of the hypothesis testing, including the test statistic, critical level, probability, p-value, decision, and confidence interval, are displayed in a table format.

