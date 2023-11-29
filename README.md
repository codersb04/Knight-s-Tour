# Knight-s-Tour
## Task
Create an algorithm to perform the knight's tour.</br>
Given a knight who can traverse only in 'L' shape, and the knight has to visit each and every block of given n*n board.
## Steps Followed
- Get the input from the user for the size of board and the initial position(Value of row and column)
- Create and print a board with the given size using functions **chess_board(size)** and print_board(board)
- Get all the possible moves from a particular position using function **moves(x, y, board, size)**, there are maximum of 8 possible moves from one point and can be calculated using:
  - All the possible position for row movement [-2, -2, 1, -1, 1, -1, 2, 2]
  - All the possible position column row movement [-1, 1, -2, -2, 2, 2, -1, 1]
- Update the board with the new found position using function **update_board(board, position_x, position_y, moves)**
- Perform the knights tour task using **Warnsdorff's Algorithm** in function **knights_tour(size, row, col)**:
  - Warnsdorff's Algorithm: Algorithm can start from any random position from the given board,
    - To get the next position, a list of all possible move is created and **the position with least number for next moves is choose as a next move** (as keeping the node with more number of possiblities reservered for later use when board would be almost full)
  - Update the move number and board according to the new position
  - repeat the steps for size*size times
