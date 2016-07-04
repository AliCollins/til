# Sheet Name

A way of getting the name of the current worksheet from a formula:
```
=MID(CELL("filename",A1),FIND("]",CELL("filename",A1))+1,255)
```

(See https://exceljet.net/formula/get-sheet-name-only for description)
