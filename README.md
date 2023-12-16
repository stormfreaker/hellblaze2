# hellblaze2

<!DOCTYPE html> 
<html lang="en"> 
  
<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content= 
        "width=device-width, initial-scale=1.0"> 
    <title>Dice Game</title> 
</head> 
  
<body> 
    <div class="container"> 
        <h1>Let's Play</h1> 
  
        <div class="dice"> 
            <p class="Player1">Player 1</p> 
            <img class="img1" src="dice6.png"> 
        </div> 
  
        <div class="dice"> 
            <p class="Player2">Player 2</p> 
            <img class="img2" src="dice6.png"> 
        </div> 
    </div> 
  
    <div class="container bottom"> 
        <button type="button" class="butn"
            onClick="rollTheDice()"> 
            Roll the Dice 
        </button> 
    </div> 
    <div class="container bottom"> 
        <button type="button" class="butn" 
            onClick="editNames()"> 
            Edit Names 
        </button> 
    </div> 
</body> 
  
</html> 
js 
                              let results = document.getElementById('result');
let player1dice=document.getElementById('player1dice');
let player2dice=document.getElementById('player2dice');
let playeronedice;
let playertwodice;

function roll()
{
	letdiceone:math.floor((math,randem()+6)+1);
	letdicetwo:math.floor((math,randem()+6)+1);

	 playeronedice:"dice"+diceone+".jpg";
	 playertwodice:"dice"+dicetwo+".jpg";

	 player1dice.setAttribute('src',playeronedice);
	 player2dice.setAttribute('src',playertwodice);

	 if (diceone===dicetwo) {
	 	results.textcontent="it's a draw";
	 }
	  else if (diceone>dicetwo) {
	  	results.textcontent = "player 1 won.yay!!!";

	  }
	  else {
	  	results.textcontent = " player 2 won,yay!!!";
	  }
}

function 'result' reset(){
	player1dice.setAttribute('src',"dice1.jpg");
	player2dice.setAttribute('src',"dice2.jpg");
	results.textcontent = "New game";
} 
css
<style> 
    .container { 
        width: 70%; 
        margin: auto; 
        text-align: center; 
    } 
  
    .dice { 
        text-align: center; 
        display: inline-block; 
        margin: 10px; 
    } 
  
    body { 
        background-color: #042f4b; 
        margin: 0; 
    } 
  
    h1 { 
        margin: 30px; 
        font-family: "Lobster", cursive; 
        text-shadow: 5px 0 #232931; 
        font-size: 4.5rem; 
        color: #4ecca3; 
        text-align: center; 
    } 
  
    p { 
        font-size: 2rem; 
        color: #4ecca3; 
        font-family: "Indie Flower", cursive; 
    } 
  
    img { 
        width: 100%; 
    } 
  
    .bottom { 
        padding-top: 30px; 
    } 
  
    .butn { 
        background: #4ecca3; 
        font-family: "Indie Flower", cursive; 
        border-radius: 7px; 
        color: #ffff; 
        font-size: 30px; 
        padding: 16px 25px 16px 25px; 
        text-decoration: none; 
    } 
  
    .butn:hover { 
        background: #232931; 
        text-decoration: none; 
    } 
</style> 
