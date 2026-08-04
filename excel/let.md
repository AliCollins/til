# Let

Because `INDIRECT()` is volatile and can be expensive if used multiple times, in modern Excel you can use `LET`:
```
=LET(txt,INDIRECT(A1),RIGHT(txt,LEN(txt)-4))
```
This calculates the `INDIRECT()` result only once.

However, you can also use it to calculated multiple named pairs. E.g. `=LET(a,1,b,2,c,3,a+b+c)` gives the result 6.
