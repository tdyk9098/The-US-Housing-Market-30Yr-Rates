# The-US-Housing-Market-30Yr-Rates

# INTRODUCTION
The goal of this project is to develop machine learning models that attempt to predict the 30Yr Conforming mortgage rate of the following week using cross-sectional data. The algorithms were designed to be run at the end of the week using the closing print and the percent change from the following inputs:
- Eurodollar 3M
- S&P 500
- Lumber
- US Dollar

The historical data for the Eurodollar, S&P 500, Lumber, and USDOLLAR were all sourced from Investing.com. The Freddie Mac Mortgage rates were sourced from the Freddie Mac Research section of the website.

# RESULTS
# EURODOLLAR AND FED FUND
The Eurodollar is commonly used as the market’s 3M prediction for the Federal Reserve Rate (Fed Funds). This relationship is tested using monthly data through a simple linear regression and can be found in the notebook titled Eurodollar and Fed Funds.
-	Fed funds = -.25 + .981eurodollar
-	Slope has a Pval of 0
-	The negative intercept shows that the Effective Fed Funds rates are typically a quarter point below the predicted Fed Funds derived from the Eurodollar.
-	The Eurodollar accounts for 97% of the explained variance in the Effective Fed Funds rate.
-	When taking the monthly closing print of the Eurodollar and comparing the monthly Effective Fed Funds rate three months later: the relative mean absolute error is 11.39%, and the mean absolute error is .35%

# 30YR CONFORMING MORTGAGE RATES
- A simple linear regression model explains 85% of the variance of the 30Yr Conforming Mortgage Rates, with a relative mean absolute error of 8.8% and a mean absolute error of .45%. 
- A random forest regressor explains 98.5% of the variance of the 30Yr Conforming Mortgage Rates, with a relative mean absolute error of 2.4% and a mean absolute error of .12%.

# NOTES
This algorithm was last run on 11/8/22 and the predicted 30Yr Conforming rate for the week of 11/6-11/12 was 6.78% with a mean squared error range of 6.61%-6.97%. 
The algorithm will be forward-tested for four consecutive weeks and the results will be uploaded in this repository.

The actual rate for the week of 11/6-11/12 was 7.08%. Future real rates will be updated in the Excel sheet in this repository. 
