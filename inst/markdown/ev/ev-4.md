## Grid capacity approach

This user case is different than the *timeframe* one. Here the objective is to distribute a given amount of power among several charging EVs.

This will only be a problem if the demand of all EVs exceed the grid capacity. In this case, [`distribute()`](.#distribute) is used to allocate the appropriate amount of power to each EV. The parameters `soc`, `vol`, `share`, `cap` and `level` serve not only to decide the order of preference, but also to predict the time when the charge of the battery will be complete.  
