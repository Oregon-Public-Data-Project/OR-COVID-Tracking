# Oregon COVID Data

Oregon collects some of the best COVID-19 data in the country. Unfortunately, they've chosen not to release the data in a data format. 

ZIP-code level case data is trapped in weekly pdf reports. Hospital capacity data is posted in a Tableau workbook with the option to download disabled. 

To help remedy the solution, I'm posting lots of the data I've collected over the last 6 months, mainly by scraping their html page and pdfs. At some point I'll add documentation, but let me stress this is a volunteer effort. 

## What is posted? 

[County level cases by day](https://github.com/Oregon-Public-Data-Project/OR-COVID-Tracking/tree/main/county) These are cumulative tests and cases. Please note that this data is released as "preliminary" and is often adjusted up or down later. 

[Weekly ZIP code totals](https://github.com/Oregon-Public-Data-Project/OR-COVID-Tracking/tree/main/zips/weekly_data) These are scraped from the weekly reports. OHA only releases this for ZIPs with more than 1,000 residents, and a precise number of cases is only given in ZIP codes where more than 10 cumulative cases are present. These files, by convention, use -1 to denote ZIP codes with 1-9 cases.

[Weekly ZIP code summary files](https://github.com/Oregon-Public-Data-Project/OR-COVID-Tracking/tree/main/zips/analysis) A csv file of ZIP code counts by week. Counts of new cases are only calculated when a specific number is given for both the prior and current week. In other words, this is not calculated if a ZIP code lists 1-9 cases one week and 12 the next, although reasonable minds might conclude there's a range of 3-11 cases. 

[State hospital occupancy](https://github.com/Oregon-Public-Data-Project/OR-COVID-Tracking/tree/main/covid_details) This used to be released daily on OHA's html page, but was moved into a tableau worksheet when hospitalizations began to spike. 

[Weekly PDF reports](https://github.com/Oregon-Public-Data-Project/OR-COVID-Tracking/tree/main/weekly_reports) These are the original (pdf) weekly reports. 

## Update speed

🐢🐢🐢

## General Disclaimer

This is a compilation of free data, curated from the web. If you want accurate data, ask OHA. 