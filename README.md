# MDP

All the project's Classes are in one single java file
All that is required to run is to compile the java file and run it

Once you run the program that is what will be presented to the user.
Please note that on every run:
	It will start with a new randomly policy assigment
	The trajectory will be created by samplying random numbers (0 to 84 sucessfuly goes to the desired direction;  85 to 92 skew one direction, 99 onwards skew the other dirrection 

Explaining graphics:
	Policy directions will be represented by arrows. Bad State by X and Goal states by O 
	The table for trajectory indicates: B- Blocked cell of the grid; U- position of UAV; X- Bad state; O- Goal state

Objects: 
	To better represent the problem and MDP I created different classes to represent this problem as a grid, a matrix of 4x4. 
	Each cell of the grid is an object with some important information for each state 
		 * @row: row number this cell is at
 		 * @col: col number this cell is at
 		 * @reward: reward of each state
		 * @utility: the utility for that state
		 * @closed: in this example there are cells of the grid that are closed, behaves like walls
		 * @start_state: indicator from where the UAV starts at
		 * @action: what is the best action to perform from this state

For more information please refer for the in-code comments
======================================================================================
        EXECUTING THE PROGRAM BELOW
======================================================================================

Creating grid:
  Discount factor: 0.9
   Generating random policy
   Random policy created:

| X | ^ | < | O |
| v |   | < | ^ |
| < | ^ | < | < |
| ^ | v | > | O |

Initiating Policy Iteration
 Number of iterations: 7
 Converged policies:
-----------------
| X | > | > | O |
| v |   | > | ^ |
| > | > | > | v |
| > | > | > | O |
-----------------
Generating trajectory from (0,0)
 Terminating at goals: (0,3) or (3,3)
 Terminating at bad state: (3,0)
Starting - 
----------------
Action at (0,0): RIGHT
| X |   |   | O |
|   | B |   |   |
|   |   |   |   |
| U |   |   | O |
----------------
Action at (0,1): RIGHT
| X |   |   | O |
|   | B |   |   |
|   |   |   |   |
|   | U |   | O |
----------------
Action at (0,2): RIGHT
| X |   |   | O |
|   | B |   |   |
|   |   |   |   |
|   |   | U | O |
----------------
Got to goal state
| X |   |   | O |
|   | B |   |   |
|   |   |   |   |
|   |   |   | U |
