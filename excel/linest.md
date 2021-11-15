### Linear Trendline
Equation: `y = m * x + b`
```
m: = SLOPE(y,x)
b: = INTERCEPT(y,x)
```
### Logarithmic Trendline
Equation: `y = (c * LN(x)) + b`
```
c: = INDEX(LINEST(y,LN(x)),1)
b: = INDEX(LINEST(y,LN(x)),1,2)
```
### Power Trendline
Equation: `y = c * x^b`
```
c: = EXP(INDEX(LINEST(LN(y),LN(x),,),1,2))
b: = INDEX(LINEST(LN(y),LN(x),,),1)
```
### Exponential Trendline
Equation: `y = c * exp(b * x)`
```
c: = EXP(INDEX(LINEST(LN(y),x),1,2))
b: = INDEX(LINEST(LN(y),x),1)
```
### 2nd Order Polynomial Trendline
Equation: `y = (c2 * x^2) + (c1 * x) + b`
```
c2: = INDEX(LINEST(y,x^{1,2}),1)
c1: = INDEX(LINEST(y,x^{1,2}),1,2)
b:  = INDEX(LINEST(y,x^{1,2}),1,3)
```
### 3rd Order Polynomial Trendline
Equation: `y = (c3 * x^3) + (c2 * x^2) + (c1 * x) + b`
```
c3: = INDEX(LINEST(y,x^{1,2,3}),1)
c2: = INDEX(LINEST(y,x^{1,2,3}),1,2)
c1: = INDEX(LINEST(y,x^{1,2,3}),1,3)
b:  = INDEX(LINEST(y,x^{1,2,3}),1,4)
```

### Calculating R<sup>2</sup>
Additional statistics need to be included, then it is in INDEX(...,3,1), for example for a Power Trendline:
```
R^2: = INDEX(LINEST(LN(y),LN(x),,TRUE),3,1)
```

### Filtered Data
See: https://superuser.com/a/821484/28450


### Apply Operator to Y data series
For example below I’ve used it to allow me to fit a cubic polynomial, but with the X^2 coefficient forced by me. $M90 is the forced X^2 coefficient, INDIRECT(D84) is the Y data series and INDIRECT(C84) is the X data series:
```
=LINEST(INDIRECT(D84)-$M90*INDIRECT(C84)^2,INDIRECT(C84)^{1;3},TRUE,FALSE)
```
This is really handy as it allows you to vary one of the coefficients and see what effect it would have on the others.
