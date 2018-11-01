# Bias in Data

Name: Vivek Pagadala
Date: 1 Nov 2018

## Goal
The notebook contained in this repo contains code to analyze the geographical bias in wikipedia articles about politicians.

## Data sources used
The following 3 data sources are used:

- Article data: https://figshare.com/articles/Untitled_Item/5513449 <br/>
  Contains page, country, and rev_id
- Population data: https://www.dropbox.com/s/5u7sy1xt7g0oi2c/WPDS_2018_data.csv?dl=0 <br/>
  Contains Greography, and Population
- Wikimedia ORES API: https://www.mediawiki.org/wiki/ORES
  Provides a prediction for the article's quality class

## Resources used
- Python: 3.6.2
- requests: 2.18.4
- json: 2.6.0
- pandas: 0.22.0
- matplotlib: 2.0.2

## Files Created
The data from the three sources listed about is joined into a
single dataframe, and is stored in the data-processed folder.

The final dataframe contains following columns: 
```page	country	rev_id	population	predictions```

## Visualizations Created


## License
This assignment is released under the MIT license.

The data located on figshare is licensed under CC.
The license for population data on dropbox is unknown.
The ORES API also licensed under CC.
