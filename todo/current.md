# Pressing tasks


## Consider what drives dividend reinvestment growth -- periodic diversification or value returned to investors?

A key point to discern is whether reinvested dividends are impactful because they provide automatic diversifictation.  For example, how would an S&P 500 portfolio compare if dividends were reinvested back into the dividend paying stock vs. reinvested back into the broader S&P?  On the flip side, could historical dividend reinvestment performance be matched by randomly selling off small fractions of stock each quarter?  From this latter perspective, dividends in and of themselves may be more or less irrelevant if the same effect can be obtained by systematically pruning company holdings within a given portfolio.


## Consider dollar cost average historical returns vs. comparing initial and final S&P 500 values

One thing I see in the historical CAGR calculations is that there are certain time periods where you cannot reach historical average returns through time in the market.  For example, investing at the peak before the stock collapse triggering the great depression (~1930) always brings down your portfolio (essentially unchanged even for 80 year investment horizons).

I'm sure it'll involve more work to track the investment over time, but I would want to see the historical returns for a dollar cost averaged investment strategy.  For example, it looks like investment periods over 30 years in the current historical CAGR analysis more or less lock in similar returns.  Does the dollar-cost averaged approach take a substantially longer time in the market, or does an additional ~10 or so years prevent locked-in losses like those for investments right before the great depression?  If nothing else, I imagine this is the more typical investment scenario, vs. the lump-sum analysis I'm currently considering.


## Parse pre-XBRL EDGAR data

Modern EDGAR filing data (post ~2010) has XBRL tags, which automate pulling various GAAP values via a simplified API.  Historical (pre ~2010 or mid-00s) EDGAR filings are more or less raw/html formatted text documents.  There are no XBRL tags, and the formatting/language used does not appear to be identical between companies/periods; however, one could hope the terminology for each line item is severely constrained by GAAP.

Since this historical data goes back to 1994, and contains comparisons to 1993 data, it would significantly extend the data for use in analyses if it were structured similarly to the modern data.  I need to either parse the historical text files myself, build on an existing open-source framework, or utilize a reliable solution to bridge the gap in EDGAR filing data.  If I do this myself, it would be a great open source project to start.

### No existing python parsers found yet

I should broaden my search for non-python systems, libraries, or databases that have parsed the old EDGAR SEC filings (pre_XBRL) into a structured data format.  If nothing comes up in the broadened search, the only way to reliably parse these historical filings may be to create something myself.


## Perform CAGR calculations in real (inflation-adjusted) terms

As I'm reading Shiller's _Irrational Exuberance_, he constantly emphasizes the importance of historical analysis in real terms.  I've personally been slightly skeptical of the accuracy in historical calculations of values w/r/t "real" or inflation-adjusted returns, but this is definitely worth learning more about.


## Look into CPI and historical inflation-adjusted calculations

Beyond the historical Shiller data, it'd be interesting to look into how well inflation metrics like the CPI capture the relative increase or decrease in consumer spending power over time. I'm particularly interested in how housing affordability has been tracked, and whether the relative ratios of various inflation metrics vary over time or have been fixed historically as a reference point.


### Consider finding sufficient data to calculate a custom inflation metric

If historical data is readily available on home prices, consumer goods, etc., it would be interesting to see how custom ratios affect the interpretation of real returns in the Shiller data or other histirocal data.


## Try to better understand stock returns

**Note**: This ties into the analysis of real returns, so this can be prioritized afterward.  

I'm curious as to why stocks seem to perform so well in real terms over time compared to bonds.  For example, why do we expect--alternatively, _do we_ expect--a diversified stock portfolio to do so much better than a bond portfolio.  Is it truly the CAPM explanation of risk, where an equally "risky"--or "volatile"--bond portfolio should have similar returns?  Or is there something else at play, that causes equities are seen as long-term performers vs. bond-like investments.  I would particularly like to answer the following question.  
_If stocks are known to outperform bond-like instruments and more effectively protect against inflation, then why isn't this performance priced-in?_

I suspect this analysis will be a bit of a rabbit hole, and it might make sense for this to go in my notes vs. "strategies," but I would like some technical analysis in addition to reading.  I see a goal of this task to be creating smaller, concrete actions I can take rather than solving everything at once.