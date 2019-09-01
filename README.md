# Michigan State Legislative District Partisanship Index

## Partisanship index for state house/senate districts for the State of Michigan

|  |  |
|:----:|:----:|
| [![State House District Partisanship Index](https://raw.githubusercontent.com/dcadata/michigan-district-partisanship-index/master/pvi-maps/State%20House%20District%20Partisanship%20Index_table.png)](https://raw.githubusercontent.com/dcadata/michigan-district-partisanship-index/master/pvi-maps/State%20House%20District%20Partisanship%20Index_table.png) | [![State Senate District Partisanship Index](https://raw.githubusercontent.com/dcadata/michigan-district-partisanship-index/master/pvi-maps/State%20Senate%20District%20Partisanship%20Index_table.png)](https://raw.githubusercontent.com/dcadata/michigan-district-partisanship-index/master/pvi-maps/State%20Senate%20District%20Partisanship%20Index_table.png) |
| HD-19 is missing due to missing precincts in shapefile |  |

(Click to view)

### [Summary Tables](https://github.com/dcadata/michigan-district-partisanship-index/tree/master/pvi-tables) | [MI Elections Data Sources](https://github.com/dcadata/michigan-district-partisanship-index/blob/master/michigan-elections-data-sources.md)

## High-Level Process

* translated Cook PVI process from national to state level
* get precinct-level gubernatorial election results for last two elections (2018, 2014) from SOS
* use shapefiles to find out which precincts lie within which state house/senate districts
  * split precincts were apportioned based on area lying in each component district
* roll up election results at the state house/senate district level
* average gubernatorial results across both years
  * at district level
  * statewide
* subtract statewide average from district-wide average, i.e. district-wide minus statewide
* captures difference between district-wide gubernatorial results vs. statewide gubernatorial results, aka partisanship of the district relative to the state as a whole

## Coming Soon

* governor/president/senate/etc. results by state house/senate district
* precinct-level election results maps
* swing precincts maps
* county-level maps for swing counties
* partisanship index calculation for other states (TX? NC?)
* Python code will be posted soon

***

**Tools:** Python - Pandas, Geopandas, Matplotlib

**Contact:** devon@ankar.io
