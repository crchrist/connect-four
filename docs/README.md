# Connect Four

Connect-Four is a tic-tac-toe-like two-player game in which players alternately place pieces on a vertical board 7 columns across and 6 rows high. Each player uses pieces of a particular color and the object is to be the first to obtain four pieces in a horizontal, vertical, or diagonal line. Because the board is vertical, pieces inserted in a given column always drop to the lowest unoccupied row of that column. As soon as a column contains 6 pieces, it is full and no other piece can be placed in the column.

https://crchrist.github.io/connect-four/

# HOW TO PLAY

1. Decide who plays first. Players will alternate turns after playing the first piece.

2. On your turn, place one of you pieces in ANY of the slots by selecting one of the columns on the grid. 

3. Play alternates until one player gets FOUR pieces of his or her color in a row. The four in a row can be horizontal, vertical, or diagonal.

# HOW TO WIN

If you are the first player to get four of your pieces in a row, you win the game!

# TO START ANOTHER GAME

Simply click the reset button at the bottom of the game board. 

## Start Up Screen:
<!-- Images of the start up screen go here  -->



# HOW TO INSTALL

## Example
1. *`Fork`* and *`Clone`* this respository to your local machine
2. Open `index.html` in your browser to play or 
3. Open the directory in your text editor of choice to view or edit the code

<!-- Other install instructions will go here -->


# HOW IT WORKS

```<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <link rel="icon" type="image/gif/png" href="https://www.pinclipart.com/picdir/big/357-3572805_four-in-a-row-circle-clipart.png">
    <title>Connect Four</title>
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@600&display=swap" rel="stylesheet">

</head>
<body>

<h1>Connect Four</h1>

<h3 class="player-turn"></h3>

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

<div class ='popup' id='popup-1'>
    <div class='overlay'></div>
    <div class='content'>
        <div class='close-btn' onclick='togglePopup()'>&times;
</div> 
    <h3>HOW TO PLAY</h3>
    <p> 1. Player one will go first. Players will alternate turns after playing the first piece.
        <br><br>
        2. On your turn, place one of your pieces in ANY of the slots by selecting one of the slots on the grid. 
        <br><br>
        3. Play alternates until one player gets FOUR pieces of his or her color in a row. The four in a row can be horizontal, vertical, or diagonal.
        <br><br>
        <h3>HOW TO WIN</h3>
        If you are the first player to get four of your pieces in a row, you win the game!
        <br><br>
        <h3>START ANOTHER GAME</h3>
        Simply click the reset button at the bottom of the game board. </p>
    </div>
</div>

<button class="instructions" onclick='togglePopup()'>Instructions</button>

<div class="reset">Reset</div>

    <script src="app.js"></script>
</body>
</html>```


