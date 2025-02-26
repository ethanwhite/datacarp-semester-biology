---
layout: exercise
topic: Combining Basics
title: Shrub Volume Carbon
language: R
---

This is a follow-up to [Shrub Volume Data Basics]({{ site.baseurl }}/exercises/Dplyr-shrub-volume-data-basics-R).

Now that you're familiar with the data, Dr. Morales wants you to conduct a preliminary analysis of these data to include in a grant proposal (*she might be a world renowned expert in carbon storage in plants, but she sure doesn't know much about computers*). If you missed it, the [data file]({{ site.baseurl }}/data/shrub-volume-data.csv) is still on the web.

You might be able to do this analysis by hand in Excel, but Dr. Morales seems to
always get funded meaning that you'll be doing this again soon with a much
larger dataset. So, you decide to write a script so that it will be easy to do
the analysis again.

Write an R script that:

- Imports the data using `read_csv()`.
- Uses a `for` loop to check each row in the dataset and groups by height: 
  `"tall"` `if (height > 5)`, `"medium"` `if (2 <= height < 5)`, 
  or `"short"` `if (height < 2)`, and builds a list of the results.
- Uses `dplyr` to determine the total amount of carbon in the shrub and 
`transmute()` rows in the dataset to produce the results table. The total
amount of carbon is equal to `1.8 + 2 * log(volume)` where `volume` is the 
volume (`length * width * height`) of the shrub.  
- Stores this information as table in a `data.frame` with each of these row
holding the results for one shrub. The first column should have the
experiment number. The second column should have the string `"tall"`, 
`"medium"` or `"short"` depending on the height of the shrub. And, the third 
column should have the shrub carbon. Be sure to use descriptive column names.
- Exports this table to a `csv` (*comma delimited text*) file titled
`shrubs_experiment_results.csv`.
- Uses functions to break the code up into manageable pieces.

*Optional: If you'd like to test your skills a little more, try determining 
the average carbon in a shrub for each of the different experiments and 
printing those values to the screen.*
