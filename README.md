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


interactive
<!DOCTYPE html>
<html lang="en">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link rel="icon" type="image/png" sizes="32x32" href="./images/favicon-32x32.png">
<link rel="stylesheet" href="style.css">
<title>Interactive rating component</title>


</head>

<body>
<div class="rate" id="rate">
<button id="star"><img src="/images/icon-star.svg" alt=""></button>
<h2>How did we do?</h2>
<p>Please let us know how we did with your support request. All feedback is appreciated
      to help us improve our offering!</p>
<div class="ratings">
<button id="one"> 1 </button>
<button id="two"> 2 </button>
<button id="three"> 3 </button>
<button id="four"> 4 </button>
<button id="five"> 5 </button>
</div>
<button id="submit" onclick="submitRating()">SUBMIT</button>
</div>


<div class="thanks hidden" >
<img src="/images/illustration-thank-you.svg" alt="">
<p class="user-rating"> You selected <span id="number-rating">4</span> out of 5</p>
<h1>Thank you!</h1>
<p>We appreciate you taking the time to give a rating. if you ever need more support,don't hesitate to get in touch!
</p>
<button   id="rate-again" onclick="rateAgain()">RATE AGAIN</button>
</div>
<script src="index.js"></script>
</body>
</html>

 js
 const one = document.getElementById('one');
const two = document.getElementById('two');
const three = document.getElementById('three');
const four = document.getElementById('four');
const five = document.getElementById('five');
const numberRating = document.getElementById('number-rating');
const rateCard=document.querySelector('.rate');
const thanksCard=document.querySelector('.thanks');


 function submitRating()
{
thanksCard.classList.remove('hidden');

rateCard.classList.add('hidden')
}
function rateAgain()
{
thanksCard.classList.add('hidden');
rateCard.classList.remove('hidden')
}

one.addEventListener('click', () => {
numberRating.innerHTML = 1;
})
two.addEventListener('click', () => {
numberRating.innerText = 2;
})
three.addEventListener('click', () => {
numberRating.innerText = 3;
})
four.addEventListener('click', () => {
numberRating.innerText = 4;
})
five.addEventListener('click', () => {
numberRating.innerText = 5;
})

</html>
css
@import url('https://fonts.googleapis.com/css2?family=Overpass&display=swap');
body{
    display: flex;
    justify-content: center;
    align-items: center;

    background-color: hsl(216, 12%, 8%);
    color: hsl(0, 0%, 100%);
    font-family: 'Overpass', sans-serif;
    height: 100vh;
}
.rate{
    max-height: 50vh;
background-color:hsl(214, 21%, 15%);
padding:2em;
width:25%;
height: 48vh;
border-radius: 20px;

}
p{
    color: hsl(217, 12%, 63%);
    font-weight: 800;
    font-size: 0.9em;
}
#submit{

color:inherit;
    font-family: inherit;
    font-weight: 800;
    width:100%;
background-color:hsl(25, 97%, 53%) ;
    border-radius: 20px;
border:none;
    padding:0.8em 0.8em;
    letter-spacing: 4px;
    margin-top:1em;
    cursor: pointer;
}
#submit:hover{
    font-weight: 800;
    background-color: white;
    color: hsl(25, 97%, 53%) ;
    border: 2px solid hsl(25, 97%, 53%);
}

.ratings{
    margin:1em 0;
display:flex;
    justify-content: space-between;
}
.ratings button{
    padding:0.8em;
    border-radius: 50%;
color:hsl(0, 0%, 100%);
background-color:hsl(203, 20%, 23%);
    font-size: 0.9em;
    font-weight: 600;
border:none;
    height:45px;
    width: 45px;
    transition:  1s all ease-in-out;
}
.ratingsbutton:hover{
background-color:hsl(203, 14%, 33%) ;
}
.ratingsbutton:focus{
background-color:hsl(25, 97%, 53%) ;
}
#star{
    border-radius: 50%;
    background-color: hsl(203, 20%, 23%);
    height:45px;
    width: 45px;
    border: none;

}
.thanks{
    max-height: 50vh;
background-color:hsl(214, 21%, 15%);
    padding:3em;
    width:25%;
    height: 50vh;
    border-radius: 20px;
    text-align: center;

}
#rate-again{

color:inherit;
    font-family: inherit;
    font-weight: 800;
    width:100%;
background-color:hsl(25, 97%, 53%) ;
    border-radius: 20px;
border:none;
    padding:0.8em 0.8em;
    letter-spacing: 4px;
    cursor: pointer;
    margin-bottom:0.8em;
}
#rate-again:hover{
    font-weight: 800;
    background-color: white;
    color: hsl(25, 97%, 53%) ;
    border: 2px solid hsl(25, 97%, 53%);
}

.hidden{
    display: none;
}
.user-rating{
color:hsl(25, 97%, 53%) ;
background-color:hsl(203, 20%, 23%) ;
    border-radius: 20px;
    padding: 0.4em;
    width:50%;
    margin:1em auto;
}

@media screen  and (max-width:768px){
.rate{
        width:100%;

    }
.thanks{
        width:100%;

    }
}
@media screen  and (max-width:1068px){
.rate{
        width:70%;

    }
.thanks{
        width:70%;

    }
}