```  *{
      margin: 0;
      padding: 0;
      box-sizing: border-box;
  }



  body {
    background-image: url("https://st2.depositphotos.com/4112313/6977/v/600/depositphotos_69779337-stock-illustration-abstract-bright-blue-geometric-background.jpg");
    background-size: 100%;
  }

  h1{
      text-align: center;
      Color: blue;
      font-size: 100px;
    
  }

  .player-turn{
    position: relative;
        top: 5vh;
        left: 50%;
        width: 150px;
        transform: translate(-50%);
        text-align: center;
        cursor: default;
        background-color: #4370F1;
        border-radius: 5px;
        border: none;
        color: white;
        display: block;
        font-size: 16px;
        font-weight: bold;
        padding: 15px 30px;
        text-transform: uppercase;
  }

  .game{
      position: relative;
      top: 4rem;
      left: 50%;
      transform: translate(-50%);
      width: 650px;
      height: 600px;
      background: yellow;
      border: 12px solid blue;
      border-radius: 8%;
      box-shadow: 5px 5px rgb(131, 128, 128);
      padding: 1rem;
    }

    .slot{
        width: 90px;
        height: 90px;
        background: white;
        border: 5px solid darkkhaki;
        border-radius: 50%;
    }

    .instructions{
      position: relative;
      top: 10vh;
      left: 40%;
      transform: translate(-50%);
      text-align: center;
      cursor: pointer;
      background-color: #4370F1;
      border-radius: 5px;
      border: none;
      color: white;
      display: block;
      font-size: 16px;
      font-weight: bold;
      padding: 15px 30px;
      text-transform: uppercase;
  }

  .instructions:hover {
    background-color: #1D50F1;
  }
  
  .instructions:active {
    background-color: #4d7ef1;
  
  }
    
  
    .popup .overlay {
      position: fixed;
      top: 0px;
      left: 0px;
      width: 100vw;
      height: 100vh;
      background: rgba(0,0,0,0.7);
      z-index: 1;
      display:none;
    }

    .popup .content {
      position: absolute;
      top:50%;
      left:50%;
      transform:translate(-50%, -50%) scale(0);
      background:yellow;
      width:450px;
      height: auto;
      z-index: 2;
      text-align: center;
      padding:20px;
      box-sizing: border-box;
      border-radius: 10%;
    }

    h3 {
      color:blue;
      font-size: xx-large;
    }

    .popup .close-btn {
      cursor: pointer;
      position:absolute;
      right:20px;
      top:20px;
      width:30px;
      height:30px;
      background:blue;
      color:white;
      font-size:25px;
      font-weight: 600;
      line-height: 30px;
      text-align: center;
      border-radius: 50%;
    }

    .popup.active .overlay {
      display: block;
    }

    .popup.active .content {
      transition:all 300ms ease-in-out;
      transform:translate(-50%, -50%) scale(1);
    }

    
    .reset{
        position: relative;
        top: 5vh;
        left: 60%;
        width: 150px;
        transform: translate(-50%);
        text-align: center;
        cursor: pointer;
        background-color: #4370F1;
        border-radius: 5px;
        border: none;
        color: white;
        display: inline-block;
        font-size: 16px;
        font-weight: bold;
        padding: 15px 30px;
        text-transform: uppercase;
    }
    .reset:hover {
        background-color: #1D50F1;
      }
      
      .reset:active {
        background-color: #4d7ef1;
      
      }

      
    ```

#Javascript

```var tableRow = document.getElementsByTagName('tr');
var tableCell = document.getElementsByTagName('td');
var tableSlot = document.querySelectorAll('.slot');
const playerTurn = document.querySelector('.player-turn');
const reset = document.querySelector('.reset');

for(let i = 0; i< tableCell.length; i++){
    tableCell[i].addEventListener('click', (e) => {
    console.log(`${e.target.parentElement.rowIndex}, ${e.target.cellIndex}`);
    })
}

while(!player1){
    var player1 = prompt('Player One: Enter your name. You will be red.');
}

player1Color = 'red';

while(!player2){
    var player2 = prompt('Player Two: Enter your name. You will be black.');
}

player2Color = 'black';

var currentPlayer = 1;
playerTurn.textContent = `${player1}'s turn!`;


Array.prototype.forEach.call(tableCell, (cell) => {
    cell.addEventListener('click', changeColor);
    cell.style.backgroundColor = 'white';
})


function changeColor(e){
    let column = e.target.cellIndex;
    let row = [];

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

function colorMatchCheck(one, two, three, four){
    return(one == two && one === three && one === four && one !=='white');
}

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

function drawCheck(){
    let fullSlot = [];
    for(let i =0; i < tableCell.length; i++){
        if(tableCell[i].style.backgroundColor !== 'white'){
            fullSlot.push(tableCell[i]);
        }
    }
    if (fullSlot.length === tableCell.length){
        return true;
    }
}
}

function togglePopup(){
    document.getElementById("popup-1").classList.toggle("active");
}

reset.addEventListener('click', ()=>{
    tableSlot.forEach(slot =>{
        slot.style.backgroundColor = 'white';
        playerTurn.style.color ='white';

    });
    playerTurn.style.Color = 'black';
    return (currentPlayer ===1 ? playerTurn.textContent = `${player1}'s turn` : playerTurn.textContent = `${player2}'s turn`);
})
```


