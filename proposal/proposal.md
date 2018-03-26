Analyzing H2B Data
================
24-7
3-26-18

``` r
install.packages("tidyverse")
```

    ## Installing package into '/home/rstudio-user/R/x86_64-pc-linux-gnu-library/3.4'
    ## (as 'lib' is unspecified)

``` r
library(tidyverse)
```

    ## ── Attaching packages ───────────────────────────────────── tidyverse 1.2.1 ──

    ## ✔ ggplot2 2.2.1     ✔ purrr   0.2.4
    ## ✔ tibble  1.4.2     ✔ dplyr   0.7.4
    ## ✔ tidyr   0.8.0     ✔ stringr 1.3.0
    ## ✔ readr   1.1.1     ✔ forcats 0.3.0

    ## ── Conflicts ──────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

``` r
library(readxl)
```

Section 1. Introduction
-----------------------

Our general research question is: what factors make companies more likely to get successfully obtain H2-B visas?

For context, an H2-B visa is a temporary work visa for foreign workers with a job offer for seasonal, non-agricultural work in the United States. Employers from the United States must first submit temporary labor certification applications to the Department of Labor to allow H-2B workers to apply for visas. (Source: U.S. Citizenship and Immigration Services)

The dataset we are using is from the Department of Labor's Office of Foreign Labor Certification (OFLC). The data comes from H-2B applications that have been received and entered into the Department of Labor Tracking system. Specific information in the dataset about the employers was gathered through the foreign labor certification applications employers submitted. Data relating to wage levels was provided by the Bureau of Labor Statistics' Occupational Employment Statistics Program.

The data is sorted by fiscal year, from 2000 to 2013. Each observation is a different petition filed by an employer. The variables in the dataset are as follows: CASE\_NUMBER, DECISION\_DATE, NPC\_SUBMITTED\_DATE, CASE\_STATUS, VISA\_CLASS, ALIEN\_WORK\_STATE, CERTIFICATION\_BEGIN\_DATE, CERTIFICATION\_END\_DATE, EMPLOYER\_NAME, EMPLOYER\_ADDRESS1, EMPLOYER\_ADDRESS2, EMPLOYER\_CITY, EMPLOYER\_STATE, EMPLOYER\_POSTAL\_CODE, AGENT\_ATTORNEY\_NAME, AGENT\_ATTORNEY\_CITY, AGENT\_ATTORNEY\_STATE, SOC\_CODE, SOC\_NAME, JOB\_TITLE, NBR\_WORKERS\_CERTIFIED, PREVIALING\_WAGE (spelling error present in data), PW\_UNIT\_OF\_PAY, BASIC\_RATE\_OF\_PAY, BASIC\_UNIT\_OF\_PAY \#\# Section 2. Data analysis plan

Our outcome variable is whether an H-2B Visa certification request made by a company is successful. Our explanatory variables are the state in which the request was made, the type of work the request was made for, by DOT Code, the number of workers requested, the time of the year the request was made, and the salary for workers.

The comparison groups will include different states, which could be combined into regions, different occupations, such as agricultural or service, the seasons in which a request was made, the salary of the workers, and whether the workers are recieving benefits.

We will primarily use hypothesis testing to determine variable independence. In other words, we will use hypothesis tests to determine if there is a statistically significant difference in the proportion of Visa applicants that get accepted. We will also make a linear model to predict whether or not certain cases would or wouldn't be granted a Visa. In doing this, we will used Cross Validation to confirm that our model would be a good predictor in situations outside of our data.

``` r
#h2b <- read_excel("data/H-2B_FY2008.xlsx") %>%
#  full_join(read_excel("data/H-2B_FY2009.xlsx"))
```

Section 3. Data
---------------
