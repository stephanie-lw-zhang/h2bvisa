Analyzing H2B Data
================
24-7
3-26-18

``` r
library(tidyverse)
```

    ## Warning: running command 'timedatectl' had status 1

    ## ── Attaching packages ───────────────────────────────────────────────────── tidyverse 1.2.1 ──

    ## ✔ ggplot2 2.2.1     ✔ purrr   0.2.4
    ## ✔ tibble  1.4.1     ✔ dplyr   0.7.4
    ## ✔ tidyr   0.7.2     ✔ stringr 1.2.0
    ## ✔ readr   1.1.1     ✔ forcats 0.2.0

    ## ── Conflicts ──────────────────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

``` r
library(broom)
library(infer)
```

Section 1. Introduction
-----------------------

Section 2. Data analysis plan
-----------------------------

Our outcome variable is whether an H-2B Visa certification request made by a company is successful. Our explanatory variables are the state in which the request was made, the type of work the request was made for, by DOT Code, the number of workers requested, the time of the year the request was made, and the salary for workers.

The comparison groups will include different states, which could be combined into regions, different occupations, such as agricultural or service, the seasons in which a request was made, the salary of the workers, and whether the workers are recieving benefits.

We will primarily use hypothesis testing to determine variable independence. In other words, we will use hypothesis tests to determine if there is a statistically significant difference in the proportion of Visa applicants that get accepted. We will also make a linear model to predict whether or not certain cases would or wouldn't be granted a Visa. In doing this, we will used Cross Validation to confirm that our model would be a good predictor in situations outside of our data.

``` r
#h2b <- read_csv("data/H-2B_FY2000csv.html")
```

Section 3. Data
---------------

``` r
#glimpse()
```
