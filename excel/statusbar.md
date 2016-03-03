# Microsoft Excel Statusbar Updates

A way of showing updates on the progress bar:
```
For i = 1 to 50
  Application.StatusBar = "Progress: " & i & " of 50: " & Format(i / 50, "0.0%")
Next i
Application.StatusBar = false
```
