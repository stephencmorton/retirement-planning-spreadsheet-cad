# ChangeLog

## v2p7p1

*Changes made by Brad Forden, and are under discussion with the author for contribution to everyone.*

**Feb 2018**

### Enhancements

- Add historical return datasets and support for using historical return investment returns. A description and detail instructions to change it are provided at the bottom of the Inputs_Summary sheet.
- Add expenses column to Income Chart Data, as a solid color red. Strategically placed the order of the data series to only show when there is an shortfall or excess of income.
- Link inflation values together by default. Can always override.
- CPP survivor benefit can be a formula, with an optional override.
- Avoid mistake with the Growth of Expenses % values. Improve names using similar wording as DB index *before* or *after* retirement, and bold formated words `relative to inflation` in the description.
- Change all (5) income charts data series order. Income is moved to the bottom, to avoid hiding other incomes.
- Change all (5) income charts data series order. OAS is moved below DB and CPP to more clearly represent integration with DB.
- Remove markers from all (5) income charts, Net-Svgs data series.
- Format acct balances with $ without decimals, and any $ inputs with commas to minimize data entry mistakes.
- Improve the additional widow expenses description on Inputs_Summary sheet and Person2 Additional Widow Expenses column.
- Correct description of Person1 DB Survivor Spouse column.
- Improve clarity of Expenses, before and after retirement, description. Replaced word "requirements" with "expenses".
- Improved CPP input description to mention this is the unadjusted, or default, payment at age 65.
- Add data validation for variable that controls Age or Year on chart X-axises.
- Improved the X-axises column title, and the explicit title on all 10 charts.
- Minor fix to move cell AT inside CHOOSE formula, for consistency.

### Bug Fixes

- Fix DB Pension clawback NOT to include Survivor CPP Benefit. (Confirmed with Fed Govn Pension Centre.)

---

## v2p7

**Feb 2017**

### Enhancements

- Updated for 2017 Tax rates.

---

## v2p6

**Dec 2016**

### Enhancements

- Updated the OAS comments and functionality. With federal budget in March 2016, normal date for taking OAS is fixed at 65.
- Spreadsheet will now calculate the increase in OAS benefits if you defer starting OAS after 65, up to the latest of 70.
- In the "Top up to Tax Bracket" experimental functionality, have updated the tax brackets to include provincial ones. Selection is now done by drop-down.

---

## v2p5

**Nov 2016**

### Enhancements

- In Annual Inputs added the column to input "Non-eligible Canadian Dividends" to allow input of income from a Canadian controlled private corporation.
- Removed the columns to input additional taxable benefit, federal and provincial tax credits (since the non-eligible dividends can now be input directly).
- Made clawback of CPP from a DB benefit able to be a fraction. This allows you to better model a DB plan of CPP clawback if you have worked at the company with the DB for only part of your career.
- CPP Benefit amount is now automatically discounted or increased if you start taking CPP at an age before or after 65.
- CPP and EI payroll deduction is now estimated to better calculate a net income.
- LIF maximum withdrawal tables have been updated for 2016 value.
- LIF maximum withdrawal is now dependent onwhether the LIF is federally or provincially governed. This changes the maximum withdrawal percentage.
- Tax rate iteration was optimized to make the convergence faster.
- You may now plot Age on the x-axis of plots as an option. Year is still also available. (Look under "Other Settings")

### Bug Fixes

- Fixed the formula that calculates "Total income less expenses in "Annual Inputs""

---

## v2p4

**April 2016**

### Enhancements

- Updated for all 2016 Tax rates (Previous version had just the new federal and Alberta rates)
- Added the feature to fund TFSA contributions during retirement from RRSP withdrawals

---

## v2p3

**Feb 2016**

### Enhancements

- TFSA limit for 2016 is set to $5500 and is inflated at the input inflation rate and rounded to $500.
- Added a message if either person has an income shortfall in retirement.
- Removed ability to reduce future TFSA limits by using a multiplier.
- Added a report of total tax lifetime income tax paid on the Inputs_Summary sheet. Select this by changing value in dropdown box in cell N7.

### Bug Fixes

- Included the federal tax abatement for Quebec. This was not included previously.
- Changed how the tax rate iteration works to remove a bug when expenses are 0 for one Person.

---

## v2p2

**Dec 2015**

### Enhancements

- Updated tables for Canada and Alberta new tax rates (approximate)
- Increased Ontario tax rates to account for Surtax.
- Increased PEI tax rates to account for Surtax.

### Bug Fixes

- Allow the OAS start age to range from 65 to 72
- Now claw back the Age Amount NRTC based on Net Income (Same as Taxable Income in this model).

---

## v2p1

**Aug 2015**

### Enhancements

- Put 2016 Alberta tax rates into province called Other1
- Added feature to turn off RRSP withdrawals until the RRIF conversion date.
- Added feature to increase RRSP withdrawals so that net income is equal to the top of a specified federal tax bracket.
- Added ability to reduce future TFSA limits by using a multiplier, so you can determine the impact of future TFSA limit reductions.

---

## v2p0

**May 2015**

### Enhancements

- Instead of specifying a % of income saved during employment phase, you now specify your expenses during this phase and the remaining money after deducting taxes and expenses is saved.
  - This allows a better way to do comparison tests of differing investing strategies.
  - In the old way the percentage saved was on a pre-tax basis, so if you changed how much you saved into RRSP from one case to another the amount of after tax available for expenses would change.
  - Better to fix expenses and change the amount of savings if the tax payable changes.
  - This also allows the simplifying of paying of Taxable account taxable income. Taxes due on investment income was payable from contributions to the taxable account.
  - Now this is handled directly in the income tax section and reduces available savings.
- The mortgage payment feature has been removed.
  - If you have expenses that change over time or will only exist fr a few years, then enter them on the Person1 or Person2 sheets in the "Additional Expenses" column.
- The logic to fund RRSP and TFSA contributions from any other Savings has been revamped to work better with the other changes in this version.

### Bug Fixes

- Net Income calculation had effectively subtracted RPP contributions twice. This has been fixed.

