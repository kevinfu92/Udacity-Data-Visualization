# Loan Data Exploration

## Data set

The dataset contains information of 113937 loans and 81 attributes out of which 11 of them were discussed in this report: CreditGrade, Term, BorrowerAPR, ProsperScore, ListingCategory (numeric), EmploymentStatus, EmploymentStatusDuration, CreditScoreRangeLower, CreditScoreRangeUpper, StatedMonthlyIncome, and LoanOriginalAmount. The dataset can be accessed [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv) and the explanation of variables can be accessed [here](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0). <br><br>
The variable of interest in this report is APR of the loan, and the discussion will focus on the impact of each variable.

## Summary

Before data exploration, I created a new variable, `AvgCreditScore`, which is the average of `CreditScoreRangeLower` and  `CreditScoreRangeUpper`, and these 2 were removed from data exploration. 

During data exploration, I found that APR of a loan is mostly determined by **credit score** and **employment status**. The term of the loan (12 month vs. 36 month vs. 60 month) does not really affect the APR. The reason of the loan may have an effect on the APR. For example, the reason of the loan with lowest APR is personal loan and the one with highest APR is cosmetic procedure. For employment status, unemployed borrowers get higher APR unsurprisingly, and self employed borrowers gets highest APR among other type of employment (part-time and full-time) and also higher than retired borrowers. Interestingly, for borrowers with ProsperScore less than 6, the APR seems to be lower as the term of the loan increases. However, people with better ProsperScore were getting higher APRs as the term of the loan increases. Finally, it is also interestingly to discover that although APR correlates negatively with prosper score, borrowers with prosper score of 11 (highest) are getting higher APR than borrowers with prosper score of 10 (second highest). 

## Slide Deck Highlight

 - The APR of the loan follows unimodal distribution with an extra peak at around 0.36.
 - The peaks of loan amount are at \\$5000, \\$10000, \\$15000, \\$20000, and \\$25000.
 - Most borrowers have average credit score and prosper score.
 - APR trends negatively with credit score and prosper score of the borrower.
 - The APR of longer term loans are generally lower for borrowers with lower prosper score and higher for borrowers with higher prosper score. 
