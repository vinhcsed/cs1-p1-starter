# CS1: Project 1

## Setup
1. Update the contents of *ID.txt* with your identifier (school email **without @school.edu**).
2. Write pseudocode for your program in *PSEUDO.txt*.

## How to Run Your Program
* [**WINDOWS**]
   - In VSCode, press the play button in the top right corner (it should appear when you open a `.cpp` file). Your program should compile and run.
   - Alternatively, open a terminal. Type `.\make.bat` and press return. Your program should compile and run.
* [**MAC/LINUX**]
   - Open a Terminal. Type `make` and press return. Your program should compile and run.

## Assignment Specification
### Combat Canoes
* Implement this program in `main.cpp`.
* This program will be a variation on the game Battleship.
* The game is played on a 4x4 board.
   - The board must be represented by a 2D array
   - You will likely need two 2D arrays (one to represent the board state and one to represent the "solution")
   - Unknown spaces are represented by a hashtag `#`
   - Spaces occupied by canoes are represent by capital alphabetic letters `A, B, C`
   - The board array is accessed using row/column indices
* When the game starts, the board is randomly populated with exactly three canoes of random length
   - Canoes have a maximum length of four
   - Canoes only need to span horizontally
   - You will need to develop an algorithm to randomly generate canoes with these restrictions
* The user will be prompted to select a row and a column.
   - If the selected space has already been selected OR it is outside the bounds of the board, the user should be continuosly prompted for a valid selection
   - If the selected space contains a canoe, it should be revealed
   - If the selected space does not contain a canoe, it should be marked with an asterisk `*`
* The user has 5 total attempts to "hit" all the canoes. Each time the user "misses" they consume one attempt.
* After any attempt, if all canoes have been revealed, the user wins.
* At the end of the game (when the user wins OR all attempts have been used), all canoes should be revealed.

### Other Requirements
* This starter code includes function commented prototypes to help you get started. These functions are not required.
* Regardless if you use the provided prototypes, your program logic must be organized into functions.
* You will be graded on code cleanliness and design.

#### Example
```
COMBAT CANOES
Try to hit all 3 canoes!
  0 1 2 3 
0 # # # #
1 # # # #
2 # # # #
3 # # # #
Select a row: -1
Select a col: 3
Invalid choice, please try again.
Select a row: 0
Select a col: 5
Invalid choice, please try again.
Select a row: 0
Select a col: 0
MISS!
4 attempts left.
  0 1 2 3 
0 * # # #
1 # # # #
2 # # # #
3 # # # #
Select a row: 0
Select a col: 0
Invalid choice, please try again.
Select a row: 1
Select a col: 3
HIT!
4 attempts left.
  0 1 2 3 
0 * # # #
1 # # # A
2 # # # #
3 # # # #
Select a row: 1
Select a col: 2
HIT!
4 attempts left.
  0 1 2 3 
0 * # # #
1 # # B A
2 # # # #
3 # # # #
Select a row: 2
Select a col: 2
HIT!
4 attempts left.
  0 1 2 3 
0 * # # #
1 # # B A
2 # # C #
3 # # # #
Select a row: 3
Select a col: 3
MISS!
3 attempts left.
  0 1 2 3 
0 * # # #
1 # # B A
2 # # C #
3 # # # *
Select a row: 3
Select a col: 0
MISS!
2 attempts left.
  0 1 2 3 
0 * # # #
1 # # B A
2 # # C #
3 * # # *
Select a row: 2
Select a col: 1
HIT!
2 attempts left.
  0 1 2 3 
0 * # # #
1 # # B A
2 # C C #
3 * # # *
Select a row: 2
Select a col: 0
MISS!
1 attempts left.
  0 1 2 3 
0 * # # #
1 # # B A
2 * C C #
3 * # # *
Select a row: 0
Select a col: 3
MISS!
0 attempts left.
YOU LOSE!
  0 1 2 3 
0 # # # #
1 B B B A
2 # C C C
3 # # # #
```

## Submission
1. Remember to *commit* and *push* your changes to this repository.
