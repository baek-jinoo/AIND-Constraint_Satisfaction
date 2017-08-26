In this exercise you will explore Constraint Satisfaction Problems by implementing the N-Queens problem using symbolic constraints in a Jupyter notebook, and solving it using the Backtracking Search algorithm from AIMA.

To launch the notebook, run the following command from a terminal with anaconda3 installed and on the application path:

    jupyter notebook AIND-Constraint_Satisfaction.ipynb

Notes by Jin:

You can run this by setting up anaconda with an environment that installs the imported modules shown in the jupyter notebook


### Backtracking Algorithm

Implemented the backtracking search algorithm in the AIMA textbook

#### Optimizations

##### Arc Consistency (2-consistency)

The AC-3 inference algorithm (As described in Figure 6.3 of AIMA [1]) is used for arc-consistency (2-consistency) check for when a value is picked for a variable in the backtracking algorithm.

##### Minimum Remaining Value (MRV)

Also added the minimum remaining value (most contrained variable) heuristic as part of the select function in the backtracking algorithm so we have a higher chance to cause a failure soon by picking the variable with the highest constraint.

##### Least Constraining Value

This heuristic was implemented for when we pick a value for the variable 
Select the order of the values in the domain of a variable
Ordering with most count to optimize the constraint satisfaction process

least constraining value
Used unit tests to validate the optimizations


### Outcome

![alt text](https://github.com/baek-jinoo/AIND-Constraint_Satisfaction/blob/master/assets/outcome.png?raw=true "Outcome")


[1] Artificial Intelligence: A Modern Approach (3rd Edition) (11 December 2009) by Stuart Russell, Peter Norvig

