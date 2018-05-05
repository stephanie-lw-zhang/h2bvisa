# project

DIMENSIONS: 
There are 31,422 observations in this data frame with 30 variables

CODEBOOK:

case_no: The OFLC-assigned case number.

decision_date: The date on which the Visa was granted or denied

npc_submitted_date: The date the Visa application was submitted 

case_status: The status of the case; typically a variation on "CERTIFIED", "DENIED", "WITHDRAWN", et cetera.

alien_work_state: The state in which the worker is trying to get a job

certification_begin_date:  The date on which the worker is allowed to begin working

certification_end_date: The date on which the worker's Visa expires

employer_city: The city the employer listed.

employer_state: The state the employer listed.

employer_postal_code: The postal code the employer listed.

agent_attorney_city: The city the agent or attorney listed

agent_attorney_state: The state the agent or attorney listed

job_title: The job title listed by the employer.

nbr_workers_certified: The number of workers/visas certified.

basic_rate_of_pay: The basic rate of pay in dollars

basic_unit_of_pay: The time unit for which the basic rate of pay is allocated 

dot_occupational_code: Job code

nbr_workers_requested: The number of workers/visas requested.

dot_name: Name of job

soc_code: Job category code

soc_name: Job category

prevailing_wage: Wage worker ends up actually receiving

pw_unit_of_pay: The time unit for which the prevailing wage is allocated


Added Variables:

wage_diff: difference between prevailing wage and baisc rate of pay

decision_season: season in which visa status was decided

submitted_season: season in which visa application was submitted

start_season: season in which worker started working

region: area of the United States employer is based in (N,S,E,W)

occupation_category: general category that job falls into



