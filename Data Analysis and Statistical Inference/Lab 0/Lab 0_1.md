#<!-- rmarkdown v1 -->
---
title: "Data Analysis and Statistical Inference - Lab 0"
author: "Baskaran Viswanathan"
date: "September 24, 2015"
output: html_document
---




```r
source("http://www.openintro.org/stat/data/present.R")

# To look at the data

present
```

```
##    year    boys   girls
## 1  1940 1211684 1148715
## 2  1941 1289734 1223693
## 3  1942 1444365 1364631
## 4  1943 1508959 1427901
## 5  1944 1435301 1359499
## 6  1945 1404587 1330869
## 7  1946 1691220 1597452
## 8  1947 1899876 1800064
## 9  1948 1813852 1721216
## 10 1949 1826352 1733177
## 11 1950 1823555 1730594
## 12 1951 1923020 1827830
## 13 1952 1971262 1875724
## 14 1953 2001798 1900322
## 15 1954 2059068 1958294
## 16 1955 2073719 1973576
## 17 1956 2133588 2029502
## 18 1957 2179960 2074824
## 19 1958 2152546 2051266
## 20 1959 2173638 2071158
## 21 1960 2179708 2078142
## 22 1961 2186274 2082052
## 23 1962 2132466 2034896
## 24 1963 2101632 1996388
## 25 1964 2060162 1967328
## 26 1965 1927054 1833304
## 27 1966 1845862 1760412
## 28 1967 1803388 1717571
## 29 1968 1796326 1705238
## 30 1969 1846572 1753634
## 31 1970 1915378 1816008
## 32 1971 1822910 1733060
## 33 1972 1669927 1588484
## 34 1973 1608326 1528639
## 35 1974 1622114 1537844
## 36 1975 1613135 1531063
## 37 1976 1624436 1543352
## 38 1977 1705916 1620716
## 39 1978 1709394 1623885
## 40 1979 1791267 1703131
## 41 1980 1852616 1759642
## 42 1981 1860272 1768966
## 43 1982 1885676 1794861
## 44 1983 1865553 1773380
## 45 1984 1879490 1789651
## 46 1985 1927983 1832578
## 47 1986 1924868 1831679
## 48 1987 1951153 1858241
## 49 1988 2002424 1907086
## 50 1989 2069490 1971468
## 51 1990 2129495 2028717
## 52 1991 2101518 2009389
## 53 1992 2082097 1982917
## 54 1993 2048861 1951379
## 55 1994 2022589 1930178
## 56 1995 1996355 1903234
## 57 1996 1990480 1901014
## 58 1997 1985596 1895298
## 59 1998 2016205 1925348
## 60 1999 2026854 1932563
## 61 2000 2076969 1981845
## 62 2001 2057922 1968011
## 63 2002 2057979 1963747
```

```r
# To print out the data

print(present)
```

```
##    year    boys   girls
## 1  1940 1211684 1148715
## 2  1941 1289734 1223693
## 3  1942 1444365 1364631
## 4  1943 1508959 1427901
## 5  1944 1435301 1359499
## 6  1945 1404587 1330869
## 7  1946 1691220 1597452
## 8  1947 1899876 1800064
## 9  1948 1813852 1721216
## 10 1949 1826352 1733177
## 11 1950 1823555 1730594
## 12 1951 1923020 1827830
## 13 1952 1971262 1875724
## 14 1953 2001798 1900322
## 15 1954 2059068 1958294
## 16 1955 2073719 1973576
## 17 1956 2133588 2029502
## 18 1957 2179960 2074824
## 19 1958 2152546 2051266
## 20 1959 2173638 2071158
## 21 1960 2179708 2078142
## 22 1961 2186274 2082052
## 23 1962 2132466 2034896
## 24 1963 2101632 1996388
## 25 1964 2060162 1967328
## 26 1965 1927054 1833304
## 27 1966 1845862 1760412
## 28 1967 1803388 1717571
## 29 1968 1796326 1705238
## 30 1969 1846572 1753634
## 31 1970 1915378 1816008
## 32 1971 1822910 1733060
## 33 1972 1669927 1588484
## 34 1973 1608326 1528639
## 35 1974 1622114 1537844
## 36 1975 1613135 1531063
## 37 1976 1624436 1543352
## 38 1977 1705916 1620716
## 39 1978 1709394 1623885
## 40 1979 1791267 1703131
## 41 1980 1852616 1759642
## 42 1981 1860272 1768966
## 43 1982 1885676 1794861
## 44 1983 1865553 1773380
## 45 1984 1879490 1789651
## 46 1985 1927983 1832578
## 47 1986 1924868 1831679
## 48 1987 1951153 1858241
## 49 1988 2002424 1907086
## 50 1989 2069490 1971468
## 51 1990 2129495 2028717
## 52 1991 2101518 2009389
## 53 1992 2082097 1982917
## 54 1993 2048861 1951379
## 55 1994 2022589 1930178
## 56 1995 1996355 1903234
## 57 1996 1990480 1901014
## 58 1997 1985596 1895298
## 59 1998 2016205 1925348
## 60 1999 2026854 1932563
## 61 2000 2076969 1981845
## 62 2001 2057922 1968011
## 63 2002 2057979 1963747
```

