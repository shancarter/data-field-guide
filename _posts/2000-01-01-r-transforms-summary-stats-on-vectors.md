---
layout: post
title: Summary stats on a vector
group: transforms
language: r
---

You should know your data – every column, every row.

To get the min, max or mean of a quantitative vector

```r

df <- data.frame(val1=c(-34, 45, 34, 69, 7, 99), val2=c(-14, 435, 134, 6, -7, 9))

#min of thr first col
min(df$val1)
mean(df$val1)
max(df$val1)


#or do summary on the whole data frame
summary(df)

```

If your data is qualitative, you can use `table`

```r

animals <- c("monkeys", "monkeys", "giraffe", "donkey", "blue whale", "giraffe", "giraffe")

table(animals)

# blue whale     donkey    giraffe    monkeys
#         1          1          3          2

```