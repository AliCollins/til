### Find the Last Match in a column
Suppose you want to find index of the last instance of id "id_1" in range A2:A8, then use:
```
=MATCH(2,1/(A2:A8="id_1"))
```
This syntax is a special trick: ```(A2:A8="id_1")``` evaluates to ```{TRUE,FALSE,FALSE,TRUE,...}```. Next, assuming that ```TRUE=1``` and ```FALSE=0```, the part ```1/{TRUE,FALSE,FALSE,TRUE,...}``` gives you ```{1,#DIV0!,#DIV0!,1,..}```.
To return last number in resulting array lookup_value should be greater than any value in lookup_array ```({1,#DIV0!,#DIV0!,1,..}``` in our case). Since array contains only ```1``` or ```#DIV0!```, we can take ```2``` as lookup_value, because it's always greater than ```1```.

See [find last match in column using built in functions in excel](https://stackoverflow.com/questions/23205575/find-last-match-in-column-using-built-in-functions-in-excel) and answer [https://stackoverflow.com/a/23205637/201618](https://stackoverflow.com/a/23205637/201618).
