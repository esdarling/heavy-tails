# Black swans in ecological time series

This repository holds code for an in-progress analysis of heavy-tailed
population dynamics. This analysis is for a PhD thesis chapter and paper by
Sean Anderson, Trevor Branch, Andy Cooper, and Nick Dulvy.

The analysis (`analysis/`) can be run by `source()`ing the file `make.R` from
within the `analysis` folder (or by running the `make` command in the Terminal
in the `analysis` folder). Alternatively, you can work through the `.R` files in
sequence (`1-...R`, `2-...R`, etc.) in an R console. Files that start with the
same number can be sourced in any order. Note that some components (population
dynamic model fitting files that start with `2-` and beta-distribution
multilevel models starting with `5.X-`) may take a long time to fit (from hours
to approximately a day depending on the file). These were run on the
[WestGrid](https://www.westgrid.ca/) computing facilities.

While I'm still actively working on this analysis, watch out for hardcoded file
paths. These make it much easier for me to quickly work on the WestGrid servers.
For example, see `root_folder = "/global/scratch/anderson/heavy"` in 
[this file](https://github.com/seananderson/heavy-tails/blob/master/analysis/1.5-compile-fit-function.R). 
Eventually I plan to remove these *and* add an option to download my previously run models.

The `analysis/gpdd/` folder contains data from the Global Population Dynamics
Database:

NERC Centre for Population Biology, Imperial College (2010). *The Global
Population Dynamics Database Version 2*.
<http://www3.imperial.ac.uk/cpb/databases/gpdd>

The file `analysis/brook-etal.csv` contains a copy of the data from the
supplemental Excel spreadsheet in:

Brook, B.W., Traill, L.W. & Bradshaw, C.J.A. (2006).
Minimum viable population sizes and global extinction risk are unrelated.
*Ecol. Lett.* 9, 375-382. <http://doi.org/10.1111/j.1461-0248.2006.00883.x>

The analysis was run with the following R packages in R 3.1.2 (local) or 3.1.0/3.1.1
(WestGrid):

### Statistics
- rstan (2.5.0) (with Stan 2.5)
- metRology (0.9-17)

### Data manipulation
- dplyr (0.3.0.9000)
- plyr (1.8.1)
- reshape2 (1.4)

### Plotting
- ggplot2 (1.0.0.99)
- gridExtra (0.9.1)
- RColorBrewer (1.0-5)
- grImport (0.9-0)
- TeachingDemos (2.9)
