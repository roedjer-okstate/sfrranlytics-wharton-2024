# ban5763-spring2024-sfrranalytics

**LAST UPDATE (Apr 29th 2024)**

Watched the winning team's (MetroMinds - NYU) Presentation At WPAC Conference. Learnings are below

- Analysis was very similar to ours. They also used composite scores and visualized effect on workplace preference rate.
- They performed ANOVA to look at differences across Job families (Business Ops, Customer Support and Sales etc.)
- They also performed a decision tree and showcased the level of depth in trees and variety of factors that could potentially be studied.
- One stand out recommendation was to have different kinds of enviornments for different roles - Customer Support (less vibrant), Tech roles (High activity spaces) etc. This was great.
- Rest of the recommendations were standard - Giving employees a budget to setup office spaces, Flexible Work Scheduling (Hot desk system) etc.
  
Report Status - 95% Complete. 
- Almost done with the report. Working on formatting it better.
- Frankle Muchahary, Ritwik Roy Chowdhury, Roe Djer Tan, and Shreyan Datta Chakraborty would like to say thank you to the professors for helping and guiding us throughout this project. It was a fantastic experience participating in Wharton People Analytics Case Competition.

Regards,
Team SFRR Analytics


**UPDATE 9 (April 15th  2024)**
Report Status - 70% Complete. 

Executive Summary - Roger
Introduction - Shreyan (Complete)
Project Objectives - Shreyan (Complete)
Data Visualization - Roger (Complete)
Data Analysis - Frankle & Roy (Complete)
Generalization/Explanation - Frankle & Roy (In Progress)
Future Scope - Frankle (In Progress)
Conclusion - Roy (In Progress)
Update Github Repo - All (In Progress)

**UPDATE 8 (April 8th  2024)**
Report Status - 40% Complete. Did not make too much progress due to engagements at work.

Executive Summary - Roger
Introduction - Shreyan (Complete)
Project Objectives - Shreyan (Complete)
Data Visualization - Roger (In Progress)
Data Analysis - Frankle & Roy (First Draft Complete -- need to review)
Generalization/Explanation - Frankle & Roy (In Progress)
Future Scope - Frankle
Conclusion - Roy
Update Github Repo - All

**UPDATE 8 (April 1st  2024)**
Report Status - 20% Complete

Executive Summary - Roger
Introduction - Shreyan (Complete)
Project Objectives - Shreyan (In Progress)
Data Visualization - Roger (In Progress)
Data Analysis - Frankle & Roy (In Progress)
Generalization/Explanation - Frankle & Roy
Future Scope - Frankle
Conclusion - Roy
Update Github Repo - All

**UPDATE 7 (Mar 25th 2024)**
Distributed tasks for all team members to work on the report. Here is the summary of the distribution:

Executive Summary - Roger
Introduction - Shreyan
Project Objectives - Shreyan
Data Visualization - Roger & Shreyan
Data Analysis - Frankle & Roy
Generalization/Explanation - Frankle & Roy
Future Scope - Frankle
Conclusion - Roy
Update Github Repo - All

**UPDATE 6 (Mar 11th 2024)**
- Built further upon our previous work on modeling with respect to different organizations. Segregated at each individual organization level. Will look into grouping organizations next.
    - Organizations having similar types of departments like Org3 and Org1 (Construction/Architecture) had similar key features driving their workplace preferences. They seemed to have a hybrid preference.
    - Similarly, Org2 and Org5 (IT Org) also had similar key features driving their importance.
    - It might be useful to deduce the "nature of work" done by a company based on the departments with majority employees and group them together based on that. Will help us get more datapoints for some orgs like Org 1 that had only around 70 data points. 
- Learnt about feature hashing. Will work on experimenting with that that in the coming weeks.
- Worked on improving our Gen AI-based bot responses using Retrieval Augmented Generation (our third recommendation). The topic for BAN5763 was LLMs this week, so, we thought it would be a good learning experience.

