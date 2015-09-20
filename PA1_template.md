# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data


```r
download.file("https://raw.githubusercontent.com/vfoss/RepData_PeerAssessment1/master/activity.csv", 
              "activity.csv", method="curl")

activity <- read.csv("activity.csv", colClasses=c("numeric","Date","numeric"),
                     row.names = NULL, stringsAsFactors = FALSE, header=TRUE)
```

## What is the total number of steps taken per day?

1. Calculate the total number of steps taken per day

```r
allsteps <- tapply(activity$steps, activity$date, sum, na.rm=TRUE)
```

2. Make a histogram of the total number of steps taken each day

```r
hist(allsteps, xlab="Total Number of Steps taken per Day")
```

![](PA1_template_files/figure-html/unnamed-chunk-3-1.png) 

3. Calculate and report the mean and median of the total number of steps taken per day

```r
mean(allsteps)
```

```
## [1] 9354.23
```


```r
median(allsteps)
```

```
## [1] 10395
```

## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
