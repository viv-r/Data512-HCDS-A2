# Bias in Data

Name: Vivek Pagadala <br>
Date: 1 Nov 2018

## Goal
The notebook contained in this repo contains code to analyze the geographical bias in wikipedia articles about politicians.

## Data sources
The following 3 data sources are used:

- Article data: https://figshare.com/articles/Untitled_Item/5513449 <br/>
  Contains page, country, and rev_id
- Population data: https://www.dropbox.com/s/5u7sy1xt7g0oi2c/WPDS_2018_data.csv?dl=0 <br/>
  Contains Greography, and Population
- Wikimedia ORES API: https://www.mediawiki.org/wiki/ORES <br>
  Provides a prediction for the article's quality class

## Library versions
- Python: 3.6.2
- requests: 2.18.4
- json: 2.6.0
- pandas: 0.22.0
- matplotlib: 2.0.2

## Output
The data from the three sources listed about is joined into a <br>
single dataframe, and is stored in the data-processed folder.

The final dataframe contains following columns: <br>
```page	country	rev_id	population	predictions```

## Tables
### 10 highest-ranked countries: Ratio of politician articles to country population
![](https://github.com/viv-r/Data512-HCDS-A2/img/least-article-pop.png)
### 10 lowest-ranked countries: ratio of article quality to article count
![](https://github.com/viv-r/Data512-HCDS-A2/img/top-article-pop.png)
### 10 lowest-ranked countries: ratio of article quality to article count
![](https://github.com/viv-r/Data512-HCDS-A2/img/least-quality-article.png)
### 10 highest-ranked countries: ratio of article quality to article count
![](https://github.com/viv-r/Data512-HCDS-A2/img/top-quality-article.png)


## Reflections

### What biases did you expect to find in the data, and why?
I expected to see higer quality articles in english speaking regions given that <br>
most Wikipedia are in English. I also expected to see the quality of article being <br>
proportional to the economic development of a country, given that access to internet <br>
could be a barrier in some regions.


### What are the results?
The list of countries with least number of articles per capita isn't very surprising <br>
given the large population of China and India. Also, the list of countries with most <br>
articles per captia a highly skewed towards very small countries.

The tables relating to the quality of articles is more surprising, however. There are a lot <br>
of countries which do not have any article classified as 'good'. The countries with a high <br>
proportion of good quality articles are also not the ones I'd expected to see. (USA, countries <br>
in europe)

### What theories do you have about why the results are what they are?
The 'ratio of articles to population' tables are highly skewed, most likely due the effect of <br>
population on the ratio.
In the second set of tables where we compare the quality to the count of articles, it looks like <br>
the regions with low total article counts domniate the top-10 list (few articles, but well <br>
written, resulting in a high ratio)

## License
This assignment is released under the MIT license.

The data located on figshare is licensed under CC. <br>
The license for population data on dropbox is unknown. <br>
The ORES API also licensed under CC.
