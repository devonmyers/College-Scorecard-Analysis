# College-Scorecard-Analysis

This repository contains code used for analyzing the College Scorecard.  The College Scorecard dataset contains institution-level data files for more than 20 years, and can be found at the following website: https://collegescorecard.ed.gov/data/.
At the time of the assignment, the most recent College Scorecard data (2019-2020) was used for analysis. 
Data was obtained by querying the College Scorecard web API, and several multiple regression models were constructed. 
The data was cleaned by checking for missing or erroneous data using the missing data feature in JMP 14 and records with missing outcome features were removed from the dataset.
After cleaning, feature extraction was completed using PCA to identify the most important features 
The model with the highest coefficient of determination and lowest mean squared error was chosen for further analysis.  
This model was a random forest regression model.

This was a multipurpose assignment:

1) What qualities make a school 'good'?  
2) Determining if Duquesne University qualifies as a 'good' school, based on (1).
3) What attributes can the university control?
4) The difference between Duquesne's predicted and actual performance.
5) What can Duquesne change, relative to its peers?  And, who are these peers?

The qualities that were considered for defining as 'good' are four-year retention rate, four-year pooled completion rate, and the ratio of 90th percentile student debt and 10-year median earnings. 
Note that these three qualities were used as outcome variables for analysis.
A school with high retention rate, which is percentage of students staying in the school from freshman through senior year, indicates that students feel comfortable at the university and wish to stay.  
Completion rate, the percentage of students that completed their program, should also be maximized for a good school.  
These first two metrics are on a scale of 0.0 to 1.0, which 0.0 indicating no retention and completion, and 1.0 indicating perfect retention and completion.
Lastly, the ratio of student debt to 10-year median earnings indicates how much students makes 10 years after leaving the university relative to the amount of debt incurred at the university.  
A low debt-to-earnings ratio (i.e., less than 1.0) would indicate that sutdents make more money 10 years after leaving the university than the amount of debt that they obtained at the university.
 
Duquesne's performance on the aforementioned metrics were 0.85, 0.80, 0.50 which means that Duquesne has high retention and completion rates, and a low debt-to-earnings ratio, so Duquesne University is a relatively good school.
The attributes that are controllable by the school are things such as amount of financial aid awarded, cost of attendance, number of program offered, etc.
Moreover, based on the random forest regression model that was constructed, the Duquesne's actaul performance exceeds its predicted results (see below)

|                 |  4 Year Retention | Rate	150% 4 Year Completion Rate| Debt-to-Earnings Ratio |
|  :-----------:  | :-----------:     |      :-----------:               |     :-----------:      |    
|Actual Outcome	  |    0.8547	        |           0.8038	               |          0.5022        |
|Predicted Outcome|  0.8436	          |           0.7267	               |          0.5178        | 
|Difference (Actual-Predicted)|  0.011|           0.0771	               |          -0.0156       |


Lastly, the hierarchical clustering feature in JMP 14 was used to identify which universities were among Duquesne's peers based on the input and outcome features.
Two of the most similar schools to Duquesne were University of Scrantion and Seattle University.
One of the outcomes of this assignment was to indicate to Duquesne that they should update their peer group by including these two universities among their peers.

