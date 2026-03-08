# Data sources


## shiller_sp500.xls -- Robert Shiller's historical analysis of the S&P 500

This data is discussed in depth on [Shiller's webpage](https://shillerdata.com/) and is available through a downloadable link.  

The xls document can be extracted using the following command (at least as long as this link is supported).

```bash
wget https://img1.wsimg.com/blobby/go/e5e77e0b-59d1-44d9-ab25-4763ac982e53/downloads/2d6fa720-95d6-4953-b869-1948ad39173e/ie_data.xls?ver=1764695321121 \
    -o shiller_sp500.xls
```

The local xls file may be slightly altered due to formatting column names or removing white space that confuses python packages, but otherwise the data is meant to be taken as-is.

### Access date

This data appears to be kept up-to-date within a month or so at the time of accessing.  The data being analyzed was retrieved in late December, so that it includes S&P data from Dec. 1st.


## yfinance

The [yfinance package](https://ranaroussi.github.io/yfinance/) simplifies API access to Yahoo's financial data.  A test of $MSFT provided 40 years of history without any issue.  More features should be explored, and the utility of the alternative data noted here.

### Access date

The $MSFT test data started on 03/13/1986 and ended on 03/03/2026.  It was accessed on 03/03/2026.  It appears that data is updated daily.


## Tiingo

[Tiingo's EOD stock data](https://www.tiingo.com/documentation/end-of-day) is available through an API, using an acces token stored locally.  The stock data seems to more or less conform to the type returned by yfinance, or available in Yahoo's finance data.  A similar test of $MSFT showed the same date ranges from 03/13/1986 through 03/03/2026, with discrepancies on the order of $0.01/day when compared to the yfinance data.

Tiingo offers other APIs, which should be explored and noted here.

### Access date

The $MSFT test data started on 03/13/1986 and ended on 03/03/2026.  It was accessed on 03/06/2026.  It appears that data is updated daily.


## EDGAR

EDGAR's CIK data was mostly downloaded from the web.  Some reference or test filing data is TBD.

### Access date

I downloaded CIK and CIK<->ticker data on 03/08/2026.


## Sources not stored within this directory


### barchart

[barchart](https://www.barchart.com/stocks) is a website providing detailed stock (and corporate) history.  It seems, however, that data access is limited to visual charts on their website, rather than via an API, without paid membership.  A similar test of $MSFT start in November 1987, rather than March of 1986.

#### Access date

I accessed the $MSFT charts on 03/07/2026, and it appears that it's updated frequently as the previous day's trading data was visible.

#### Todo

[The free trial](https://www.barchart.com/get-barchart-premier?ref=histDownload) might be worth exploring for an alternative data source on basic historical data like $MSFT.


### Nasdaq

[Nasdaq](https://www.nasdaq.com/) provides a lot of stock data in chart form.  They appear to also have fine-grained, all-history data on dividend payouts, although _I was immediately blocked_ for accessing this one day.  They seem to block any systematic search, so this may only be a good reference for data that seems unreliable/spotty in other sources.

Curiously, the data appears restricted on Nasdaq's charts.  Selecting "all" only shows price history back to August 1992.  The dividend history, however, appears to cover all of the ticker's history (i.e., it's not limited by the chart range).

#### Access date

As of writing this, I've accessed the Nasdaq site on 03/07/2026.