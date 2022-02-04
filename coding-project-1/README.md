# Coding Project #1
Pull CPU Utilization data from a sample Circonus account (via our API) and use it to render a sample graph using the Highcharts library. The sample graph should be styled like the provided mockup and should have simple date range selectors in the upper right that change the view to show the most recent 1 hour/2 hours/6 hours/1 day of data available. You will be provided with an account ID & API token for the associated Circonus account, and the other needed resources are available for free (Highcharts is available to use for free via their CDN.)

The General API docs provide general details about accessing the Circonus API, such as authentication procedures, and the Data Fetch API docs provide details about the particular data "/fetch" endpoint you will need to use to retrieve multiple streams of data simultaneously for the graph.

## Resources
* [Mockup](coding-project-1-mockup.png)
* Styles: 
```
Page Background Color: #edf0f1
Chart Title: 16px Open Sans Semibold #353f43
Chart Background Color: #ffffff
Chart Axis Labels: 12px Open Sans Regular #62757c
Chart Tooltips Text: 12px Open Sans Regular #4b5a5f
Chart Tooltips Background Color: #ffffff
Chart Tooltips Border: 1px solid #d0d7da
Chart Horizontal Grid Lines: 1px solid #d0d7da
Chart Series Line Colors: #217dc3, #ef7820, #7bba52, #6651a4
Chart Series Line Width: 2px
Date Selector Text: 14px Open Sans Semibold #62757c
Date Selector Border: 1px solid #62757c
Date Selector Selected Background Color: #62757c
Date Selector Selected Text Color: #ffffff
```
* [Highcharts docs](https://www.highcharts.com/docs/index)
* [Open Sans font](https://fonts.google.com/specimen/Open+Sans)
* [Circonus General API docs](https://docs.circonus.com/circonus/api/)
* [Circonus Data Fetch API docs](https://docs.circonus.com/irondb/api/data-retrieval/#retrieving-and-transforming-data)

When searching for metrics, use the following:
* Metrics search string: 'and(__name:b"Q1BVIHV0aWxpemF0aW9u")'
* Account ID & API Token will be provided once you are ready to begin
* Create your own app name (it's only for internal reference)

We recently removed CORS support from our public API, so until it's added back in, you will need to either pull the data using a non-browser method (e.g. via calling cURL through PHP), or use a browser add-on to simulate CORS headers:
* https://addons.mozilla.org/en-US/firefox/addon/access-control-allow-origin/
* https://chrome.google.com/webstore/detail/allow-cors-access-control/lhobafahddgcelffkeicbaginigeejlf
