# District Info Project

## About

The District Info Bot is a script that supplies on-demand, relevant district information/context to social media users talking about a U.S. congressional district.

Currently, it runs on the social media platform Reddit using their API. It is monitoring the following political subreddits: `VoteBlue`, `Democrats`, `Conservative`, `Republican`. To avoid spamming, the script only replies in the specific mentioned subreddits. However, due to the nature of the submissions in each subreddit, almost all of the script's replies have been in `VoteBlue`.

Given this use case, districts with missing data were dropped and voteshares (percentages) were rounded to the nearest percent or to one decimal place depending on the field.

## Data Descriptions and Sources

| Field | Description | Source | Comment |
|------|-------------------------------------|-----------------------|-----------------------|
| `state` | US state in which district is located, iso code e.g. `MI` | (default/merge field) |  |
| `dist_no` | District number with no preceding zero and AL* = 1 e.g. `01`| (default/merge field) | * At-large congressional district. In some datasets, these appear as AL and in others as 1 or 01. |
| `dist_name` | District name e.g. `Michigan 11th` | (default) |  |
| `uncontestedhouse18` | Was 2018 US House race uncontested? Binary 0/1 | (created) | Inferred from 100/0 result AND no third-party candidate |
| `uncontestedhouse16` | Was 2016 US House race uncontested? Binary 0/1 | (created) | Inferred from 100/0 result AND no third-party candidate |
| `pvi` | Cook's Partisan Voter Index (PVI) | [The Cook Political Report](https://cookpolitical.com/pvi-0) |  |
| `pres2016` | How district voted for US President in 2016 | [Daily Kos Elections' presidential results by congressional district for 2016, 2012, and 2008](https://docs.google.com/spreadsheets/d/1zLNAuRqPauss00HDz4XbTH2HqsCzMe0pR8QmD1K8jk8/edit#gid=0) | for congressional districts used in 2018 elections |
| `pres2012` | How district voted for US President in 2012 | [Daily Kos Elections' presidential results by congressional district for 2016, 2012, and 2008](https://docs.google.com/spreadsheets/d/1zLNAuRqPauss00HDz4XbTH2HqsCzMe0pR8QmD1K8jk8/edit#gid=0) | for congressional districts used in 2018 elections |
| `incumbent_party` | Party affiliation of the Representative currently occupying the seat | [@unitedstates/ congress-legislators](https://github.com/unitedstates/congress-legislators) | bot now refreshes daily; pulls daily from the source (as of 11/19) |
| `incumbent_name` | Name of the Representative currently occupying the seat | [@unitedstates/ congress-legislators](https://github.com/unitedstates/congress-legislators) | bot now refreshes daily; pulls daily from the source (as of 11/19) |
| `lean` | FiveThirtyEight's Partisan Lean - District | [their GitHub](https://github.com/fivethirtyeight/data/tree/master/partisan-lean) |
| `pretty_dist_code` | Nice district code to display | (created) |
| `house18net` | Margin of victory in 2018 US House elections, e.g. `R+6` means Republican won by 6%, `D+6` means Democrat won by 6% | [U.S. House 1976–2018 from MIT Election Data and Science Lab](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/IG0UN2) - uses 2018 districts | Originally used [2018 U.S. House of Representatives election results (unofficial)](/2018-house-results) before MIT dataset was published on Apr 24, 2019 |
| `house16net` | Margin of victory in 2016 US House elections | [CLEA Lower Chamber Elections Archive](http://www.electiondataarchive.org/clea-lower-chamber-elections-archive.php) - uses 2016 districts | MIT also has these elections; there are several reliable sources for 2016 |
| `538 Trump Score` | FiveThirtyEight's Trump Score | [their GitHub](https://github.com/fivethirtyeight/data/tree/master/congress-trump-score) | pulled dynamically/live (as of 11/19) |

***

## Tools Used

Python - Pandas and Python Reddit API Wrapper (PRAW)
