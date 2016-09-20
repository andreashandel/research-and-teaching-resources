#This list is a collection of specific commands to do Data Analysis tasks in R

*List maintained by Andreas Handel (ahandel@uga.edu). Last updated 9/22/2016.*
*If you know of other good examples, please let me know.*

Most of the commands use the ['tidyverse' packages](https://github.com/hadley/tidyverse). 
So to make sure commands work, you need the corresponding packages, most simply done by `install.packages(tidyverse)` to get them _all_.

__Conventions:__ The data is assumed to be a data frame called `dat`, I'm using the pipe-operator notation, the outcome of interest is called `outcome`, variables are `var1`, `var2`, etc. or just refered to as `varname`

###Renaming a column/variable
`newdat <- dat %>% rename( newvarname = oldvarname)`  

###Renaming values of a a variable
In this example, the value 1 in varname is replaced by 'infected'
`newdat <- dat %>% mutate(varname = replace(varname, '1','infected')`  

###Resorting variables
While usually it doesn't matter at which position which variable is, sometimes it's more convenient to for instance have the outcome



