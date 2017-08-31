In this exercise you will explore Constraint Satisfaction Problems by implementing the N-Queens problem using symbolic constraints in a Jupyter notebook, and solving it using the Backtracking Search algorithm from AIMA.

To launch the notebook, run the following command from a terminal with anaconda3 installed and on the application path:

    jupyter notebook AIND-Constraint_Satisfaction.ipynb

## Notes by Jin:

You can run this by setting up an environment in anaconda dependencies required in the jupyter notebook

This project was a step towards building a more general problem solver with domain indpendent heuristics with problems that can be defined in binary constraints. The backtracking algorithm implemented in this project can solve problems with finite and discrete domains.


### Backtracking Algorithm

Implemented the [backtracking search algorithm](https://github.com/aimacode/aima-pseudocode/blob/master/md/Backtracking-Search.md) in the AIMA textbook. 

#### Optimizations
Note: Unit tests were added to validate the optimization algorithms.

##### Arc Consistency (2-consistency)

The AC-3 inference algorithm (As described in Figure 6.3 of AIMA [1]) is used for arc-consistency (2-consistency) check for when a value is picked for a variable in the backtracking algorithm. This allowed the algorithm to infer and backtrack quicker.

##### Minimum Remaining Value (MRV)

Added the MRV (most contrained variable) heuristic as part of the select function in the backtracking algorithm so we have a higher chance to cause a failure sooner by picking the variable with less available values in the domain.

##### Least Constraining Value (LCV)

This heuristic was implemented for when we pick a value for the variable in the backtracking algorithm. It picks the variable that leaves the most options for subsequent variable selection. This is somewhat different from MRV in that MRV tries to find the value with the least constraint while LCV tries to pick the value that allows the next variable to have more options so it tries to see if there is a solution in the current branch of the search.

### Outcome

![alt text](https://github.com/baek-jinoo/AIND-Constraint_Satisfaction/blob/master/assets/outcome.png?raw=true "Outcome")



### Reference

[1] Artificial Intelligence: A Modern Approach (3rd Edition) (11 December 2009) by Stuart Russell, Peter Norvig

