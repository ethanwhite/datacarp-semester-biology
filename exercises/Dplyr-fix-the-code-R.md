---
layout: exercise
topic: dplyr
title: Fix the Code
language: R
---

This is a follow-up to
[Shrub Volume Aggregation]({{ site.baseurl }}/exercises/Dplyr-shrub-volume-aggregation-R).
If you don't already have the [shrub volume data]({{ site.baseurl }}/data/shrub-volume-data.csv) in your working directory download it.

The following code is supposed to import the shrub volume data and calculate the
average shrub volume for each site and, separately, for each experiment.

```r
read_csv("shrub-volume-data.csv")
shrub_data |>
  mutate(volume = length * width * height) |>
  group_by(site) |>
  summarize(mean_volume = max(volume))
shrub_data |>
  mutate(volume = length * width * height)
  group_by(experiment) |>
  summarize(mean_volume = mean(volume))
```

1. Fix the errors in the code so that it does what it's supposed to
2. Add a comment to the top of the code explaining what it does
