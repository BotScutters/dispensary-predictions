# Project Luther Proposal:

## Predicting Revenues for a Recreational Marijuana Dispensary

_Scott Butters_

### Overview

In 2012, Washington state legalized the recreational use of marijuana, and since 2014 approximately 500 state licensed dispensaries have opened throughout the state, with nearly 150 of those here in Seattle. The industry is heavily tracked and regulated and a wealth of sales and business statistics are publicly available.

### Question

As my MVP, I'd like to train a linear regression model to predict the monthly revenue of Washington state recreational cannabis dispensaries using the inventory and demographic data as follows.

### Data Sources

My data set will be derived from a number of sources, including leafly.com, 502data.com, and census data. From leafly I plan to scrape data specific to dispensaries such as inventory, user ratings and reviews, medical/recreational classification, and location coordinates. I also intend to gather demographic data at the zip code level for each dispensary. For my target data I've downloaded monthly sales data from the Washington State Liquor and Cannabis Board (WCLSB) for each registered dispensary extending from 11/2017-1/2019. 

### Features

In order to predict a dispensary's monthly sales data, I indend to use at least some of the following features, and potentially more:

| Feature            | Description                                                  | Type       |
| ------------------ | ------------------------------------------------------------ | ---------- |
| Flowers            | Number of unique products offered categorized by Leafly as "Flower" | Continuous |
| Concentrates       | Number of unique products offered categorized by Leafly as "Concentrates" | Continuous |
| Edibles            | Number of unique products offered categorized by Leafly as "Edibles" | Continuous |
| Pre-Rolls          | Number of unique products offered categorized by Leafly as "Pre-Rolls" | Continuous |
| Other              | Number of unique products offered categorized by Leafly as "Other" | Continuous |
| Rating             | Rating on Leafly on a scale from 0-5 with one decimal of precision | Continuous |
| Reviews            | Number of reviews on Leafly                                  | Continuous |
| Population Density | Population density by zip code                               | Continuous |
| Income             | Average income by zip code                                   | Continuous |

Depending on available resources, I may also collect/engineer more features such as additional demographic information for a location (race, age, education and gender distributions), distance to nearest competing dispensary, number of dispensaries in the same zip code, crime stats, walkscore, etc.

### Stretch Goals

After establishing my MVP I intend to work on improving my project by a number of methods:

#### Additional Data

As mentioned previously, with only 500 cannabis dispensaries in the state it's difficult to develop a very large dataset. Time allowing, I'd like to augment my dataset with additional observations of the same dispensaries at various points in the past by using snapshots from the Internet Archive to scrape historical datapoints from Leafly and compare those against their nearest month's revenue.

#### Feature Engineering

In addition to the basic features used in my MVP, there are many other features I could potentially use to train my models on. I may also collect/engineer more features such as additional demographic information for a location (race, age, education and gender distributions), distance to nearest competing dispensary, number of dispensaries within a given distance (i.e. 1 mile), area crime stats, walkscore, etc.

#### Additional Models

To extend my project, I also plan to test other predictive methods on my data such as K nearest neighbors, decision trees, random forest regression, and potentially others. I'd also like to select and tune my models using a grid search and validate them using KFolds cross validation so-as to minimize my loss of accuracy due to a small observation count.

#### Further Insights

By analyzing the results of my most effective model(s), I should be able to glean additional insights about what factors contribute to the highest revenues and then make suggestions to dispensaries about what might be desirable qualities in location or inventory.

### Known Challenges

The passing of Washington Initiative 502 wrote into law that state dispensaries would collect and report vast amounts of data about business and operations, which was both ambitious and admirable. That said, the rollout has not been entirely smooth. In the years since recreational cannabis has been legalized the state has shifted between multiple providers for its data collection and aggregation services and there have been numerous reports of inaccuracies and inconsistencies in the data between retailers and centrailized database. Additionally, the industry is still young and therefore experiencing rapid growth and change. These factors are likely to introduce some error and unpredictability into the data I'll be working with. Coupled with the relatively small number of observations I'll likely be working with, I expect that this may present a challenge for developing very accurate prediction models and that these issues are something I will spend a lot of time attempting to mitigate.