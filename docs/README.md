# Connect Four

Connect-Four is a tic-tac-toe-like two-player game in which players alternately place pieces on a vertical board 7 columns across and 6 rows high. Each player uses pieces of a particular color and the object is to be the first to obtain four pieces in a horizontal, vertical, or diagonal line. Because the board is vertical, pieces inserted in a given column always drop to the lowest unoccupied row of that column. As soon as a column contains 6 pieces, it is full and no other piece can be placed in the column.

### HOW TO PLAY

1. Decide who plays first. Players will alternate turns after playing the first piece.

2. On your turn, place one of you pieces in ANY of the slots by selecting one of the columns on the grid. 

3. Play alternates until one player gets FOUR pieces of his or her color in a row. The four in a row can be horizontal, vertical, or diagonal.

### HOW TO WIN

If you are the first player to get four of your pieces in a row, you win the game!

### TO START ANOTHER GAME

Simply click the reset button at the bottom of the game board. 

# Start Up Screen:
<!-- Images of the start up screen go here  -->
![Startup-Image-1](https://github.com/crchrist/connect-four/blob/main/docs/Screen-Shot-1.png?raw=true)
<br>
![Startup-Image-2](https://github.com/crchrist/connect-four/blob/main/docs/Screen-Shot-2.png?raw=true)
<br>
![Startup-Image-3](https://github.com/crchrist/connect-four/blob/main/docs/Screen-Shot-3.png?raw=true)
<br>
![Startup-Image-4](https://github.com/crchrist/connect-four/blob/main/docs/Screen-Shot-4.png?raw=true)


# HOW TO INSTALL

1. *`Fork`* and *`Clone`* this respository to your local machine
2. Open `index.html` in your browser to play or 
3. Open the directory in your text editor of choice to view or edit the code

## PLAY ONLINE
https://crchrist.github.io/connect-four/


<!-- Other install instructions will go here -->


# HOW IT WORKS

## The Table

```html
<div class="game">
    <table>
        <tr>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
        </tr><tr>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
        </tr><tr>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
        </tr><tr>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
        </tr><tr>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
        </tr><tr>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
            <td class="slot"></td>
        </tr>
    </table>
</div> 
```

## Horizontal Check

```js 
function horizontalCheck(){
    for(let row = 0; row < tableRow.length; row++){
        for (let col = 0; col < 4; col ++){
            if(colorMatchCheck(tableRow[row].children[col].style.backgroundColor, tableRow[row].children[col+1].style.backgroundColor, 
                tableRow[row].children[col+2].style.backgroundColor, tableRow[row].children[col+3].style.backgroundColor)){
                    return true;
                }
        }
    }
};
```

## Vertical Check

```js 
function veritcalCheck(){
    for(let col = 0; col < 7; col ++){
        for (let row = 0; row < 3; row++){
            if (colorMatchCheck(tableRow[row].children[col].style.backgroundColor, tableRow[row+1].children[col].style.backgroundColor,
                tableRow[row+2].children[col].style.backgroundColor, tableRow[row+3].children[col].style.backgroundColor)){
                    return true;
                }
        }
    }
}
```

## Diagnoal Check

```js 
function diagonalCheck1(){
    for (let col = 0; col < 4; col++){
        for (let row = 0; row < 3; row++){
            if(colorMatchCheck(tableRow[row].children[col].style.backgroundColor, tableRow[row+1].children[col+1].style.backgroundColor,
                tableRow[row+2].children[col+2].style.backgroundColor, tableRow[row+3].children[col+3].style.backgroundColor)){
                    return true;
                }
        }
    }
}

function diagonalCheck2(){
    for (let col = 0; col < 4; col++){
        for (let row = 5; row > 2; row--){
            if(colorMatchCheck(tableRow[row].children[col].style.backgroundColor, tableRow[row-1].children[col+1].style.backgroundColor,
                tableRow[row-2].children[col+2].style.backgroundColor, tableRow[row-3].children[col+3].style.backgroundColor)){
                    return true;
                }
        }
    }
}
```

## The Win Check

```js
for (let i = 5; i > -1; i--){
        if(tableRow[i].children[column].style.backgroundColor == 'white'){
            row.push(tableRow[i].children[column]);
            if(currentPlayer ===1){
                row[0].style.backgroundColor = player1Color;
                if (horizontalCheck() || veritcalCheck() || diagonalCheck1() || diagonalCheck2()){
                    playerTurn.textContent = `${player1} WINS!`;
                    playerTurn.style.color = player1Color;
                    return;
                }else if(drawCheck()){
                    playerTurn.textContent = "IT'S A TIE!";
                    return;
                }else{
                playerTurn.textContent = `${player2}'s turn!`;
                return currentPlayer = 2;
            }

        }else{
            row[0].style.backgroundColor = player2Color;
            playerTurn.textContent = `${player1}'s turn`
            if (horizontalCheck() || veritcalCheck() || diagonalCheck1() || diagonalCheck2()){
                playerTurn.textContent = `${player2} WINS!`;
                playerTurn.style.color = player2Color;
                return;
            }else if(drawCheck()){
                playerTurn.textContent = "IT'S A TIE!";
                return;
            }else{
            playerTurn.textContent = `${player1}'s turn!`;
            return currentPlayer = 1;
            }
        }
    }
}
```




# Future Considerations
<br>
- Ending the placement of pieces once a player has won. 
<br>
- Add effect of pieces hovering over column before placement. 
<br>
- Add button to change player name rather than alert on page open. 
<br>
- Add media query 
