## Term Deposit Campaign - Banking Telesales Analytics

# Project Overview 
This project focuses on analyzing data from telesales marketing from a Portuguese banking institution. 
- Business Goal: Increasing the number of customers subscribed to term deposits and optimizing the telesales strategy.
- Method: Using descriptive analytics to identify potential customer segments  and evaluate the effectiveness of the calling method.
  
# Data Overview
- Datasource: [Moro et al., 2011] S. Moro, R. Laureano and P. Cortez. Using Data Mining for Bank Direct Marketing: An Application of the CRISP-DM Methodology. In P. Novais et al. (Eds.), Proceedings of the European Simulation and Modelling Conference - ESM'2011, pp. 117-121, Guimarães, Portugal, October, 2011. EUROSIS.
- Number of Instances: 45,211 records
- Target variable (y): Has the client subscribed to a term deposit? (Yes, No)
- Main attribute:
  * Customer information: Age, Job, Marital, Education, Balance, Default,  Housing Loan, Personal Loan.
  * Campaign information: Call type, Date, Month, Duration.
  * Call History: Number of previous contacts, result of previous campaigns.
    
# Executive Summary  
Result overview: 
- 45,211 contacts -> 5,289 subscribed
- Conversion rate: 11.7%
- Average 2.76 calls/customer

The purpose is to identify which factors affect the decision to open a term deposit and provide a recommended strategy through the analysis of the period (5/2008 to 11/2010).

# Deep Dive Analysis 
1. Customer Profile
From the report, customers segment that have a high likelihood of subscribing to a term deposit share the same characteristics:
* Occupation: White-Collar workers have the highest proportion, followed by Skilled/Technical and Blue-Collar.
* Education: Customers with a tertiary education have the best response to the campaign.
* Financial statement: Customers with no debt or only a housing loan are the best prospects.
* Age group: The average age of subscribers is ~42 years old. Retired groups have a small proportion but usually have a high conversion rate.

2. Campaign & Seasonality
- Best month to call:
  * May has the highest subscriptions, but May also has the highest number of contacts. 
  * Calling near the end of the year or in March, September, or October yields a better conversion rate even with fewer total contacts.
- Duration:
  * This metric is a post-call engagement variable that correlates with subscription and is not available before calling, so only use it for operational insights rather than pre-call targeting.
  * Calls that have a duration under 2 minutes typically indicate customers do not want to hear about the marketing campaign. When the interactions are longer, the percentage of acceptance increases to 48.4%

 3. Contract Strategy
- Contact type:
  * Cellular: Has the highest proportion with a conversion rate of ~15%
  * Telephone: Only 5-7% of the conversion rate
- History response:
  * New/Never contacted customers: Account for 63.98% of total subscriptions, the highest proportion of total contacts
  * Re-contacted customers: Contributing 36.02% to the total subscriptions. Notably, if customers had a positive "Success" response in the previous campaign, the possibility of success in this campaign is very high.
 
# Recommendations 
1. Targeting:
   - Prioritize the customer segments when calling: Management -> Retired -> Student.
   - Prioritize customers with no debt and high account balances.
2. Seasonality:
   - May is peak season, but calls should also be made in Q3 and Q4 to capture year-end savings deposit demand. 
3. Optimize contact type:
   - Prioritize cellular over telephone to increase the call acceptance.
   - For the customer whose previous outcome was "Success", provide special attention to this group. 
  
# Dash Board: 
The dashboard can be found at the Power BI link [here](https://app.powerbi.com/view?r=eyJrIjoiNjQ3YTZlMDItNmQ1Yi00OTQwLWIyMmQtMjk3NjkwZDBjMGVkIiwidCI6ImM5MTAzYTUyLWYwMGEtNDBiOC04MTFiLWVkNWJmMjYwOWJjNCJ9&pageName=bfcdbc29f574e618bccf) for further interaction with the report. 
![overview](https://github.com/user-attachments/assets/c835217a-31cb-49d3-aaba-c032ba81eb36)
![insight](https://github.com/user-attachments/assets/2e808c12-d005-414d-b4f2-60b04a64d241)
![strategy](https://github.com/user-attachments/assets/8c22ecb6-3dad-478e-97a0-9b9a70ffebdf)

# Tool: 
- Using Power BI for data handling and visualization.