```r
# dimensions of this data frame

dim(present)
```

```
## [1] 63  3
```

```r
# The names of columns

names(present)
```

```
## [1] "year"  "boys"  "girls"
```

```r
# This will print your data set in the console:

head(present)
```

```
##   year    boys   girls
## 1 1940 1211684 1148715
## 2 1941 1289734 1223693
## 3 1942 1444365 1364631
## 4 1943 1508959 1427901
## 5 1944 1435301 1359499
## 6 1945 1404587 1330869
```

```r
# To access the data in a single column of a data frame separately

present$boys
```

```
##  [1] 1211684 1289734 1444365 1508959 1435301 1404587 1691220 1899876
##  [9] 1813852 1826352 1823555 1923020 1971262 2001798 2059068 2073719
## [17] 2133588 2179960 2152546 2173638 2179708 2186274 2132466 2101632
## [25] 2060162 1927054 1845862 1803388 1796326 1846572 1915378 1822910
## [33] 1669927 1608326 1622114 1613135 1624436 1705916 1709394 1791267
## [41] 1852616 1860272 1885676 1865553 1879490 1927983 1924868 1951153
## [49] 2002424 2069490 2129495 2101518 2082097 2048861 2022589 1996355
## [57] 1990480 1985596 2016205 2026854 2076969 2057922 2057979
```

#Question 1

How many variables are included in this data set?


```r
names(present)
```

```
## [1] "year"  "boys"  "girls"
```

3

#Question 2

What command would you use to view just the counts of girls born?


```r
present$girls
```

```
##  [1] 1148715 1223693 1364631 1427901 1359499 1330869 1597452 1800064
##  [9] 1721216 1733177 1730594 1827830 1875724 1900322 1958294 1973576
## [17] 2029502 2074824 2051266 2071158 2078142 2082052 2034896 1996388
## [25] 1967328 1833304 1760412 1717571 1705238 1753634 1816008 1733060
## [33] 1588484 1528639 1537844 1531063 1543352 1620716 1623885 1703131
## [41] 1759642 1768966 1794861 1773380 1789651 1832578 1831679 1858241
## [49] 1907086 1971468 2028717 2009389 1982917 1951379 1930178 1903234
## [57] 1901014 1895298 1925348 1932563 1981845 1968011 1963747
```

#Question 3

Is there an apparent trend in the number of girls born over the years? How would you describe it?


```r
# Plot girls born per year against boys plot(x,y) is the form

plot(present$year, present$girls)
```

![plot of chunk unnamed-chunk-4](figure/unnamed-chunk-4-1.png) 

```r
# Now add a line
plot(present$year, present$girls, type = "line")
```

```
## Warning in plot.xy(xy, type, ...): plot type 'line' will be truncated to
## first character
```

![plot of chunk unnamed-chunk-4](figure/unnamed-chunk-4-2.png) 

Answer 

There is initially an increase in the number of girls born, which peaks around 1960. After 1960 there is a decrease in the number of girls born, but the number begins to increase again in the early 1970s. Overall the trend is an increase in the number of girls born in the US since the 1940s.

#Question 4

