# ban5763-spring2024-sfrranalytics

**UPDATE 5 (Feb 19th 2024)**

1.a: What factors predict people’s preferences about where to work and where they feel most productive?

- Further decided to use the combination of PostC_impact_shift_A_focus, PostC_impact_shift_E_innovate as the target variable as the definition of productivity is to get tasks done efficiently.
- Two groups of variables make significant impact to where people feel most productive:
  - Productivity in Collaborative Settings (37% R2 affecting where people feel most productive): PostC_impact_shift_G_teammeetings, PostC_impact_shift_I_managersconnect, PostC_impact_shift_C_collab, PostC_impact_shift_F_colleagueaccess, PostC_impact_shift_D_videoconf; High productivity in collaborative settings indicates that employee feel productive at home and at office.
  - Home Office Satisfaction (32% R2 affecting where people feel most productive): SATSF_facilitate_Home_1A_focus, SATSF_facilitate_Home_1C_virtualcollab, SATSF_facilitate_HomeTech_3A_virtualcollab, SATSF_HomeOffice_E_seating, SATSF_facilitate_Home_1B_inpersoncollab, SATSF_facilitate_HomeTech_3C_virtualcollab, SATSF_HomeOffice_D_furniture, SATSF_facilitate_HomeTech_3B_inpersoncollab, SATSF_HomeOffice_C_CollabTools; High satisfaction in home office settings indicates that employee feel productive at home.
 - In short, employees feels productive when they have the ability to Participate in team meetings, Interact with managers, Connect via video conference, and Access and collaborate; or when they are satisfied with Settings for individual work, Settings for collaboration, and Environment comfort (seatings, furniture)
 - Productivity in collaborative settings can be improved by improving Ability for connect and social with others, Light levels while collaboration, and Accessibility with colleagues and superiors.
 - Home office satisfaction can be improved by improving Hardware and software (including meeting software) for work, Acoustic and natural light, and Furniture and seatings for collaborative settings.
 - Additional info: By comparing employees with unsatisfied and satisfied home settings, employees with satisfied home settings have 20% less distraction than opposing part.



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
