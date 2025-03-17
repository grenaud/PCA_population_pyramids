# Population Pyramid PCA and Animation

## Overview

This project analyzes population pyramid data from 1950 to 2024 for multiple countries and visualizes demographic transitions using Principal Component Analysis (PCA). The script filters for countries with more than 1 million people in 1950, vectorizes the population pyramid data (separately for males and females) into frequency vectors, and then uses PCA to reduce the high-dimensional data into two main components. Each country's PCA position is marked with its national flag, and a smooth animation is created to illustrate the evolution of demographic structures over time.

## Background

Population pyramids graphically represent the distribution of a population by age and sex. They are a crucial tool in demography, providing insights into the socio-economic and health challenges of a country. In recent decades, many countries have experienced falling fertility rates, which have led to significant shifts in the shape of these pyramids. For example:

- **Youth cohorts shrink:** Fewer births result in a narrower base.
- **Aging populations:** Longer life expectancies cause the median age to increase.
- **Economic and Social Implications:** Changes in the age structure impact labor markets, healthcare systems, and social security programs.

By visualizing these changes via PCA, we can better understand how falling fertility rates and other demographic shifts alter the overall population structure.

## Why PCA?

PCA is a powerful statistical method that reduces the dimensionality of complex data while preserving as much variance as possible. In this project, PCA transforms the high-dimensional frequency vectors (derived from age and sex distributions) into two principal components. These components capture the major trends in demographic changes, allowing us to visualize and compare the evolution of population structures across countries and over time.

## Dependencies

The script relies on the following Python libraries:

- **pandas**
- **numpy**
- **scikit-learn**
- **matplotlib**
- **pycountry**
- **requests**
- **Pillow**
- **moviepy**

You can install the dependencies using pip:

```bash
pip install pandas numpy scikit-learn matplotlib pycountry requests Pillow moviepy
```


## Data Format
- Population Pyramid Files:
Each CSV file should be named in the format:
pyrpop_{country_code}_{year}.csv
and contain the following columns:

```
Age,M,F
0-4,28433,27232
5-9,22549,21605
...
```


A file named code2country should provide a mapping between country codes and country names. Each line should follow this format:

```
"242"   "fiji"
"246"   "finland"
...
```


## How to Run
Prepare Your Data:
Ensure that all population pyramid CSV files and the code2country mapping file are in the same directory as the script.

Run the Script:
Execute the script:

```
python PCA.py
```



## Project Motivation
The falling fertility rate is one of the most critical demographic trends observed in recent decades. This project was created to visually capture how such demographic shifts are reflected in population pyramids. By leveraging PCA, we can summarize complex demographic data into a two-dimensional space, allowing for clear visualization of trends such as:

- The narrowing base of population pyramids.
- The aging of populations.
- The overall impact of changing fertility and mortality rates on national demographics.
- These insights can be invaluable for policymakers, researchers, and anyone interested in understanding the socio-economic implications of demographic transitions.

## License
This project is licensed under the MIT License.

## Acknowledgements
This project builds on publicly available demographic data from https://www.populationpyramid.net/. The code/README was mostly written by ChatGPT. It uses various Python libraries to analyze and visualize the data. Special thanks to the developers of the libraries and tools that made this project possible.

