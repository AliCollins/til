

///
Dim r As Range
Set r = Range(Selection.Address)

[Do some work]

r.Select
Application.CutCopyMode = False
///
