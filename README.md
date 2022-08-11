# (Dataset Exploration Title)
## by (your name here)


## Dataset

> The dataset used in this analysis is the Loan data by Prosper. The data is provided as a csv file with 113,937 loans with 81 variables on each loan. The data is loaded using the URL provided in the project workspace resource for linked files which an amazon s3 storage URL.
> The Data has so many features but since this analysis is focused on factors that affect the loan status, the following data wrangling steps were performed
> 1. Data without a prosper rating were removed
> 2. Removal of unneeded columns
> 2. Datatype of LoanOriginationDate was changed from object to date
> 3. ProsperRating (Alpha) and listingCategory (numeric) were renamed to ProsperRating and listingCategory respectively
> 4. Encoding of listingCategory with information in the data dictionary
> 5. Creation of a new column to hold the Loan Origination Year from LoanOriginationDate to allow analysis by year of Loan Origination

> The Wrangling steps listed above reduced the dataset to 84,853 loans and 14 features

## Summary of Findings

> I investigated the features LoanStatus, EmploymentStatus, StatedMonthlyIncome, Term and IncomeRange. Majority of the Loan have term of 36 months and are taken by people who are employed, more loans were given to people who have earnings between income range [25,000 - 74,999], surprisingly, people earning higher than this range seem to take lesser loan. Also I observed that majority of the loan originated in year 2013 and they have a loan status of current with few defaults

>ListingCategories Debt Consolidation, Wedding Loans, Baby&Adoption, Business and Home Improvement have Loan Amount with higher ranges of default. Also Income range from 25K to 100K have the highest loan ranges with defaults. Persons with Loan Rating AA and A usually take loans with higher term, persons with Loan Rating D go for short term loans. Lower loan amount between 4k to 5k over a 12 month term tend to default more on loans taken

> A Surpriisng discovery is that Majority of Loans with Term of 12 months have lower Loans category and less defaults. Another surprising interaction is that most loans with defaults are from employed persons, those with no earnings (0 dollars and not employed) seem to complete their loans. Loans with higher amount over a 60 month term seem to complete but default when the term is shorter even for persons in higher Income Range. Also the number of defaulted loans have reduced after it peaked in the year 2013 most like because the company reduced the number of loans after 2013


## Key Insights for Presentation

> The exploration is all about Loan status and what factors can affect the loan status. The following features have been observed to have effect on the loan status
>1. Employment Status
>2. Income Range
>3. Term
>4. BorrowerRate
>5. ListingCategory
>6. ProsperRating

> Most Loans are given to employed persons, but it has been observed through this analysis that most persons within the income range [25,000 to 49,999] seem to default more on their loans, for this kind of persons, it has been observed that when the listing category is for wedding and Baby&Adoption, the default rate is high, the company might need to take this into consideration for other persons requesting for loans.
Also, the higher the BorrowerRate, the higher the probabily that the persons will default, hence, due dilligence needs to be carried out to know if the ProsperRating is HR, D and E which seem to be the ProsperRating with more Defaults