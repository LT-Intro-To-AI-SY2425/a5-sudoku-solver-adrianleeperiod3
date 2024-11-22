# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. How do the performance and efficiency of the Depth-First Search (DFS) and Breadth-First Search (BFS) algorithms compare when solving Sudoku puzzles? In what scenarios might one approach be preferable over the other?

DFS required less iterations to complete more difficult puzzles, however BFS would likely be more successful on bigger sudoku boards which hold more possibilities. Since DFS explores each pathway in its entirety until failure, boards which force the algorithm to make more guesses on a constrained cell would increase the number of computations DFS needs to be successful. Therefore, for theoretical boards of larger size, BFS would be the more efficient method of search as it is able to explore numerous possibilities in a faster manner. 

2. How did the choice of data structures (like the Stack for DFS and Queue for BFS) impact the implementation and functionality of the algorithms? Are there alternative data structures or design patterns that could have been used to achieve the same objectives?

Other examples of linear data structures besides stack & queue are arrays and linked lists. However, these structures do not seem to offer any inherent advantage to this situation. Another type of structure that can be created is a list which selects choice at random, as opposed to being FILO or LILO. This carries the potential to be the most efficient or most inefficient methods of handling.

3. Considering the current implementation, how might the Sudoku solver be adapted or extended for larger puzzles or different types of grid-based logic games? How can the lessons learned from this assignment be applied to real-world problem-solving or optimization challenges?

For single player grid based logic games, the approach we took is likely one of the most effective for solving the puzzle. Bigger sudoku puzzles or grid based games may require some tweaking to the algorithm to exploring a larger amount of possbilities to keep computation time down. Optimizing the solutions to real-world problems can become easier considering the lessons learned in how FILO and LILO operate. Selecting which one to use and the benefits and downfalls of each can help in deciding how to approach an intimidating problem. 