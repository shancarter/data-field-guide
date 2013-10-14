---
layout: default
title: Aggregation
language: r
---
```r
#to get, say, the total strikeouts per year (from our homework)
agg <- aggregate(data$strikeouts, list(data$year), sum)

#to get, say, the total strikeouts per team per year (from our homework)
agg <- aggregate(data$strikeouts, list(data$year, data$team), sum)

# the third argument takes any function (including a custom one)
# fewest strikeouts per team per game
agg <- aggregate(data$strikeouts, list(data$year, data$team), min)

```
