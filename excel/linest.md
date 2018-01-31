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
