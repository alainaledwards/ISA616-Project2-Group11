# Overview of the Repository

The purpose of this repository is to interact with GitHub to access the files for our second project in ISA 616. 

## Data Insight Question
We will explore what majors have the best/worst placement results in terms of percentages and salary levels. This question was given to us by Mr. Kirk Bogard to inform him in his role in Development and External Relations.

## Contributors
Marti Walstad and Alaina Edwards

## Business Value Proposition

![BVP - Student Sucess](https://github.com/alainaledwards/ISA616-Project2-Group11/assets/146125942/55de55b1-3225-4caa-b900-76ae07b2981d)

1. Define the client or audience for your data analysis solution.
  Our client for this project is Kirk Bogard, Associate Vice President for Development and External Relations in FSB.
2. Define the client jobs.  What jobs are your clients trying to get done.  Use a separate bullet point for each job you intend to help your client get done.
  *  Inform FSB rankings
  *  Make case for admission (showing parents and students the placement reults through percentages and salary levels)
  *  Attracting other companies to recruit from FSB
  *  FSB Brand Management -- evidence to support claims made
  *  Show which majors have the best / worst placement results in terms of percentages
  *  Show which majors have best / worst placement results in terms of salary levels
4. Add pains.  What are the pains before, during, and after your client is trying to get their jobs done?  Create a bullet point for every specific pain.
  *  Before:
      *  Students not filling out survey to get information
  * During:
      * Inputation errors -- missing variables (average salaries: student adding salary to survey vs external relations have to find salary online)
  * After:
      *  Not having enough support and evidence to back up brand management claims
      * Lacking information to recruit prospective students into certain FSB
5. Describe your intended solution.  Give a bullet point for each major element of your product or solution.
  Our intended solution is a dashboard showing statistics with FSB majors best / worst placements, specifically percentages and salary levels.
  *  Using Student Success data from 2019-2021
  *  Missing data will be filled in (missing salaries)
  *  Give statistics to be used in marketing that will be appealing to future prospective students about FSB majors
6. What are the pain killers from your solution? You should be able to map a pain killer to a client pain.
  *  Using national averages and public data to input missing salary values
  *  Imrpove prospective student recruitment
  *  Using salary statistics to back up our Top 10 ranking for ROI claim
  *  Having the data avaliable to support any other brand management claims
7. Add gains.  What else might your solution deliver that will surprise or benefit your client above and beyond simply killing their pain?
  *  Guide future marketing programs -- finding more data to support future rankings or statistics
  *  Strengthen relationships with companies who currently recruit out of FSB -- proving our continued success to encourage companies to keep returning to Miami career fairs, etc.
  *  Evidence to show Covid year didn't affect students post-grad placements
8. What are the gain creators?   You should be able to map a gain creator to a client gain.
  *  Student salary and major statistics guiding brand management and marketing 
  *  Generating compelling statistics to best market to prospective student and parents based on major focus
  *  Learning about FSB strengths through exploring covid data -- data didn't change through this year
    *  We can use this internally to learn what recruiting works best
    *  Helps strengthen company relationships and show to prospective students that even during Covid FSB students were still placing well in terms of percentages and salary levels

## Project Overview

Annually, the FSB conducts a senior survey of graduates to learn of their employment status.  In addition, information is verified using LinkedIn and employer survey information.  The data you are provided ('FSB_BI_Survey_2019_2021.rds') contains data on graduates for 2019, 2020, and 2021.  The data are merged from two sources:  the senior survey, and data from the Miami University database.  

The data are anonymized, however it is possible that if you look hard enough, you can identify students.  You are bound, ethically not to do so.  It is a strict ethical code that you will not discuss individual data points with ANYONE except for me and your team.  Failure to comply with this code of ethics will result in a failing grade in the course.  

## Data Sources

You have three years of data representing FSB graduates, including graduates in 2019, 2020, and 2021.  The dataset provided had 42 variables.  The source is either derived by me during data cleaning/merging, from the Oracle Business Intelligence Enterprise Edition (OBIEE) maintained by Miami adminsitration, or from the self reported senior survey.  I have cleaned and merged the files into one file.  

1.  nmajor: numeric,derived, the number of majors 
2.  major1: text, OBIEE, first major
3.  major 2: text, OBIEE, second major
4.  BBRJ: binary, OBIEE, an attribute of a student, but we do not know what this stands for
5.  Business Direct Admit: binary, OBIEE, a direct admit to FSB as a first year
6.  Combined Cacc and Masters: binary, OBIEE, combined degree student
7.  Dean's List: binary, OBIEE, achieve dean's list status at least once
8.  First Generation College Stdnt: binary, OBIEE, first generation student status
9.  FSB Scholars: binary, OBIEE, FSB scholars program
10.  Honors Program: binary, OBIEE, member of University honors program
11.  President's list: binary, OBIEE, achieved president's list at least once
12.  Study Abroud Courtesy Account: binary, OBIEE, do not know meaning
13.  Transfer Work: binary, OBIEE, do not know exact meaning
14.  Cum Laude: binary, OBIEE, graduated Cum Laude
15.  Magna Cum Laude: binary, OBIEE, graduated Magna Cum Laude
16.  Summa Cum Laude: binary, OBIEE, graduated Summa Cum Laude
17.  University Honors: binary, OBIEE, graduated with University Honors
18.  University Honors w/Distinction: binary, OBIEE, graduated with University Honors with Distinction
19.  minor1: text, OBIEE, first listed minor
20.  minor2: text, OBIEE, second listed minor
21.  IPEDS.Race.Ethnicity: text, OBIEE, race/ethnicity
22.  Gender: text, OBIEE, sex
23.  GPA.Range: text, OBIEE, GPA within a .5 range
24.  Term.Code: numberic, OBIEE, First four digits are the physcal year (beginning in July, e.g. July 2020 is FY 2021).  Last two digits is the term (10=fall, 15=winter, 20=spring, 30=summer).
25.  Year.x: text, derived, first four digits of Term.Code stored as a character variable
26.  latin_honors: text, survey, latin honors designation
27.  survey_city: text, survey, student reported city in which their job is located
28.  survey_company: text, survey, student reported company in which they accepted a job
29.  survey_deptfunc: text, survey, student reported job function
30.  survey_gradprogram: text, survey, student reported graduate program they will be attending
31.  survey_gradschool: text, survey, stuent reported graduate school they will be attending
32.  survey_internfour: text, survey, student reported fourth internship they held during college
33.  survey_internthree: text, survey, student reported third internship they held during college
34.  survey_interntwo: text, survey, student reported second internship they held during college
35.  survey_internone: text, survey, student reported first internship they held during college
36.  Survey_internships: text, survey, Student reported number of internships they held during college
37.  survey_offers: text, survey, student reported number of offers for full time employment received
38.  survey_plans: text, survey, student reported plans after graduation
39.  survey_pref_field: text, survey, student reported whether working in preferred field
40.  survey_pref_loc: text, survey, student reported whether working in preferred location
41.  survey_salary: numeric, survey, student reported salary
42.  survey_state: text, survey, student reported state in which job is located
