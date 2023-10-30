# Overview of the Repository

The purpose of this repository is to interact with GitHub to access the files for our second project in ISA 616. 

## Data Insight Question
We will explore what majors have the best/worst placement results in terms of percentages and salary levels. This question was given to us by Mr. Kirk Bogard to inform him in his role in Development and External Relations.

## Contributors
Marti Walstad and Alaina Edwards

## Business Value Proposition

![BVP - Student Sucess](https://github.com/alainaledwards/ISA616-Project2-Group11/assets/146125942/55de55b1-3225-4caa-b900-76ae07b2981d)

1. Define the client or audience for your data analysis solution.
    * Our client for this project is Kirk Bogard, Associate Vice President for Development and External Relations in FSB.
2. Define the client jobs.  What jobs are your clients trying to get done.  Use a separate bullet point for each job you intend to help your client get done.
    *  Inform FSB rankings
    *  Make case for admission (showing parents and students the placement reults through percentages and salary levels)
    *  Attracting other companies to recruit from FSB
    *  FSB Brand Management -- evidence to support claims made
    *  Show which majors have the best / worst placement results in terms of percentages
    *  Show which majors have best / worst placement results in terms of salary levels
4. Add pains.  What are the pains before, during, and after your client is trying to get their jobs done?  Create a bullet point for every specific pain.
    *  Before:
        *  Client stated students not filling out survey to get information was a pain. 
    * During:
        * Inputation errors -- missing variables (average salaries: student adding salary to survey vs external relations have to find salary online)
    * After:
        *  Not having enough support and evidence to back up brand management claims (Top 10 ranking for ROI)
        * Lacking information to best recruit prospective students into certain FSB programs
5. Describe your intended solution.  Give a bullet point for each major element of your product or solution.
      * Our intended solution is a dashboard showing statistics with FSB majors best / worst placements, specifically percentages and salary levels.
      *  Using Student Success data from 2019-2021
      *  Missing data will be filled in (missing salaries)
      *  Give statistics to be used in marketing that will be appealing to future prospective students about FSB majors
6. What are the pain killers from your solution? You should be able to map a pain killer to a client pain.
    *  Using national averages and public data to input missing salary values -- external relations won't have to spend time searching for missing data 
    *  Improve prospective student recruitment -- find data to use in marketing based on the specific majors  
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

Annually, the FSB conducts a senior survey of graduates to learn of their employment status.  In addition, information is verified using LinkedIn and employer survey information.  The data provided ('FSB_BI_Survey_2019_2021.rds') contains data on graduates for 2019, 2020, and 2021.  The data are merged from two sources:  the senior survey, and data from the Miami University database.  Based on this data, we are to answer our data insight question to address our client's needs and pains. 

## Data Sources

There are three years of data representing FSB graduates, including graduates in 2019, 2020, and 2021.  The dataset provided had 42 variables.  The source is either derived by me during data cleaning/merging, from the Oracle Business Intelligence Enterprise Edition (OBIEE) maintained by Miami adminsitration, or from the self reported senior survey.  It was cleaned and merged the files into one file.  We took the 42 variables and cleaned them down to 16 variable that were the most useful to our data insight question.  

1.  Major: text, OBIEE, first major
2.  FirstGen: binary, OBIEE, first generation student status
3.  Honors: binary, OBIEE, member of University honors program
4.  Minor: text, OBIEE, first listed minor
5.  RaceEthnicity: text, OBIEE, race/ethnicity
6.  Gender: text, OBIEE, sex
7.  GPARange: text, OBIEE, GPA within a .5 range
8.  Year: text, derived, first four digits of Term.Code stored as a character variable
9.  InternOne: text, survey, student reported first internship they held during college
10. InternTwo: text, survey, student reported second internship they held during college
11. InternThree: text, survey, student reported third internship they held during college
12. InternFour: text, survey, student reported fourth internship they held during college
13. InternshipCount: text, survey, Student reported number of internships they held during college
14. OfferCount: text, survey, student reported number of offers for full time employment received
15. Plans: text, survey, student reported plans after graduation
16. Salary: numeric, survey, student reported salary

## Contents of Folder
1. .gitignore: ignores certain data that is listed
2. 231003 FSB Student Success: Contains BVP and image, sets working directory and imports data, project overview, original data sources
4. 231011 FSB Student Success: Cleans data--import data and load variables, removes unecessary variables, explore missing data and handle this missing data, renames columns, reorders columns, verify cleaned data to export as RDS
5. 231012 FSB Student Success: includes session information along with cleaning the data--allows reproducibility
6. 231015 FSB Student Success: Dashboard template based on data insight question includes data exploration overview and written insights
7. 231022 FSB Student Success: Final Dashboard with graphs to answer data insight question
8. 231029 FSB Student Success: Final Dashboard with graphs to answer data insight question; includes our conclusions and insights taken from the graphs
9. Analytics Class Project from Client: Project information--client, data insight questions
10. FSB_BI_Survey_2019_2021: original data from FSB senior surveys
11. ISA616-CareerProj: includes saved data used in process of cleaning and exporting to our final analysis
12. README: contains BVP, data insight question, updated data source with variables, explanation of files
13. Student Template for accessing Svc data:
14. cleaned_FSB_Student_Success: file with final cleaned data
15. missing_data_df: Shows variables with missing variables

## Final Student Success Deliverable
Our final dashboard delivered to Mr. Kirk Bogard addresses the pains and needs we stated for exploring what FSB majors have the best/worst placement in terms of percentages and salary levels. We were able to successfully determine what variables would work best in this solution, and clean the data based on this. We also renamed and reorderd variables to make our results more user friendly to our client. In our dashboard template we used our cleaned data to create graphs that meaningfully represented the solution to our data insight question. First, we created two graphs one to show the average salary by major and another to show the number of responses for salary by major. This second graph shows how data could be skewed based on the number of responses. Next, we used factors of First Generation Students, Honors, and Minor to show salaries based on major. Finally, we gave graphs on salary by major for each of the years, 2019-2021 that we had survey data from. Our graphs can provide meaningful statistics to be used in marketing that will be appealing to future prospective students, and also help inform FSB rankings. Using all of our graphs we are able to help address our client's needs and pains.  
