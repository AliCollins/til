# Dynamic Named Range

If a graph of a dynamicly changing range is required in an Excel sheet, this can be done by creating a named range and using the LET function, with FILTER to remove blank cells:
```
=LET(x,Polynomial!$BC$5:INDEX(Polynomial!$BC:$BC,ROW(Polynomial!$BC$5)+200),FILTER(x,x<>""))
```
Polynomial!$BC$5 is the first cell of data in the chosen column (Polynomial!$BC:$BC).
