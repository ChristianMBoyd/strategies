# Pressing tasks

## Consider what drives dividend reinvestment growth -- periodic diversification or value returned to investors?

A key point to discern is whether reinvested dividends are impactful because they provide automatic diversifictation.  For example, how would an S&P 500 portfolio compare if dividends were reinvested back into the dividend paying stock vs. reinvested back into the broader S&P?  On the flip side, could historical dividend reinvestment performance be matched by randomly selling off small fractions of stock each quarter?  From this latter perspective, dividends in and of themselves may be more or less irrelevant if the same effect can be obtained by systematically pruning company holdings within a given portfolio.


## Consider dollar cost average historical returns vs. comparing initial and final S&P 500 values

One thing I see in the historical CAGR calculations is that there are certain time periods where you cannot recover your losses through time in the market.  For example, investing at the peak before the stock collapse triggering the great depression (~1930) always brings down your portfolio (essentially unchanged even for 80 year investment horizons).

I'm sure it'll involve more work to track the investment over time, but I would want to see the historical returns for a dollar cost averaged investment strategy.  For example, it looks like investment periods over 30 years in the current historical CAGR analysis more or less lock in similar returns.  Does the dollar-cost averaged approach take a substantialy longer time in the market, or does an additional ~10 or so years prevent locked-in losses like those for investments right before the great depression?


## Parse pre-XBRL EDGAR data

Modern EDGAR filing data (post ~2010) has XBRL tags, which automate pulling various GAAP values via a simplified API.  Historical (pre ~2010 or mid-00s) EDGAR filings are more or less raw/html formatted text documents.  There are no XBRL tags, and the formatting/language used does not appear to be identical between companies/periods; however, one could hope the terminology for each line item is severely constrained by GAAP.

Since this historical data goes back to 1994, and contains comparisons to 1993 data, it would significantly extend the data for use in analyses if it were structured similarly to the modern data.  I need to either parse the historical text files myself, build on an existing open-source framework, or utilize a reliable solution to bridge the gap in EDGAR filing data.  If I do this myself, it would be a great open source project to start.

### No existing python parsers found yet

I should broaden my search for non-python systems, libraries, or databases that have parsed the old EDGAR SEC filings (pre_XBRL) into a structured data format.  If nothing comes up in the broadened search, the only way to reliably parse these historical filings may be to create something myself.
