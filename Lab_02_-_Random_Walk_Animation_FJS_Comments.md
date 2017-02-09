Lab 02 - Random Walk Animation
================
Francisco Santamarina
February 2, 2017

Load the necessary packages and dataset.

``` r
library( animation )
```

#### Animation

``` r
saveGIF({
    random.walk <- 0
    for( i in 1:100)
    {
      random.walk[i] <- cumsum(rnorm(100))
      plot( random.walk, type="l", col="darkred", axes=F, 
            xlab="", ylab="", xlim = c(0,100), ylim = c(-3,3), 
            main="Random Walk" )
      abline( h=0, lty=2, col="gray" )
    }
},

movie.name = "Random_Walk_Animation.gif",
interval = .1,
ani.width = 800,
ani.height = 400
)
```

![](C:/Users/franc/Documents/GitHub/DDM-II/lab-02-animations-fjsantam/Random_Walk_Animation.gif)
