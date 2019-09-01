# Michigan Elections Data Sources

## Michigan GIS Open Data

[Link to Michigan GIS Open Data](http://gis-michigan.opendata.arcgis.com/)

### Voting Precincts Shapefiles

* [2018 Voting Precincts](http://gis-michigan.opendata.arcgis.com/datasets/2018-voting-precincts)
  * Due to missing shapefiles for some election years, used 2018 shapefile for all years to preserve consistency
* [2016 Voting Precincts](
http://gis-michigan.opendata.arcgis.com/datasets/2016-voting-precincts)
* [2014 Voting Precincts](
http://gis-michigan.opendata.arcgis.com/datasets/2014-voting-precincts)
* 2008-2012 - no shapefile available

### State House/Senate Shapefiles

* [Michigan State House Districts (v17a)](http://gis-michigan.opendata.arcgis.com/datasets/michigan-state-house-districts-v17a?geometry=-175.605%2C40.447%2C177.715%2C83.83)
  * from Michigan Geographic Framework base map. Uses 2011 Apportionment Plan as enacted by PA 129 of 2011.
* [Michigan State Senate Districts (v17a)](http://gis-michigan.opendata.arcgis.com/datasets/michigan-state-senate-districts-v17a)
  * from Michigan Geographic Framework base map. Uses 2011 Apportionment Plan as enacted by PA 129 of 2011.

### Cities/Townships Shapefiles: Data matching `MCDFIPS` with city/township names

* [Minor Civil Divisions (Cities & Townships) (v17a)](https://gis-michigan.opendata.arcgis.com/datasets/minor-civil-divisions-cities-townships-v17a)
  * The voting precincts shapefile has a *number*, `MCDFIPS`, for each township/city.
  * The election results from step (1) has a *name* for each township/city (e.g. `Southfield`).

### County Shapefiles: Data matching `COUNTYFIPS` with county names

* [Counties (v17a)](https://gis-michigan.opendata.arcgis.com/datasets/counties-v17a)
  * Similar number/name difference

## Election Results

### Michigan Secretary of State

Warning: `County Code` and `City/Town Code` in these files are NOT the same as `countyfips` and `mcdfips` in the shapefiles!

Direct link to precinct-level (and county-level) election results: [https://miboecfr.nictusa.com/cgi-bin/cfr/precinct_srch.cgi](https://miboecfr.nictusa.com/cgi-bin/cfr/precinct_srch.cgi)
* To get to this link, visit [https://www.michigan.gov/sos/0,4670,7-127-1633_8722-486915--,00.html](https://www.michigan.gov/sos/0,4670,7-127-1633_8722-486915--,00.html)
* Then scroll down to "Related Content" and then click on "November General Election Results by Precinct" (the first link under "Related Content")

### Oakland County

Additional election results available at Oakland County Precinct Detail via [Oakland County Clerk/Register of Deeds website](https://www.oakgov.com/clerkrod/elections/Pages/past-election-results.aspx)
* [Governor and Lieutenant Governor - November 6, 2018 General Election](http://results.enr.clarityelections.com/MI/Oakland/91321/222847/en/md_data.html?cid=88&)
* [President and Vice President - November 8, 2016 General Election](http://results.enr.clarityelections.com/MI/Oakland/63990/184040/en/md_data.html?cid=0106&)
* [Governor and Lieutenant Governor - November 4, 2014 General Election](http://results.enr.clarityelections.com/MI/Oakland/54212/149511/en/md_data.html?cid=0106&)
* [President and Vice President - November 6, 2012 General Election](http://results.enr.clarityelections.com/MI/Oakland/43747/114561/en/md_data.html?cid=0106&)
* [Governor and Lieutenant Governor - November 2, 2010 General Election](http://results.enr.clarityelections.com/MI/Oakland/22923/42960/en/md_data.html?cid=0106&)
* [President and Vice President - November 4, 2008 General Election](http://results.enr.clarityelections.com/MI/Oakland/9047/13955/en/summary.html)
  * precinct-level data was not available for 2008
* The Oakland County Clerk/Register of Deeds office offers maps [such as this one](https://results.enr.clarityelections.com/MI/Oakland/91321/222847/en/md.html?cid=88). However, these maps only show a blue-or-red binary color for each precinct. My maps show shades of red and blue, better displaying the true partisanship of each precinct.
