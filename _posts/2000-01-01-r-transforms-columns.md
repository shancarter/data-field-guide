---
layout: post
title: Manipulating Columns
group: transforms
language: r
---
```r
#Delete a column
data$name <- NULL

#Rename one column, in this case the second column
colnames(data)[2] <- "newname"

#Rename all the columns at once
colnames(data) <- c("newname1", "newname2", "newname2")

```

