# Data Sceince in Scala

## Libraries

### Base 

#### Breeze (like Numpy)


#### Saddle (like R or Panda)


### Visualization

#### Wisp 
https://github.com/quantifind/wisp
Interactive web-based (Highcharts) Scala Plotting

#### Vega 

### Interoperability

#### jvmr 
http://dahl.byu.edu/software/jvmr/
https://github.com/dbdahl/jvmr
https://github.com/cran/jvmr

*A self-contained and bi-directional interface between R and Scala, Java, and other JVM-based languages*

```
> b=breezeInit()
> b['import breeze.stats.distributions._']
NULL
> b['Poisson(10).sample(20).toArray']
 [1] 13 14 13 10  7  6 15 14  5 10 14 11 15  8 11 12  6  7  5  7
> summary(b['Gamma(3,2).sample(10000).toArray'])
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
 0.2124  3.4630  5.3310  5.9910  7.8390 28.5200 
> 
```


***
