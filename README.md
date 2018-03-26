# project
dimensions: 

codebook:
case_no: The OFLC-assigned case number.
visa_type: "H-2A" or "H-2B".
fy: The fiscal year of the most recent OFLC decision/progress on the case.
last_event_date: The date of the most recent OFLC decision/progress on the case.
case_status: The status of the case; typically a variation on "CERTIFIED", "DENIED", "WITHDRAWN", et cetera.
n_requested: The number of workers/visas certified.
n_certified: The number of workers/visas certified.
is_certified: True/False; a standardization of the case_status field.
certification_begin_date / certification_begin_date: "Actual date granted to an employer indicating when the need for the foreign workers to perform agricultural services or labor is expected to [begin / end]." Unavailable for H-2B data prior to FY2007.
job_title: The job title listed by the employer.
employer_name: The name of the employer applying for certification; converted to all-caps.
employer_state: The state the employer listed.
employer_city: The city the employer listed.
employer_address_1: The first line of the address the employer listed.
employer_address_2: The second line of the address the employer listed.
employer_postal_code: The postal code the employer listed.
agent_name: The name of the agent or attorney filing the application for the employer. Some years of data include multiple columns related to visa agents; the standardized field combines these fields, separating them by a :.
organization_flag: Various types of organizations — including sole employers and joint employers — can apply for visa certifications. This field tracks OFLC's categorizations. Only available for H-2A decisions.
is_duplicate: True/False/null: This derived value will be True — indicating that this row corresponds a sub-application of a joint employer's "master application" — if (a) visa_type is "H-2A", (b) the organization_flag is blank, and (c) comes from fiscal year 2008 or later. H-2A data from FY 2006 and FY 2007 do not contain a organization_flag field. For these records, and H-2B records, is_duplicate will be null.
