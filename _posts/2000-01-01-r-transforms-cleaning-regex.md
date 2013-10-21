---
layout: post
title: Cleaning: regular expressions
group: transforms
language: r
---
We frequently need to strip out unwanted characters from vectors. `gsub` is R's way of doing this.

```r
dirty <- c("VA)", "ID)", "KY)", "MO)", "CO)", "IL)", "IN)", "MS)", "NE)", "OH)")

# get rid of right parentheses, replace them with nothing
gsub("\\)", "", dirty)

```
