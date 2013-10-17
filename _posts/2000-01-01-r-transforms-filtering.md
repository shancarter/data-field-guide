---
layout: post
title: Filtering
language: r
---
Return a new dataset that has only the elements that match given criteria.

```r
filtered_data <- subset(data, year > 2000)

# can take many arguments
filtered_data <- subset(data, year <= 2000 & player_name == "Shavin")

# filter matching many conditions
upper_midest = subset(data, state_abb%in%c("Minnesota", "Wisconsin", "North Dakota", "South Dakota"))
```