**UPDATE 6 (Mar 11th 2024)**
- Explore other composite variables in modeling
- Addition of other factors like health and wellbeing quotient, distance to office etc. to build a more compelling story.
- Explore feature hashing
- Check if we build model with respect to different organizations. We can seggregate the organizations based on the timeline of the survey.
- Waiting for WPAC to upload all the finalists' analysis. We can take queues from there on how to improve our analysis.


**UPDATE 5 (Feb 19th 2024)**

1.a) What factors predict people’s preferences about where to work and where they feel most productive?

- Further decided to use the combination of PostC_impact_shift_A_focus, PostC_impact_shift_E_innovate as the target variable as the definition of productivity is to get tasks done efficiently.
- Two groups of variables make significant impact to where people feel most productive:
  - Productivity in Collaborative Settings (37% R2 affecting where people feel most productive): PostC_impact_shift_G_teammeetings, PostC_impact_shift_I_managersconnect, PostC_impact_shift_C_collab, PostC_impact_shift_F_colleagueaccess, PostC_impact_shift_D_videoconf; High productivity in collaborative settings indicates that employee feel productive at home and at office.
  - Home Office Satisfaction (32% R2 affecting where people feel most productive): SATSF_facilitate_Home_1A_focus, SATSF_facilitate_Home_1C_virtualcollab, SATSF_facilitate_HomeTech_3A_virtualcollab, SATSF_HomeOffice_E_seating, SATSF_facilitate_Home_1B_inpersoncollab, SATSF_facilitate_HomeTech_3C_virtualcollab, SATSF_HomeOffice_D_furniture, SATSF_facilitate_HomeTech_3B_inpersoncollab, SATSF_HomeOffice_C_CollabTools; High satisfaction in home office settings indicates that employee feel productive at home.
 - In short, employees feels productive when they have the ability to Participate in team meetings, Interact with managers, Connect via video conference, and Access and collaborate; or when they are satisfied with Settings for individual work, Settings for collaboration, and Environment comfort (seatings, furniture)
 - Productivity in collaborative settings can be improved by improving Ability for connect and social with others, Light levels while collaboration, and Accessibility with colleagues and superiors.
 - Home office satisfaction can be improved by improving Hardware and software (including meeting software) for work, Acoustic and natural light, and Furniture and seatings for collaborative settings.
 - Additional info: By comparing employees with unsatisfied and satisfied home settings, employees with satisfied home settings have 20% less distraction than opposing part.

1.b) What affects preference to work from home/office
 
Bucketed variables into multiple categories that are most sound with external research. Explored relationships aginst employee work preference against them. Categories are:
 
1. Collaboration Quotient: Mix of variables like access to colleagues, team meetings, managers, clients etc. Found that those have have more collaborative work tend to prefer working from office. Moreover, people have diff levels of comfort from diff environments.
 
2. Wellbeing Quotient: Includes vars like Work life separation and health & wellness preferences. Found that those who rate these highly prefer mostly WFH.
 
3. Distraction Factors: Includes multiple observation factors like distraction due to desk visitors, environment (lights, noise...), technology issues etc. Found that each variable has different meaning with preference. Eg: people losing more time due to noise prefer WFH whereas those who lose more time due to tech challenges prefer work from office. Backed this up with "Environmental Quotient" which shows employees' preferences towards aforementioned vars.
 
4. Tech Quotient: Assesses preference for access to tech tools. Those who rate this highly prefer working from office.
 
5. Commute Quotient: Includes safety and commute vars. Those who think long commutes are painful prefer WFH.
 
6. Org Culture Quotient: Includes Social events, leadership policy, community etc. Those who find these important prefer work from office.
 
Generally found that PostCovid most people shifting to WFH or Hybrid situation. People prefer to go to work based on aforementioned factors and their roles. Productivity metrics and all Quotients help is define segments.
 
**Segmentation**
 
- Broadly classified into 3 groups: People who prefer WFH, Hybrid or WF Office.

