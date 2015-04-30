## Getting data

Components and sites have subresources to query for timeseries data. These timeseries data calls return interval, rather than accumulated values for the granularity chosen. For example, if you ask for energy from 2013-01-01T00:00:00 to 2014-01-01T00:00:00 at yearly granularity, you would receive the energy measured only during the calendar year of 2013.

Timestamps in responses of data calls represent the beginning of that time interval. This is also known as a "leading" timestamp. The interval includes data up until just before the following timestamp in the data response. Using the same yearly example as above, the timestamp for data received would be 2013-01-01T00:00:00 and would include all energy where the timestamp is >= 2013-01-01T00:00:00 and < 2014-01-01T00:00:00.

For all data calls, the time period allowed depends upon the granularity chosen.

* 5min: < 7 days
* 15min: < 7 days
* hourly: < 31 days
* daily: < 1 year
* monthly: no limitations
* yearly: no limitations