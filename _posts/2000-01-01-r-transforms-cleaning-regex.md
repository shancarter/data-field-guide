---
layout: post
title: Cleaning: strsplit
group: transforms
language: r
---
R's strsplit lets you break up strings into little chunks (called lists), which you can then pull out with another method called `sapply`.
This is not the most efficient way to do this, but it's presented here in multiple steps for clarity.

```r

dirty <- c("ACCOMACK(VA)", "ADA(ID)", "ADAIR(KY)", "ADAIR(MO)", "ADAMS(CO)", "ADAMS(IL)", "ADAMS(IN)", "ADAMS(MS)", "ADAMS(NE)", "ADAMS(OH)", "ADAMS(PA)", "ADAMS(WI)", "AIKEN(SC)")

# try this in the console. it returns a list (of lists!)
strsplit(dirty, split = "\\(")

# make a function to fetch out the second element of a list
get_second_element <- function(item) {
  return (item[2])
}

# use sapply to apply this function to each element. the strange dashes here in front of the parens are because it's a special character.

dirty_list <- strsplit(dirty, split = "\\(")

sapply(dirty_list, get_second_element)

```
