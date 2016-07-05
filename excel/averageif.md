# Average If...

Average of a range, even if it includes #N/A or similar:
```vbnet
=AVERAGE(IF(ISNUMBER(A1:A4),A1:A4))
```
This is an array formula and needs to be entered using CTRL + Shift + Enter, not just Enter.
