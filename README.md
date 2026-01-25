# COC-project--Sudoku-Grid-validator
Author-Priyanshi Jain
<br>
#include <stdio.h>
#include <stdbool.h>
#define SIZE 9
<br>
//Checks if a single row is valid
<br>
bool check_row(int grid[SIZE][SIZE], int row){
bool seen[SIZE +1] = {false};
for(int col = 0; col<SIZE; col++){
int num = grid[row][col];
if(num<1 || num>9 || seen[num])
return false;
seen[num] = true;
}
return true;
}
<br>

bool check_col(int grid[SIZE][SIZE], int col){
ool seen[SIZE+1] = {false};
for(int row=0; row<SIZE; row++){
int num = grid[row][col];
if(num<1 || num>9 || seen[num])
return false;
seen[num] = true;
}
return true;
}
<br>
//check 3*3 box is valid
<br>
bool check_-subgrids(int grid[SIZE][SIZE], int start_row, int start-col){
bool seen[SIZE+1] ={false};
for(int r=0; r<3; r++){
for(int c=; c<3; c++){
    int num = grid[start_row + r][start_col + c];
    if(num < 1 || num > 99 || seen[num])
    return false;
    seen[num] = true;
    }
    <br>
    //check whole grid
    <br>
    bool is is_valid_sudoku(int grid[SIZE][SIZE]){
    for(int i=0; i<SIZE; i++){
    if(! check_row(grid,i) || ! check_col((grid,i))
    return false;
    }
    for(int r=0; r<SIZE; r += 3){
    if(! check_subgrid(grid,r,c))
    return false;
    }
    }
    return true;
}
int main(void){
int grid[SIZE][SIZE];
printf("Enter the sudoku grid (row by row, 9 numbers er line):");
for(int i=0; i<SIZE; ++i){
   for(int j=0; j<SIZE; ++j){
   if(scanf("%d", &grid[i][j]) !=1){
   printf("Invalid input.");
   return 1;
   }
   }
}
if(isvalid_sudoku(grid)){
Printf("VALID SOLUTION");
} else {
printf(INVALID SOLUTION");
}
return 0;
}



