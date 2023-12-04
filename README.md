# overwatch-2-rank-scraper
Scrapes overwatch.blizzard.com for user ranks, given a username as input. 

## Prerequisites
Make sure the accounts you are trying to connect to are set to **Public**. This can be changed in the Overwatch 2 Game Settings: `Launch Game > Menu > Options > Social > Privacy > Identity > Career Profile Visibility`

### Libraries
- [Requests](https://docs.python-requests.org/en/latest/index.html)
- [NumPy](https://numpy.org/doc/stable/)
- [lxml](https://lxml.de/)
#### Optional
- [pygsheets](https://pygsheets.readthedocs.io/en/stable/)

## The Function
There are a max of 3 possible ranks to be had by any user one for each role. In this loop, we try each XPath by iterating through a counter. The role image src, and we check for the matching role image src, then add the rank image src to a NumPy array called `ranks`. The array is then returned. You can use this output however you'd like.


## The Example
 In the example provided, the array is put into a google sheet. Python connects to a google sheet using the Google Sheets API from Google Cloud, and displays the output on a table. This is just one usecase for this. Documentation on how to use Google Sheets API can be found [here](https://developers.google.com/sheets/api/guides/concepts).
