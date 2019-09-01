# Michigan State Legislative District Partisanship Index

Calculate partisanship index for state legislative districts (state house/senate) for the State of Michigan

|  |  |
|:----:|:----:|
| [![State House District Partisanship Index](https://raw.githubusercontent.com/dcadata/michigan-district-partisanship-index/master/pvi-maps/State%20House%20District%20Partisanship%20Index_table.png)](https://raw.githubusercontent.com/dcadata/michigan-district-partisanship-index/master/pvi-maps/State%20House%20District%20Partisanship%20Index_table.png) | [![State Senate District Partisanship Index](https://raw.githubusercontent.com/dcadata/michigan-district-partisanship-index/master/pvi-maps/State%20Senate%20District%20Partisanship%20Index_table.png)](https://raw.githubusercontent.com/dcadata/michigan-district-partisanship-index/master/pvi-maps/State%20Senate%20District%20Partisanship%20Index_table.png) |

### [Data Summary](https://github.com/dcadata/michigan-district-partisanship-index/tree/master/pvi-tables)

### [Sources](https://github.com/dcadata/michigan-district-partisanship-index/blob/master/michigan-elections-data-sources.md)

### High-Level Process

* translated Cook PVI process for the state level
* get gubernatorial election results for last two elections (2018, 2014) at precinct level
* use shapefiles to find out which precincts lie within which state house/senate districts
  * split precincts were apportioned based on area lying in each component district
* roll up election results at the state house/senate district level
* average gubernatorial results across both years
  * at district level
  * statewide
* subtract statewide average from district-wide average, i.e. district-wide minus statewide
* captures difference between district-wide gubernatorial results vs. statewide gubernatorial results, aka partisanship of the district relative to the state as a whole

### Coming Soon

* governor/president/senate/etc. results by state house/senate district
* precinct-level election results maps
* swing precincts maps
* county-level maps for swing counties
* Python code will be posted soon
