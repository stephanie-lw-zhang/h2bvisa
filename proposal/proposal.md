Analyzing H2B Data
================
24-7
3-26-18

Section 1. Introduction
-----------------------

Our general research question is: what factors make companies more likely to get successfully obtain H2-B visas?

For context, an H2-B visa is a temporary work visa for foreign workers with a job offer for seasonal, non-agricultural work in the United States. Employers from the United States must first submit temporary labor certification applications to the Department of Labor to allow H-2B workers to apply for visas. (Source: U.S. Citizenship and Immigration Services)

The dataset we are using is originally from the Department of Labor's Office of Foreign Labor Certification (OFLC). However, we are using the dataset from BuzzFeedNews which standardized the variable names, state abbriviations, and consolidates infromation about the visa agents. The raw data comes from H-2B applications that have been received and entered into the Department of Labor Tracking system. Specific information in the dataset about the employers was gathered through the foreign labor certification applications employers submitted. Data relating to wage levels was provided by the Bureau of Labor Statistics' Occupational Employment Statistics Program.

The data is sorted by fiscal year, from 2000 to 2013. Each observation is a different petition filed by an employer. The variables in the dataset are as follows:

case\_no: The OFLC-assigned case number.

visa\_type: "H-2A" or "H-2B".

fy: The fiscal year of the most recent OFLC decision/progress on the case.

last\_event\_date: The date of the most recent OFLC decision/progress on the case.

case\_status: The status of the case; typically a variation on "CERTIFIED", "DENIED", "WITHDRAWN", et cetera.

n\_requested: The number of workers/visas certified.

n\_certified: The number of workers/visas certified.

is\_certified: True/False; a standardization of the case\_status field.

certification\_begin\_date / certification\_begin\_date: "Actual date granted to an employer indicating when the need for the foreign workers to perform agricultural services or labor is expected to \[begin / end\]." Unavailable for H-2B data prior to FY2007.

job\_title: The job title listed by the employer.

employer\_name: The name of the employer applying for certification; converted to all-caps.

employer\_state: The state the employer listed.

employer\_city: The city the employer listed.

employer\_address\_1: The first line of the address the employer listed.

employer\_address\_2: The second line of the address the employer listed.

employer\_postal\_code: The postal code the employer listed.

agent\_name: The name of the agent or attorney filing the application for the employer. Some years of data include multiple columns related to visa agents; the standardized field combines these fields, separating them by a :.

organization\_flag: Various types of organizations — including sole employers and joint employers — can apply for visa certifications. This field tracks OFLC's categorizations. Only available for H-2A decisions.

is\_duplicate: True/False/null: This derived value will be True — indicating that this row corresponds a sub-application of a joint employer's "master application" — if (a) visa\_type is "H-2A", (b) the organization\_flag is blank, and (c) comes from fiscal year 2008 or later. H-2A data from FY 2006 and FY 2007 do not contain a organization\_flag field. For these records, and H-2B records, is\_duplicate will be null.

Section 2. Data analysis plan
-----------------------------

Section 3. Data
---------------
