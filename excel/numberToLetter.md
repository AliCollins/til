# Formula to Convert Number to Letter

A formula for converting a numeric value into the equivelent column letter name:

```vbnet
=SUBSTITUTE(ADDRESS(1,COLUMN(),4),"1","")
```
