## HHS Hospital Data

See the [news release](https://www.hhs.gov/about/news/2020/12/07/hhs-publishes-covid-19-hospital-facility-level-data.html).

The actual datasets are [available here](https://healthdata.gov/search/type/dataset?query=covid-19&sort_by=changed&sort_order=DESC). 

This is mostly concerned with [COVID-19 Reported Patient Impact and Hospital Capacity by Facility](https://healthdata.gov/dataset/covid-19-reported-patient-impact-and-hospital-capacity-facility). The summary page is worth reading. In particular note the following variable name conventions. 

### The "ccn" column 

The CCN is the CMS ID but be careful in processing not to chop the leading zeros. 

### Variable name conventions

The list of included variables is quite long


Reported elements include an append of either “\_coverage”, “\_sum”, or “\_avg”.

A "\_coverage” append denotes how many times the facility reported that element during that collection week.
A “\_sum” append denotes the sum of the reports provided for that facility for that element during that collection week.
A “\_avg” append is the average of the reports provided for that facility for that element during that collection week.

Suppression is applied to the file for sums and averages less than four (4). In these cases, the field will be replaced with “-999,999”.

### Collection week

This data is being released on a weekly basis from 7/31 through 11/27. There are about 4800 hospitals reporting weekly. 

### A simplified subset of COVID variables

There are many useful variables. But for a quick summary sometimes its easier to just use a subset. This is a renaming convention I've been using for an abbreviated view. 


  all\_adult\_hospital\_inpatient\_beds\_7\_day\_avg ==> adult\_inpatient\_beds
  
  inpatient\_beds\_used\_7\_day\_avg ==>  inpatient\_beds\_used
  
  total\_adult\_patients\_hospitalized\_confirmed\_and\_suspected\_covid\_7\_day\_avg ==>  covid\_all
  
  total\_adult\_patients\_hospitalized\_confirmed\_covid\_7\_day\_avg ==>  confirmed\_covid
  
  total\_icu\_beds\_7\_day\_avg ==>  tot\_icu\_beds
  
  total\_staffed\_adult\_icu\_beds\_7\_day\_avg ==>  staffed\_icu\_beds
  
  staffed\_adult\_icu\_bed\_occupancy\_7\_day\_avg ==>  icu\_occupancy
  staffed\_icu\_adult\_patients\_confirmed\_and\_suspected\_covid\_7\_day\_avg ==>  all\_covid\_icu
  
  staffed\_icu\_adult\_patients\_confirmed\_covid\_7\_day\_avg ==>  confirmed\_covid\_icu

