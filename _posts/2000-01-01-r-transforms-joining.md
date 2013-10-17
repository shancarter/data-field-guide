---
layout: post
title: Joining Two Datasets
language: r
---
```r

# field names must match for R to know what to join on
# note: this will DROP RECORDS that don't join; returns only successful joins
merged <- merge(dataframe1, dataframe2, by="field_name")

# to keep all the records in dataframe1 even if they dont join perfectly to dataframe2
merged <- merge(dataframe1, dataframe2, by="field_name", all.x = TRUE)

# to keep all the records in dataframe2 even if they dont join perfectly to dataframe1
merged <- merge(dataframe1, dataframe2, by="field_name", all.y = TRUE)
```

