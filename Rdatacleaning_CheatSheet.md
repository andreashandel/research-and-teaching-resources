#R data cleaning tasks cheat-sheet

This list is a collection of specific commands to do specific, often-needed data cleaning and prepping tasks in R. Most of the commands use the ['tidyverse' packages](https://github.com/hadley/tidyverse). So to make sure commands work, you need the corresponding packages, most simply done by `install.packages(tidyverse)` to get them _all_.

*List maintained by Andreas Handel (ahandel@uga.edu). Last updated 9/22/2016.*
*If you know of other good examples, please let me know.*


__Conventions:__ The data is assumed to be a data frame called `dat`, I'm using the pipe-operator notation, the outcome of interest is called `outcome`, variables are `var1`, `var2`, etc. or just refered to as `varname`

###Renaming a column/variable
`newdat <- dat %>% rename(newvarname = oldvarname)`  

###Renaming values of a a variable
In this example, the value infctd in varname is replaced by 'infected'

`newdat <- dat %>% mutate(varname = replace(varname, varname=='infctd','infected')`  


###Resorting variables
While usually it doesn't matter at which position which variable is, sometimes it's more convenient to for instance have the outcome

`newdat <- dat %>% select(outcome, everything() )`

###Remove variables

Either just pick the ones you want to keep

`newdat <- dat %>% select ( c(var1,var2,var3))`

Or delete the ones you don't want to keep

`newdat <- dat %>% select ( -c(var4,var5,var6) )`


###Checking for NA



