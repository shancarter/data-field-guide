---
layout: post
title: Sorting
group: transforms
language: r
---
```r
#sort data frame on a field name – note ascending order by default.
data <- data[order(data$fieldname),]

#descending sort
data <- data[order(data$fieldname, decreasing=TRUE),]

```