Assessing the impact of previous variables on these groups and what drives them to prefer working from wherever.
 
- Finding concentration of work roles (Accounting, Marketing, Sales etc.) within these groups to show what they're composed of.
 
- Vetting their prefernce against satisfaction to show gaps in current work situation vs what would make them more satisfied.
 
- Exercise allows us to setup foundational gaps in these groups to segway into recommendations. Focus on what are these groups, what do they prefer, what problems are they facing and how are their satisfaction levels right now?

**Simple Model**
 
Creating a Decision Tree model to predict what would be peoples' WFH rates and using the factors to build a Rule Based process. 
 
**Usable Product - Dashboard**
 
Allows executives to see what factors contribute to preferences in our 3 segmented groups.
Highlights problems in their Quotients and where there are vulnerabilities
Uses some GenAI to summarize most important insights based on which group is selected.
Work In Progress: Trying to quantify upliftment by comparing employee satisfaction between unsatisfied groups and satisfied groups. Delta shows the effect of interventions. 

<br>
<br>

**UPDATE 4 (Feb 16th 2024)**


This update contains our notes from the work and the Q&A call that took place on 2/15.

Q&A Call
- Different organizations have different survey structures. Lot of missing data between variables so story needs to be constructed carefully.
- Asked when businesses explore the need for surveying + action. Found that they usually have a goal in mind but questions cannot be too naunced or it will be biased.
 
 
1.a: What factors predict people’s preferences about where to work and where they feel most productive?
Decided to use the combination of PostC_impact_shift_A_focus, PostC_impact_shift_B_productive, PostC_impact_shift_C_collab, and PostC_impact_shift_E_innovate as a proxy target variable for "where they feel most productive".
Currently investigating the relationship between chosen variables and the proxy target variable: 
Distraction variables (OBSV_PreC_5A_lost_layout to OBSV_PreC_5L_lost_indoorlight) - more distractions could lead to low productivity
Interactive work variables - the nature and frequency of interactive work may affect productivity in different settings
DEMO_meeting_remote - ability to conduct meetings or work that cannot be done remotely, indicating the necessity for in-person collaboration, may affect productivity in different settings
Influential Factors - factors influence their decision to work from home or in the office may directly influence their productivity in different settings
 
1.b: What can we learn about the factors that determine when people prefer to work from the office and when they prefer to be remote?
 
- Continuing the train of thought and using a combination of similar + different variables from question 1.a (productivity preference) to build a story.
- Trying to build the story such that we pick up influential factors from each bucket that cover variety of work-related factors like fraction of work time spent in meetings, type of work (collaborative/individual), health and wellness priority, productivity/distraction metrics, ability to enjoy work at specific environments etc.
 
Things we found interesting:
- Commute Length: Direct relationship with preference to work at office/remote.
- Pre-covid meeting style: Fraction of calls (Pre-Covid) wherein at least 1 person joined online shows preference to work remote in today's world.
- Productivity: Pre-covid those who spent considerable time being distracted at work now prefer working at home and are more satisfied.
- Work Enjoyment: Effect of innovation/creation and focus driven work is more enjoyable when people are in their preferred environments. They tend to prefer working from home/office based on these metrics.
- Collaboration: Those who have roles that require more in-person collaboration would prefer going into office whereas those spending most time on calls prefer home.
-  Health & Wellness: People who prioritze health and family prefer working at home. They're more satisfied and creative when they can juggle between these important parts easily.
- Work Life Separation: Ultimately, work-life balance is crucial for people selecting their preferred work environment.
- Still exploring for other variables that signify exact role structure, affinity for leadership + purposeful roles, % of time spent in office vs outside of office (sedentary/laborious roles), impact of access to technology and social structures etc.

