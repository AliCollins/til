# Selection

Saving the current selected range to return to it later (so the user doesn't see a change in selection, if used for copy/paste etc):
```
Dim r As Range
Set r = Range(Selection.Address)

[Do some work]

r.Select
Application.CutCopyMode = False
```
