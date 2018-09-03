# Flamingo Project

Data analysis project to gather, clean and analyze data for the U.S. housing market using Zillow Research and Consumer Price Index (CPI) to compare housing costs and cost of living across multiple U.S. cities.

The Jupyter Notebook retrieves and filters data on various criteria (state, city, zipcodes, neighborhood); it outputs a single clean dataset per city that can be used to perform visualizations using Matplotlib or to export them to CSV files to be used in other application, like Tableau.

## Objectives
The following objectives were set for this project with the goal to quickly identify and compare prices and several housing indicators across different cities:

1. Buy costs of single family units: 1 bedroom, 2 bedroom
2. Affordability rate
3. Price/rent ratio
4. Rent vs buy breakeven horizon
5. Rent & buy forecast
6. Price evolution (time series)
7. Miscellaneous indicators and metrics (buyer/seller index, market health index, days on market, increasing/decreasing values)
8. Consumer Price Index (CPI)

## Quick Start
```
git clone https://github.com/ricardo-hdz/flamingo_project.git
cd flamingo_project
jupyter notebook
```

The only lines you will need to modify to perform your own analysis are the following:

*Cities Filter*
```
# Cities to filter data for
# Change this list to gather data for the cities you want to compare.
# E.g. cities_filter = ['miami,fl','seattle,wa','orlando,fl']
cities_filter = ['orlando,fl']
```

*Geographies Filter*
```
# Geographies (levels) to use to gather and analyze data
# Eg. State, City, Zipcode, Neighborhood
geographies_filter = ['Zip','Neighborhood']
```

*Zip Codes Filter*
```
# Zip codes to filter the data
# Use this filter to limit results to a list of zip ypu want to analyze
zip_filter = ['32835','32811','32805','32839','32809','32819']
```

## Data Output
After running the Jupyter Notebook cells, the local path will have multiple directories with the new data tat was downloaded/processed:

- `datasets` the original datasets downloaded from Zillow
- `indicators` the original indicator datasets downloaded from Zillow
- `{city}` one folder for each city in the cities filter (holding the datasets for each place)
    - inside each `{city}` folder a file `{city}/{geography}_prices_clean.csv` (e.g. `orlando/Zip_prices_clean.csv`) will be placed; this contains the clean dataset you can use to perform a visual analysis of the data