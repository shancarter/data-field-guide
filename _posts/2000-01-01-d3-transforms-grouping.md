---
layout: post
title: Grouping
language: d3
---
How you aggregate really depends on what you want. [Mister Nester](http://bl.ocks.org/shancarter/raw/4748131/) is useful for tinkering.

```javascript

d3.nest()
  .key(function(d) { return d.year; })
  .rollup(function(values) {
    return {
      totalStrikeouts: d3.sum(values, function(d) { return d.strikeouts })
    };
  })
  .entries(data);
```
