# ban5763-spring2024-sfrranalytics

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
