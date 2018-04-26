PROJECT TITLE
================
24-7
4-20-18

    ## ── Attaching packages ──────────────────────────────────────────────────── tidyverse 1.2.1 ──

    ## ✔ ggplot2 2.2.1     ✔ purrr   0.2.4
    ## ✔ tibble  1.4.2     ✔ dplyr   0.7.4
    ## ✔ tidyr   0.8.0     ✔ stringr 1.3.0
    ## ✔ readr   1.1.1     ✔ forcats 0.3.0

    ## ── Conflicts ─────────────────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()

    ## 
    ## Attaching package: 'lubridate'

    ## The following object is masked from 'package:base':
    ## 
    ##     date

    ## 
    ## Attaching package: 'maps'

    ## The following object is masked from 'package:purrr':
    ## 
    ##     map

### Background

### Data Manipulation

    ## Warning: Expected 3 pieces. Missing pieces filled with `NA` in 8953 rows
    ## [11173, 11174, 11175, 11176, 11177, 11178, 11179, 11180, 11181, 18268,
    ## 18269, 18270, 18271, 18272, 18273, 18274, 18275, 18276, 18277, 18278, ...].

    ## Warning: Expected 3 pieces. Missing pieces filled with `NA` in 8953 rows
    ## [11173, 11174, 11175, 11176, 11177, 11178, 11179, 11180, 11181, 18268,
    ## 18269, 18270, 18271, 18272, 18273, 18274, 18275, 18276, 18277, 18278, ...].

    ## Warning: Expected 3 pieces. Missing pieces filled with `NA` in 22469
    ## rows [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19,
    ## 20, ...].

    ## Warning: Expected 3 pieces. Missing pieces filled with `NA` in 22469
    ## rows [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19,
    ## 20, ...].

    ## Joining, by = c("year", "case_no", "decision_date", "npc_submitted_date", "case_status", "alien_work_state", "certification_begin_date", "certification_end_date", "employer_city", "employer_state", "employer_postal_code", "agent_attorney_city", "agent_attorney_state", "job_title", "nbr_workers_certified", "prevailing_wage", "pw_unit_of_pay", "basic_rate_of_pay", "basic_unit_of_pay", "dot_occupational_code", "nbur_workers_requested", "dot_name", "soc_code", "soc_name", "wage_diff")
    ## Joining, by = c("year", "case_no", "decision_date", "npc_submitted_date", "case_status", "alien_work_state", "certification_begin_date", "certification_end_date", "employer_city", "employer_state", "employer_postal_code", "agent_attorney_city", "agent_attorney_state", "job_title", "nbr_workers_certified", "prevailing_wage", "pw_unit_of_pay", "basic_rate_of_pay", "basic_unit_of_pay", "dot_occupational_code", "nbur_workers_requested", "dot_name", "soc_code", "soc_name", "wage_diff")

    ## Joining, by = c("year", "case_no", "decision_date", "decision_month", "decision_day", "decision_year", "npc_submitted_date", "case_status", "alien_work_state", "certification_begin_date", "certification_end_date", "employer_city", "employer_state", "employer_postal_code", "agent_attorney_city", "agent_attorney_state", "job_title", "nbr_workers_certified", "prevailing_wage", "pw_unit_of_pay", "basic_rate_of_pay", "basic_unit_of_pay", "dot_occupational_code", "nbur_workers_requested", "dot_name", "soc_code", "soc_name", "wage_diff", "submitted_month", "submitted_day", "submitted_year")

### Visualizations

![](project_files/figure-markdown_github/-%20map-1.png)

![](project_files/figure-markdown_github/line-graph-1.png)

In 2008, Congress failed to renew the Save Our Small and Seasonal Bussinesses Act (SOSSBA). This reduced the cap for the total number of H2B Visas that could be approved every year.

### Hypothesis Tests

### Regression Model

    ## # A tibble: 17,361 x 3
    ##    nbr_workers_certified nbur_workers_requested percent_approved
    ##                    <int>                  <int>            <dbl>
    ##  1                     0                     20            0.   
    ##  2                    15                     15            1.00 
    ##  3                     5                      5            1.00 
    ##  4                     4                      4            1.00 
    ##  5                    24                     24            1.00 
    ##  6                    19                     20            0.950
    ##  7                     3                      3            1.00 
    ##  8                    13                     13            1.00 
    ##  9                    10                     11            0.909
    ## 10                    15                     15            1.00 
    ## # ... with 17,351 more rows
