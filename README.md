# Loan Data Exploration
## by Amicah Maina

This investigation is based on  Loan Data from Prosper Loans a Peer-to-Peer Lending company where individuals can either invest in personal loans or request to borrow money.

#### The prosper loans dataset contains over 100k observations with 81 variables with a date span of 9 years.. 
The columns are: ListingKey,ListingNumber,ListingCreationDate,CreditGrade,Term,LoanStatus,ClosedDate, BorrowerAPR, BorrowerRate, LenderYield, EstimatedEffectiveYield, EstimatedLoss, EstimatedReturn, ProsperRating (numeric), ProsperRating (Alpha), ProsperScore, ListingCategory, BorrowerState, Occupation, EmploymentStatus, EmploymentStatusDuration, IsBorrowerHomeowner, CurrentlyInGroup, GroupKey, DateCreditPulled, CreditScoreRangeLower, CreditScoreRangeUpper, FirstRecordedCreditLine, CurrentCreditLines, OpenCreditLines, TotalCreditLinespast7years, OpenRevolvingAccounts, OpenRevolvingMonthlyPayment, InquiriesLast6Months, TotalInquiries, CurrentDelinquencies, AmountDelinquent, DelinquenciesLast7Years, PublicRecordsLast10Years, PublicRecordsLast12Months, RevolvingCreditBalance, BankcardUtilization, AvailableBankcardCredit, TotalTrades, TradesNeverDelinquent, TradesOpenedLast6Months, DebtToIncomeRatio, IncomeRange, IncomeVerifiable, StatedMonthlyIncome, LoanKey, TotalProsperLoans, TotalProsperPaymentsBilled, OnTimeProsperPayments, ProsperPaymentsLessThanOneMonthLate, ProsperPaymentsOneMonthPlusLate, ProsperPrincipalBorrowed, ProsperPrincipalOutstanding, ScorexChangeAtTimeOfListing, LoanCurrentDaysDelinquent, LoanFirstDefaultedCycleNumber, LoanMonthsSinceOrigination, LoanNumber, LoanOriginalAmount, LoanOriginationDate, LoanOriginationQuarter, MemberKey, MonthlyLoanPayment, LP_CustomerPayments, LP_CustomerPrincipalPayments, LP_InterestandFees, LP_ServiceFees, LP_CollectionFees, LP_GrossPrincipalLoss, LP_NetPrincipalLoss, LP_NonPrincipalRecoverypayments, PercentFunded, Recommendations, InvestmentFromFriendsCount, InvestmentFromFriendsAmount, Investors.

The goal was to determine the best variables and fields that can be used to predict how the BorrowerRate will be assigned to a listing. 

The main variables of interest I identified were:
- `CreditGrade`
- `LoanStatus`
- `BorrowerAPR`
- `LenderYield`
- `BorrowerState`
- `ProsperRatingNumeric`
- `ProsperScore`
- `LoanOriginalAmount`
- `Investors`
- `EmploymentStatus`
- `CreditScoreRangeUpper`
- `CreditScoreRangeLower`
- `EstimatedLoss`

Additional Variable I considered are:

- `DebtToIncomeRatio`
- `MonthlyLoanPayment`

I used Univariate exploration of the variables, then combined them in pair on Bivariate exploration then in multiple on Multivariate Exploration.

## Summary of Findings
The nature of the relationships discovered were:
- Strong Positive corelation between Borrower Rate and the variables; BorrowerAPR, LenderYield and EstimatedLoss.
- A negative correlation between the BorrowerRate and the Categorical variables; ProsperScore, ProsperRatingNumeric and CreditGrade.
- Negative Correlation was also observed between the BorrowerRate and the CreditScoreRangeUpper and lower.
- Weak Negative Correlation was observed between LoanOriginalAmount and Investors with BorrowerRate.
- Interesting relationship was also observed between the EmploymentStatus of a borrower and the BorrowerRates.Where a higher count of loans was for employed borrowers as compared to not-available and unemployed. This relationship was also right skewed, showing a lower borrowerrate for employed borrowers particularly Full-time employees.
- DebtToIncomeRatio exhibited weak positive correlation with BorrowerRate.
- MonthlyLoanPayment exhibited weak negative Correlation with BorrowerRate.


## Key Insights
With the nature of variable relationships a few key insights were made;

1. With a low Prosper Score, which is a risk score for the insights which spans from 1-11 11 being the favorable score, combined with a high credit rating it is highly probable to have a low Estimated Loss for the loan and hence have a low Borrower Rate.

2. A higher loan amount can result into a lower Borrower Rate, which is strengthened by a low risk score for the loan. However, the Borrower Rate assigned does have a limit where at the lowest risk score, with the highest loan amount this limit cannot be surpassed. 

3. The employment status of an individual and their Income Range will determine the average BorrowerRate assigned for their loan listing. 




