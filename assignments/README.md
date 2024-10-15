# Possible Assignments

## Movement
Agents move in a two-dimensional grid randomly.

This is POSSIBLE thanks to the Excel's iterative recalculation function (set to 1, so that it "saves" the last iteration's values).

## Forest Fire
Spread of fire in a two-dimensional forest where each cell represents a tree in either of three states: idle, burning or dead.

This may be possible to model thanks to the Excel's iterative recalculation function, however, we would not get partial results, only the final result, which is not sufficient for the simulation's analysis.

## Population
The population consists of males and females that grow old, can reproduce and eventually die. The aim is to calculate whether in time, the population grows or diminished.

This is NOT POSSIBLE due to missing Excel functionality.
1. Excel cannot generate new rows when a new child is born
2. Excel cannot remove a row when a person dies
3. Excel cannot perform operations such as "if a certain condition in a cell is met, do something with a different cell", it can only update its own value based on a formula (however, this is doable through iterative recalculation and many helper cells)

Based on [NetLogo Sex Ratio Equilibrium](https://ccl.northwestern.edu/netlogo/models/SexRatioEquilibrium)

