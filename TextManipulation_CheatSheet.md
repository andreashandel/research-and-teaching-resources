#R text wrangling and manipulation commands cheat-sheet

This list is a collection of specific commands to do specific text/string manipulations in R.

*List maintained by Andreas Handel (ahandel@uga.edu). Last updated 7/9/2018.*
*If you know of other good examples, please let me know.*



#### Insert a blank between 2 bits of text.

This uses regex capturing groups.

```{r}
gsub("(#)(\\w)","\\1 \\2", text) #first symbol is a #, second is a word character. an empty space is inserted.  
gsub("(#)([A-Z])","\\1 \\2", text) #first symbol is a #, second is an upper case letter. an empty space is inserted.
```

