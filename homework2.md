Homework \#1 – Pet Names Dataset
================
Nawaf almutairi
2022-05-27

2210002968

**Deadline:** 23:59 on Monday, 21 March 2022

## Loading Packages

``` r
library(tidyverse)
library(openintro)
library(ggrepel)
```

\##Exercises

1.  How many pets are included in this dataset? (Simply count the number
    of rows)

``` r
nrow(seattlepets)
```

    ## [1] 52519

Write your answer here: 52519

*Knit the document, commit your changes with a commit message that says
“Completed Exercise 1”, and push. Make sure to commit and push all
changed files so that your Git pane is cleared up afterwards.*

2.  How many variables do we have for each pet? (Simply count the number
    of columns)

``` r
ncol(seattlepets)
```

    ## [1] 7

Write your answer here: 7

*Knit the document, commit your changes with a commit message that says
“Completed Exercise 2”, and push. Make sure to commit and push all
changed files so that your Git pane is cleared up afterwards.*

3.  What are the three most common pet names in Seattle? To do this you
    will need to count the frequencies of each pet name and display the
    results in descending order of frequency so that you can easily see
    the top three most popular names.

``` r
seattlepets %>%
  count(animal_name)%>%
  arrange(desc(n))
```

    ## # A tibble: 13,930 × 2
    ##    animal_name     n
    ##    <chr>       <int>
    ##  1 <NA>          483
    ##  2 Lucy          439
    ##  3 Charlie       387
    ##  4 Luna          355
    ##  5 Bella         331
    ##  6 Max           270
    ##  7 Daisy         261
    ##  8 Molly         240
    ##  9 Jack          232
    ## 10 Lily          232
    ## # … with 13,920 more rows

Write your answer here:The most popular pet names in Seattle are Lucy
With 439, Charlie With 389, and Luna With 355.

*Knit the document, commit your changes with a commit message that says
“Completed Exercise 3”, and push. Make sure to commit and push all
changed files so that your Git pane is cleared up afterwards.*
