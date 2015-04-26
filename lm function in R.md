---
title: "lm function in R"
output: html_document
---
```{r}
x <- 1:3
y <- c(5,7,9)
plot(c(0,x),c(3,y))
lines(c(0,x),c(3,y),type = "l", lwd = 2, col = "red")

#method 1
#The follow command fit outcome y w.r.t predictor x, with intercept. As we can see, Intercept is 3 and slope of regression line is 2.
lm(y~x)

#method 2
#The follow command fit outcome y w.r.t predictor x, without intercept. i.e. It fits data points by a line passing throuth 0.
lm(y~x-1)
```
Specificly, to fit (1,5),(2,7),(3,9) by method 2, we need to 
minimize
l(a) = (ax1 - 5)^2 + (ax2 - 7)^2 + (ax3 - 9)^2
Apply calculus, we get a = 23/7 = 3.285714, which is the same as the result from command lm(y~x-1).
