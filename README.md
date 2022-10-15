# (Prosper loan Data Exploration)
## by (Utibe Edet Bassey)


## Dataset

This ‘Communicate Data Findings’ project is my final project in my Udacity Data Analyst 
Nano Degree Program.  
The dataset used for this project is the Prosper Loan Dataset which contains information 
from over 113,000 loans from Prosper marketplace which is a peer-to-peer lending marketplace 
in the United States founded in 2005. The dataset consists of 113937 rows with 81 variables 
(columns) on each loan, including loan original amount, borrower annual percentage rate, 
current loan status, borrower income, and many others. 


## Summary of Findings

After wrangling the data, I used Python visualization libraries to systematically explore the 
Prosper loan dataset, starting from plots of singles variables and building up to plots of 
multiple variables in the exploratory analysis phase.  In the exploration phase I selected 
some features to work with as I could not use the whole 81 columns and chose BorrowerAPR 
(Borrower Annual Percentage Rate) as my main feature of interest. Plotting BorrowerAPR against 
ProsperRating_Combined showed a negative correlation excluding the No Credit (NC) rating which 
was discontinued after July 2009. BorrowerAPR against IncomeRange also showed a negative 
correlation for IncomeRange from Very_low ($1-24,999) – High range ($100,000+). I selected 
rows that did not have any ProsperRating_Combined value to explore and was surprised to see that 
their borrower annual percentage rate (borrowerAPR) was even lower than those with ratings which 
led me to believe that IncomeRange was equally as important as the prosper rating. 

IncomeRange feature helped uncover the reason as to why more loans were taken in year 2013 
and why the number of loans dropped in year 2014. This was noticed when I plotted the BorrowerAPR 
across Year and IncomeRange as it showed the influx of Not_employed and Not_displayed IncomeRange 
in 2013 which influenced the number of loans gotten that year while the following year 2014 showed 
fewer IncomeRange borrowers only from Very_low to High. 

I also examined the relationship of other features and realized that though the DebtToIncomeRatio 
did not have any correlation with my main feature of interest (BorrowerAPR), it showed a weak 
negative correlation to ProsperRating_Combined. 


## Key Insights for Presentation

For the presentation, I focus on features that directly and indirectly influence my main feature of 
interest (BorrowerAPR).  I start by showing the distributions of BorrowerAPR, ProsperRating_Combined, 
IncomeRange, Year, Term, and LoanStatus (for borrowers without a ProsperRating). After which I proceed 
to discover relationships between the features. The boxplots show the relationship between Borrower APR 
versus Prosper Rating and Borrower APR versus Year. Lineplots for Borrower APR versus IncomeRange for 
borrowers with Prosper rating and borrowers without Prosper rating were plotted to comfirm if not having 
a Prosper rating would cause a borrower to have a have a high borrowerAPR. 
After establishing that Prosper rating influenced borrowerAPR, I went further to check what 
influenced Prosper rating by plotting a barplot of ProsperRating_Combined versus DebtToIncomeRatio 
to determine the relationship. I explored the relationships of 3 
variables to see if the addition of the third feature strengthened the relationship. Addition of 
IncomeRange to the BorrowerAPR versus Year plot revealed reasons for the Year distribution better 
than the bivariate plot of BorrowerAPR versus Year. 

The following changes were made for the explanatory analysis to polish the plots:
 - I set the ylim values to start from 0 and end at their respective maximum sizes for both lineplots 
   of IncomeRange against BorrowerAPR for borrowers with ProsperRating_Combined values and borrowers 
   without ProsperRating_Combined values so that they can be compared easily.

 - For the Borrower Annual Percentage Rate across ProsperRating_Combined and IncomeRange barplot, I 
   changed the location of the legend so as not to obstruct the view of the bars for High IncomeRange.

 - I changed the location of the legend for proper visibility of the DebtToIncomeRatio across 
   ProsperRating_Combined and IncomeRange plot.
