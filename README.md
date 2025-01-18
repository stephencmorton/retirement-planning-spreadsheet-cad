# Retirement Planning and Forecasting Spreadsheet for Canadians

This is a continuation of Steven Brown's "Retirement Planning and Forecasting Spreadsheet for Canadians v2.7"

In 2013, Steven Brown released his [Retirement Planning and Forecasting Spreadsheet for Canadians](https://pabroon.blogspot.com/2015/05/retirement-planning-and-forecasting-20.html) and it was updated until version 2.7 in 2017. It had not been updated since then. I'm putting it online so that I can update it and hopefully get others to contribute to it too.

## What the spreadsheet does
- It allows you to plan for you retirement, starting at any time in your life.
- Based on your income and expenses, the spreadsheet calclates taxes and the difference is savings which are placed into your accounts.  
- The spreadsheet calculates the growth in your various savings accounts (RRSP, LIRA, TFSA and non-tax free account) 
- You set your expenses (income required) during retirement and the spreadsheet withdraws the amounts from the accounts to give you the after tax income you desired.  
- It accounts for a DB pension you may have, CPP and OAS payments and does tax calculations for all the provinces.  
- The way the spreadsheet is structured, it allows you to easily try many different scenarios such as different retirement ages, different expenses amounts, and which account to withdraw money from first.  
- The results of the spreadsheet is a detailed income forecast and from what source, or account, the income is sourced.  The spreadsheet also shows the balance in your savings, investment and retirement accounts vs time.  


## Instructions			

- Only enter data into yellow cells. Do not change any other cells.  		

- When you open the spreadsheet make sure to enable macros. There is a function macro and also a macro to calculate the tax rates iteratively.		
- This spreadsheet can handle the retirement planning for a couple.		
- All the inputs and a summary of the results are shown on the "Inputs_Summary" sheet. 		
- Enter the particulars for one person under the "Person 1" column and a second person (spouse) under the "Person 2" column.		
- If you want to use the function where the estate of Person1 passes to Person2 then Person1 should pre-decease Person2.		
- To set the Person2 to inactive set the on/off switch next to the start year to Off.  		
- After you change any inputs, click the "Iterate Tax Rates" button on the Inputs_Summary sheet.  This process iterates to find the required before tax income for a given after tax income.  		
- In the cells to the right of the yellow input cells there is a description of each input.		
- On the "Inputs_Summary" sheet it gives a summary of results at the top, including whether you can meet your retirement income goals and how much money you have left.		
- Also on the "Input_Summary" sheet, charts of income and account balances are shown for Person 1 and either Person 2 or Both people (summed together).		
- The charts at the bottom of the "Inputs_Summary" sheet can be changed from Person 2 to Both by changing the yellow cell just above these charts.  		
- On the Person1 and Person2 sheets you can enter some values annually in the "Annual Inputs" section. A description of each of these inputs is contained in the first row above each column. Note these are in current $.		

## How the spreadsheet works			

- During the employment phase:		
   - Employment income is specified and can be grown at a different rate other than CPI.	
   - Expenses during employment is specified, taxes are calculated and the remainder (Income - Taxes - Expenses) is saved. 	
   - Income tax due on interest and dividend income in the Investment account is also calculated as part of tax payable.	
   - Income tax is calculated based on your province of residence.	
   - The amount saved is put to your RRSP, TFSA and Investment accounts depending on room and settings you specify..	
   - DC pension contribution percentage is specified and put into a LIRA account. 	
   - Net Income after tax and Net Income after tax and savings are shown on the plots.	
- During the retirement phase:		
   - The amount of DB pension, CPP and OAS is calculated first.	
   - OAS clawback is calculated based on previous years income.	
   - Expenses (required income) is specified and the gross income is estimated from an initial guess of effective tax rate.	
   - Any amount above DB, CPP and OAS that is required to meet expenses is withdrawn from the savings accounts (RRSP, TFSA, LIRA and Investment).	
   - Weightings for withdrawal from the 4 accounts can be changed to prefer one account over the other.	
   - RRSP/RRIF and LIRA/LIF withdrawals are calculated first.The mandated minimum and maximum withdrawals are imposed. 	
   - If the minimum wthdrawals result in more income than expenses then the extra will go to TFSA or Investment accounts.	
   - If additional income is still required, then withdrawals from the Investment account and then the TFSA account will be made. 	
   - If you have chosen to fund TFSA after retirement, then additional money will be withdrawn from the Investment account to put to the TFSA account.	
   - Income tax calculation is done next.The "Iterate Tax Rate" macro button copies this calculated tax rate back to the initial guess of the effective tax rate.The macro does this iteration at least 5 times.	
   - You may pass the estate from Person1 to Person2, including RRSP and TFSA amounts as a survivor.	
- Sheets		
   - Inputs_Summary: All inputs and basic summary plots are here.  	
   - Person1 and Person2 sheets is where the calculation is performed.  These sheets are almost identical.	
   - 	For the calculation columns there is a description on the first row of what the column is and how it is calculated.
   - The Both sheet sums up the results for the two individuals.  	
   - Charts	
   - 	The P1_Inc chart shows the income for Person1 as a stacked line for all possible sources of income.The Net income, after income taxes and money to savings, is shown as a green line.
   - 	The P1_Accts shows the balance of the 4 types of savings accounts as a stacked line chart.
   - 	The Both charts are for Person1 and Person2 summed together.

- Only enter data into yellow cells. Do not change any other cells.  		
- Don't touch cells that have no colour, these are calculated.		
- These cells are ones that the developer needs to change when new tax tables are available for a new year.  		
- These cells in sheets Person 1 and Person 2 are the inputs that come from the "Inputs_Summary" sheet.		



## Key Features			

- The summary section and the plots can be shown in actual $ or in current $.		
- You can specify any of the 13 provinces or territories for calculating income tax.		
- From Income, DB pension plan Pension Amount and and DC pension plan contributions, calculates RRSP room each year.		
- RRSP limits, Tax brackets and Non refundable tax credit amounts are indexed to CPI.		
- TFSA limits are no longer indexed to CPI.		
- The spreadsheet automatically puts savings into the RRSP, TFSA and investment accounts.		
- You can specify a % of RRSP contributions that go to your Spouse.		
- Saving into TFSA and RRSP accounts can be turned off (if you want to determine if these are actually useful)		
- DC pension contributions are put into the LIRA account.  		
- For the Investment account:		
   - You can specify what percentage of the growth in the account is capital gains and what percentage is dividend income, the remainder is interest income.	
   - Handles the tax treatment differences for interest income, capital gains and dividends.	
   - Income tax payable on income from the account is payable from employment income during employment and paid from withdrawals from the account when retired.	
- You can convert a portion of a LIRA to RRSP upon retirement.  Legislation allows 50% in Alberta if at the same time the LIRA is also converted to a LIF. 		
- You can convert a LIRA to a LIF at any time between 50 and 71.The minimum and maximum LIF withdrawal amounts are imposed by the spreadsheet.		
- You can convert an RRSP to an RRIF any time before 71.The minimum withdrawals rates are imposed.		
- Withdrawals from each of the 4 different accounts can be changed by changing the account withdrawal weightings.Normally these are set to 1, but if you want the RRSP withdrawn first set the RRSP weighting higher (maybe 2 or 10).		
- You can continue to contribute to a TFSA (from a taxable savings account) after retirement.		
- Can specify DB pension amounts, how it is indexed and clawed back for CPP.		
- Can split DB pension with spouse and specify survivor benefit amount.		
- Accurate income tax model.		
- On death of Person1, the funds can be tranfered to Person 2 assuming as a beneficiary.  Investments are sold at market, income tax paid and funds tranfered to Person2.  RRSP, LIRA and TFSA accounts are transferred.  		
- Calculates estate values.   Investments are sold at market, income tax paid.  RRSP and LIRA are cashed.  TFSA is non-taxable.  Estate value is stated after tax paid.  		
- Can specify CPP survivor benefit amount.  		

## Compromises			
- OAS clawback based on previous years income.		
- Same investment growth % for all accounts.		
- Pension tax credit of between $1000 to $2000 not included.		
- Tax calculation does not include special provincial tax amounts (ON health premium, NT/NU refundable cost of living)		
- Tax calculation does not include Federal and YT employment amount for NRTC		
- Used the Federal clawback schedule to determine clawback for provincial Age Amount (the difference is quite small).		
