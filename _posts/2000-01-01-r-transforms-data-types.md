---
layout: post
title: Formatting Data types
group: transforms
language: r
---

Sometimes, when we load a data frame into the R console, it's not in the right format. Dumb R might make it a factor, or the numbers might be strings, or whatever.

To turn a character vector into a number vector:

```r

bad <- c("1", "3", "23", "9238")
good <- as.numeric(bad)

# note: if it's not a number, R turns it into NA.
bad <- c("1", "3", "giraffe", "9238")
good <- as.numeric(bad)
# returns  1    3   NA 9238

```

To turn a character vector of dates into a date class R likes isn't hard, but you do need to specify the format your date is in. Mostly this just takes practice. See `?format.Date` in the R console for more details.

```r

bad <- c("4-16-81", "9-19-45", "1-3-93")
good <- as.Date(bad, format="%m-%d-%y")

bad <- c("04/16/1981", "09/19/1945", "01/03/1993")
good <- as.Date(bad, format="%m/%d/%Y")



```