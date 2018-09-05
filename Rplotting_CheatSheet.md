# R plotting commands cheat-sheet

This list is a collection of specific commands to do specific (pieces of) plots that I often need. Most of the commands use ggplot2.

*List maintained by Andreas Handel (ahandel@uga.edu). Last updated 12/9/2016.*
*If you know of other good examples, please let me know.*


__Conventions:__ The data is assumed to be a data frame called `dat`, I'm using the pipe-operator notation, the outcome of interest is called `outcome`, variables are `var1`, `var2`, etc. or just refered to as `varname`. ggplot library is assumed to be loaded for most commands.


#### Increase legend
If one uses dashed/dotted/solid lines in lineplots, the default legend in ggplot is often not big enough to properly show the different lines. One can increase this with
```{r}
theme(legend.key.width = unit(X,"line"))
````
where X is the length/width one wants.


#### Sorting order of entries in plots/legend
ggplot shows legends alphabetically for non-factor variables. Easiest approach is to turn variable into factor and sort as needed. 


