# Michigan State House/Senate District Partisanship Index

***Calculating Cook-PVI-style partisanship index for each State House and State Senate District in the state of Michigan***

|  |  |
|:----:|:----:|
| [![State House District Partisanship Index](https://raw.githubusercontent.com/dcadata/michigan-district-partisanship-index/master/pvi-maps/State%20House%20District%20Partisanship%20Index_table.png)](https://raw.githubusercontent.com/dcadata/michigan-district-partisanship-index/master/pvi-maps/State%20House%20District%20Partisanship%20Index_table.png) | [![State Senate District Partisanship Index](https://raw.githubusercontent.com/dcadata/michigan-district-partisanship-index/master/pvi-maps/State%20Senate%20District%20Partisanship%20Index_table.png)](https://raw.githubusercontent.com/dcadata/michigan-district-partisanship-index/master/pvi-maps/State%20Senate%20District%20Partisanship%20Index_table.png) |
| HD-19 is missing due to missing precincts in shapefile |  |

(Click to view)

### [PVI Summary Tables](https://github.com/dcadata/michigan-district-partisanship-index/tree/master/pvi-tables)

***

### See also: [Gubernatorial Elections by State House/Senate Districts](gubernatorial-elections.md)

### Summary Tables: [Governor](https://github.com/dcadata/michigan-district-partisanship-index/tree/master/governor-tables), [State Legislature (both chambers)](https://github.com/dcadata/michigan-district-partisanship-index/tree/master/state-lege-tables), [President](https://github.com/dcadata/michigan-district-partisanship-index/tree/master/president-tables)

***

## [MI Elections Data Sources](https://github.com/dcadata/michigan-district-partisanship-index/blob/master/michigan-elections-data-sources.md)

***

## High-Level Process

(translated Cook PVI process from national to state level)

* get precinct-level gubernatorial election results for last two elections (2018, 2014) from SOS
* use shapefiles to find out which precincts lie within which state house/senate districts
  * split precincts were apportioned based on area lying within each component district
* roll up (sum) election results by state house/senate district (group by)
* average gubernatorial results across both years (unweighted average, i.e. 50/50 weight)
  * district-wide (at district level)
  * statewide
* subtract statewide average from district-wide average, i.e. district-wide minus statewide
* this captures the difference between district-wide gubernatorial results vs. statewide gubernatorial results, aka partisanship of the district relative to the state as a whole

## Coming Soon

* ~~governor/~~ president/senate/etc. results by state house/senate district
* precinct-level election results maps
* swing precincts maps
* county-level maps for "key" counties
* partisanship index calculation for other states (TX? NC?)
* Python code will be posted soon

***

**Tools:** Python - Pandas, Geopandas, Matplotlib

**Contact:** [devon@ankar.io](devon@ankar.io)
