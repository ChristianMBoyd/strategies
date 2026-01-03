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