In what year did we see the most total number of births in the U.S.? Hint: You can refer to the help files or the R reference card (http://cran.r-project.org/doc/contrib/ Short-refcard.pdf) to find helpful commands.


```r
present$totals = present$girls + present$boys
sort.int(present$totals, index.return = TRUE)
```

```
## $x
##  [1] 2360399 2513427 2735456 2794800 2808996 2936860 3136965 3144198
##  [9] 3159958 3167788 3258411 3288672 3326632 3333279 3494398 3501564
## [17] 3520959 3535068 3554149 3555970 3559529 3600206 3606274 3612258
## [25] 3629238 3638933 3669141 3680537 3699940 3731386 3750850 3756547
## [33] 3760358 3760561 3809394 3846986 3880894 3891494 3899589 3902120
## [41] 3909510 3941553 3952767 3959417 4000240 4017362 4021726 4025933
## [49] 4027490 4040958 4047295 4058814 4065014 4098020 4110907 4158212
## [57] 4163090 4167362 4203812 4244796 4254784 4257850 4268326
## 
## $ix
##  [1]  1  2  6  5  3  4 34 36 35 37 33  7 38 39 40 29 28  9 11 32 10 30 27
## [24] 41 42 44 45 43  8 31 12 47 26 46 48 13 58 57 56 14 49 59 55 60 54 15
## [47] 63 62 25 50 16 61 53 24 52 51 17 23 19 20 18 21 22
```

```r
present$year[22]
```

```
## [1] 1961
```

1961

#Question 5

Now, make a plot of the proportion of boys over time, and based on the plot determine if the following statement is true or false: The proportion of boys born in the US has decreased over time.


```r
present$boys > present$girls
```

```
##  [1] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
## [15] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
## [29] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
## [43] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
## [57] TRUE TRUE TRUE TRUE TRUE TRUE TRUE
```

Answer = TRUE

#Question 6

Which of the following is true?

Answer = Every year there are more boys born than girls.

#Question 7

Make a plot that displays the boy-to-girl ratio for every year in the data set. What do you see?


```r
#Now get the total births by adding

present$babies <- present$boys + present$girls

head(present$babies)
```

```
## [1] 2360399 2513427 2808996 2936860 2794800 2735456
```

```r
# Using that newly created variable as the denominator, calculate the
# proportoin of boys born in a give year

present$proportionBoys <- present$boys/present$babies

head(present$proportionBoys)
```

```
## [1] 0.5133386 0.5131376 0.5141926 0.5138001 0.5135613 0.5134745
```

```r
plot(present$year, present$proportionBoys)
```

![plot of chunk unnamed-chunk-7](figure/unnamed-chunk-7-1.png) 

```r
# In what years to boys outnumber girls?

present$boysGreater <- present$boys > present$girls

head(present$boysGreater)
```

```
## [1] TRUE TRUE TRUE TRUE TRUE TRUE
```

```r
# Check to make sure all the variables are in order with the head() command.

head(present$babies)
```

```
## [1] 2360399 2513427 2808996 2936860 2794800 2735456
```

```r
head(present$year)
```

```
## [1] 1940 1941 1942 1943 1944 1945
```

```r
# Plot the boy-girl ratio for all years

present$ratio <- present$boys/present$girls

plot(present$year, present$ratio)
```

![plot of chunk unnamed-chunk-7](figure/unnamed-chunk-7-2.png) 

```r
plot(present$year, present$ratio, type = "line")
```

```
## Warning in plot.xy(xy, type, ...): plot type 'line' will be truncated to
## first character
```

![plot of chunk unnamed-chunk-7](figure/unnamed-chunk-7-3.png) 

```r
#Now Find out in what year was the difference between the number of boys and girls greatest.

# Create the variable of the absolute difference for each year
present$absoluteDif <- present$boys - present$girls

# Check that your code did what you expected it to do.
head(present$absoluteDif)
```

```
## [1] 62969 66041 79734 81058 75802 73718
```

```r
# Use the command max() on the newly created variable to find the answer.
max(present$absoluteDif)
```

```
## [1] 105244
```

Answer = There is initially a decrease in the boy-to-girl ratio, and then an increase between 1960 and 1970, followed by a decrease.

#Question 8

Calculate absolute differences between number of boys and girls born in each year, and determine which year out of the present data had the biggest absolute difference in the number of girls and number of boys born?

Answer = 1963

Questions 9 to 13 should be answered by the individuals.
