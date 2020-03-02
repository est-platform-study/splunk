## trendline Command
- trendline computes the moving averages of a field
```
trendline <trendtype><period>(field) [AS newfield]
```
- Must define the period over which to compute the trend
- period must be an integer between 2 and 10000 
### trendtype
- sma
    - simple moving average
- ema
    - exponential moving average
- wma 
    - weighted moving average
## iplocation Command
- Use iplocation to look up and add location information to an event
    - This information includes city, country, region, latitude an longtitude
## geostats Command
- Use geostats to compute statistical functions and render a cluster map
```
geostats [latfield=string][longfield=string][stats-agg-term][by-clause]
```
- Data must include latitude and longitude values
