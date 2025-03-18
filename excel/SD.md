### Standard Deviation and other stats
The normal standard deviation (in absolute terms) is given for 95% coverage as
```
= 1.96 * STDEV(range)
```

However, (following Mark Tudge's efforts) alternative preferred statistics are as follows:
```
sumsq:      = SUMSQ(IF(ISNUMBER(range),range))
count:      = COUNT(IF(ISNUMBER(range),range))
mean:       = AVERAGE(IF(ISNUMBER(range),range))
mad:        = SUM(ABS((IF(ISNUMBER(range),range))))/count
rmse:       = SQRT(sumsq/count)
95% cover:  = 1.96 * rmse
```

Note that `mad` is the [Mean Absolute Deviation](https://en.wikipedia.org/wiki/Median_absolute_deviation)  and `rmse` is the [Root Mean Sqaure deviation or Error](https://en.wikipedia.org/wiki/Root_mean_square_deviation).
