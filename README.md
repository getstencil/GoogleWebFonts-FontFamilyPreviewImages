
Naming convention of files:  
Non-hyphens, non-alphabetic and non-numeric characters are removed. This includes spaces.  
Naturally, I leave the case of the `family` as is.


Here is the regex I use to strip out those characters: `/[^A-Za-z0-9\-]/`
