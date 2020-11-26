# Oregon COVID Data

Oregon collects some of the best COVID-19 data in the country. Not all of it is accessible in a traditional data format. 

We're thrilled that OHA posts regionwide hospital capacity data in a Tableau workbook with the option to download enabled. 

ZIP-code level case data is (to our knowledge) only available in weekly pdf reports. There's a reasonable archive of them here in the [weekly reports](https://github.com/Oregon-Public-Data-Project/OR-COVID-Tracking/tree/main/weekly_reports) directory. 


## What is posted? 

[County level cases by day](https://github.com/Oregon-Public-Data-Project/OR-COVID-Tracking/tree/main/county) These are cumulative tests and cases. Please note that this data is released as "preliminary" and is often adjusted up or down later. 

[Weekly ZIP code totals](https://github.com/Oregon-Public-Data-Project/OR-COVID-Tracking/tree/main/zips/weekly_data) These are scraped from the weekly reports. OHA only releases this for ZIPs with more than 1,000 residents, and a precise number of cases is only given in ZIP codes where more than 10 cumulative cases are present. These files, by convention, use -1 to denote ZIP codes with 1-9 cases.

[Weekly ZIP code summary files](https://github.com/Oregon-Public-Data-Project/OR-COVID-Tracking/tree/main/zips/analysis) A csv file of ZIP code counts by week. Counts of new cases are only calculated when a specific number is given for both the prior and current week. In other words, this is not calculated if a ZIP code lists 1-9 cases one week and 12 the next, although reasonable minds might conclude there's a range of 3-11 cases. 

[State hospital occupancy](https://github.com/Oregon-Public-Data-Project/OR-COVID-Tracking/tree/main/covid_details) This used to be released daily on OHA's html page, but was moved into a tableau worksheet when hospitalizations began to spike. 

[Weekly PDF reports](https://github.com/Oregon-Public-Data-Project/OR-COVID-Tracking/tree/main/weekly_reports) These are the original (pdf) weekly reports. 

## Querying the data

The new and cumulative case counts can be queried, and joined to basic demographic data, using this live queryable [datasette](https://covid-5gwuku226a-ue.a.run.app/). (The URL may change in the future). 

Here are some sample queries:

[Cases for a single ZIP.](https://covid-5gwuku226a-ue.a.run.app/COVID_ZIPs/Cases+for+a+single+ZIP+by+week)
    
[New case rate per 10,000 residents for Nov. 25 weekly report](https://covid-5gwuku226a-ue.a.run.app/COVID_ZIPs/New+case+rate+per+10%2C000+residents+for+Nov.+25+weekly+report)
    
[Cumulative case rate per 10,000 residents for Nov. 25 weekly report](https://covid-5gwuku226a-ue.a.run.app/COVID_ZIPs/Cumulative+case+rate+per+10%2C000+residents+for+Nov.+25+weekly+report)

Using the powerful vega plugin, it's relatively straightforward to visualize simple relationships. For instance, here's a [plot of cases for a given ZIP code](https://covid-5gwuku226a-ue.a.run.app/COVID_ZIPs/Cases+for+a+single+ZIP+by+week#g.mark=bar&g.x_column=date&g.x_type=ordinal&g.y_column=count&g.y_type=quantitative). 

And here's an [X-Y scatter plotting per-10,000 case rate vs median household income](https://covid-5gwuku226a-ue.a.run.app/COVID_ZIPs/Cumulative+case+rate+per+10%2C000+residents+for+Nov.+18+weekly+report#g.mark=circle&g.x_column=medhinc_cy&g.x_type=quantitative&g.y_column=count_per_10k&g.y_type=quantitative). 

## Update speed

🐢🐢🐢

## General Disclaimer

This is a compilation of free data, curated from the web. If you want accurate data, ask OHA. 


## Maintenance

This is a project from [@jsfenfen](https://github.com/jsfenfen/).
