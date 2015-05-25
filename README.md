# Data Science in Scala

## Libraries

### Base 

#### netlib-java

https://github.com/fommil/netlib-java

*netlib-java is a wrapper for low-level BLAS, LAPACK and ARPACK that performs as fast as the C / Fortran interfaces with a pure JVM fallback*
*Used by Breeze and Spark*

to temporarly avoid 
```
java: symbol lookup error: /tmp/jniloader1662186932314700536netlib-native_system-linux-x86_64.so: undefined symbol: cblas_dcopy
```
because some compilation flag stuff on Fedora packages, you need to start sbt with those args 
```
sbt -Dcom.github.fommil.netlib.BLAS=com.github.fommil.netlib.F2jBLAS -Dcom.github.fommil.netlib.LAPACK=com.github.fommil.netlib.F2jLAPACK -Dcom.github.fommil.netlib.ARPACK=com.github.fommil.netlib.F2jARPACK
```

#### Breeze 

*like Numpy*

##### Example

```scala
import breeze.linalg._
```

#### Saddle 

*like R or Panda*


### Visualization

#### Wisp 

https://github.com/quantifind/wisp

*Interactive web-based (Highcharts) Scala Plotting*

#### Vega 

### Interoperability

#### jvmr 

http://dahl.byu.edu/software/jvmr
https://github.com/dbdahl/jvmr
https://github.com/cran/jvmr

*A self-contained and bi-directional interface between R and Scala, Java, and other JVM-based languages*

```R
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
