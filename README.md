# Knight's Tour

On a chess board, a knight's move consists of moving two squares in one direction and then one square left or right. In the picture below, K represents the current position of a knight and x represents the possible squares to which the knight can move in one step.

      . x . x .
      x . . . x
      . . K . .
      x . . . x
      . x . x .

A knight's tour of an M × N chess board with M rows and N columns is a sequence of knight's moves that visits all squares of the board exactly once.

Represent each square of an M × N chessboard as a pair (i,j), 1 ≤ i ≤ M and 1 ≤ j ≤ N, giving the row number and column number of the square.

I have created a Python function knightstour(M,N,i,j) that takes as input the board dimensions M × N and the starting position (i,j) and returns a list of positions corresponding to knight's tour for an M × N chessboard, starting at (i,j). If no tour is possible, my function returns the empty list [].

For instance knightstour(5,6,1,1) will return the following solution:

      [(1, 1), (2, 3), (1, 5), (3, 6), (5, 5),
       (4, 3), (5, 1), (3, 2), (4, 4), (5, 6),
       (3, 5), (1, 6), (2, 4), (1, 2), (3, 1),
       (5, 2), (3, 3), (4, 5), (5, 3), (4, 1),
       (2, 2), (1, 4), (2, 6), (3, 4), (4, 6),
       (5, 4), (4, 2), (2, 1), (1, 3), (2, 5)]

Here I have implemented the heuristic known as Warnsdorff's rule to speed up the search.
