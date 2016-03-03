### Excel VBA Timers

A simple way of getting a timer with second resolution
```
[H5] = Now()
[H6] = ""

for i = 1 to 1000000000
Next i

[H6] = Now()
```

A (fairly) simple way of getting a timer with millisecond resolution
```
Private Declare Function GetTickCount Lib "kernel32" () As Long
...
[H5] = GetTickCount
[H6] = ""

for i = 1 to 1000000000
Next i

[H6] = GetTickCount
```