2.
- Looking at the different variables to understand how we can segment the data. We have looked at variables related to the Departments.
- The way that the employees have responded to questions Post Covid can be a way to judge the sentiments of the people since they have theoretically experienced the way that work was before COVID and can compare it to th one after COVID.
- The next two important set of variables are preference and satisfaction with respect to the work place environment.
- We will try out different combinations of these variables and ultimately shortlist it to the final variables based on the already conducted secondary research and the variables that are important in our modelling.

  3.
- We are keeping this very open ended at this point but have a few ideas that we would want to explore especially knowing the kind of industries that this survey was sent along with the timeline.
- We will make sure that our reccomendations are mostly role specific and not organization specific as we cannot identify an individual with their organization and due to the missing values.

**UPDATE 3 (Feb 11th 2024)**  
- Broken down the problem statement into multiple individual supervised and unsupervised problems.
- Problem Statement 1: Using a simple decision tree model to extract rules, study the rules, understand feature importance, and carry out SHAP analysis.  
    - Using the `% ratio of days` as the target variable for the first problem to understand factors that influence workplace environment preference for an employee
    - The variables related perceived impact of the work environment on the distributed nature of the work (post covid) have a very significant influence on the preference (based on Global SHAP Analysis). Personal preferences and specific work type-related preferences also make an impact.
    - Local SHAP Analysis was carried out to get a deeper understanding of each factor and how they lead to the decisions made by the employees. Approach: Bucket the target variable ratios into three different buckets (Low, High, Medium) and take 10-20 random samples from each bucket. Create force plots to analyze visually how the different factors affect the decision-making in each of the three buckets. Look for common patterns.
- Problem Statement 2: Use the key variables determined by the model from Problem Statement 1 to group the customers into 3-4 different groups using hierarchical clustering. Profile the groups based on the perspective of an employer such that certain common arrangements can be made according to employee preferences.


**UPDATE 2 (Feb 9th 2024)**
- Split the survey data (high number of variables) into different categories like Workplace Features, Space Type & Preferences, and Influential Factors.
- Carried out some preliminary univariate analysis, some example findings are:
    - Demographic: Most respondents worked in Finance and Engineering.
    - Influential Factor driving respondents to the office: Awareness that many will be at the office that day (most influential) | food (least influential)
    - Mobility: Respondents spent on average 0.75 days WFH and 218 minutes commuting in a week during pre-Covid period
    - Interactive Work: Respondents spent on average 62% of the time interacting with others in the same physical space during pre-Covid period
    - Space Type & Preferences: Respondents were observed to spend on average 1,200 minutes on work desks in the office in a week during pre-Covid period | 31% preferred home while 26% preferred work/desk when it comes to focused work.
    - Workplace Satisfaction: More respondents were satisfied with focused work at home but more respondents were statisfied with inperson collaboration at office.
    - Impact Distribution Work: The respondents think that office has the strongest support for social connection and home has the best ability to connect via video conferences.
    - Environment Preference: Strongest preference for focused work - quiet environment | Strongest preference for collaboration work - bright lightings
    - Workplace Characteristics: Many are satisfied with current office's characteristic of space for knowledge-sharing | Most think that a space that can foster a sense of pride in the work of the organization is most important.
    - Workstyle: More than half of the respondents spent more than 70% of their work time to work on individual assignments.
    - Workplace Features: Currrently, technology is the most satisfied feature for both office and home office | Technology is the most important feature for office | Lockers, food, kitchen, gym, greenspace and event are unimportant features for work while chairs and privacy are important.
    - Etc: Excluding unanwered respondents, ~64% of remaining respondents agree to have freedom in choosing either WFH or work in the office.

**UPDATE 1 (Feb 4th 2024)**
- All team members to explore the data, and carry out external research for understanding factors influencing workplace preferences. Come back on Wednesday and share findings with each other.
- Subtask Division - Topics to focus on:
    - Frankle: Question 1 Part 2 (Location Preference)
    - Roger: Are there any patterns across groups of employees? (Segmentation) 
    - Roy: Question 1 Part 1 (Productivity Factors)
    - Shreyan: Organizational Factors vs Employee-centric Factors 
