# Covid-19 Analysis

## The objective of this project is to analyse the evolution of covid-19 this past months

#### This analysis is possible thanks to the daily reports available here: https://github.com/CSSEGISandData/COVID-19

## Cleaning the Data

#### The first thing I had to do was to clean the datasets, since the daily reports did not have the same column names or column value names. To do this, I used mapping.

```
col_mapping = {
    'Last Update': 'Last_Update',
    'Long_': 'Longitude',
    'Lat': 'Latitude',
    'Country/Region': 'Country_Region'
}

country_mapping = {
    'Mainland China':'China',
    'Russia': 'Russian Federation',
    'South Korea': 'Korea, Republic of',
    'Korea, South': 'Korea, Republic of',
    'Republic of Korea': 'Korea, Republic of',
    'Taiwan': 'Taiwan, Province of China',
    'Taiwan*': 'Taiwan, Province of China',
    'UK': 'United Kingdom',
    'Tanzania': 'Tanzania, United Republic of',
    'The Bahamas': 'Bahamas',
    'Bahamas, The': 'Bahamas',
    'US': 'United States',
    'Venezuela': 'Venezuela, Bolivarian Republic of',
    'Bolivia': 'Bolivia, Plurinational State of',
    'Vietnam': 'Viet Nam',
    'Palestine': 'Palestine, State of',
    'West Bank and Gaza': 'Palestine, State of',
    'Republic of Moldova': 'Moldova, Republic of',
    'Moldova': 'Moldova, Republic of',
    'Macedonia': 'Macedonia, the Former Yugoslav Republic of',
    'North Macedonia': 'Macedonia, the Former Yugoslav Republic of',
    'Macau': 'Macao',
    'Laos': "Lao People's Democratic Republic",
    'Ivory Coast': 'Côte d’Ivoire',
    "Cote d'Ivoire": 'Côte d’Ivoire',
    'Iran': 'Iran, Islamic Republic of',
    'Eswatini': 'Swaziland',
    'Czechia': 'Czech Republic',
    'Congo (Kinshasa)': 'Congo, the Democratic Republic of the',
    'Congo (Brazzaville)': 'Congo',
    'Cabo Verde': 'Cape Verde',
    'Burma': 'Myanmar',
    'Brunei': 'Brunei Darussalam',
    'Holy See': 'Holy See (Vatican City State)',
    'Syria': 'Syrian Arab Republic'
}
```

## Output

#### We have 3 plots, 2 saved as html and one showed in the notebook.The first 2 are timeseries comparing the evolution of the virus among some pre-selected countries.

![Timeseries Plot](https://github.com/ffrancacorrea/covid-19-analysis/blob/master/output/cases_comparison_scatter_plot.png)

#### The 3rd is a map showing the number of confirmed cases per country.

![GeoScatter Plot](https://github.com/ffrancacorrea/covid-19-analysis/blob/master/output/geo_scatter.png)
