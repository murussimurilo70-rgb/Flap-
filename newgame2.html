<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Flappy Plane FULL</title>
<style>
body {
  margin: 0;
  background: skyblue;
  overflow: hidden;
  font-family: Arial;
}
canvas {
  display: block;
}

#ui {
  position: fixed;
  top: 10px;
  left: 10px;
  color: white;
  font-size: 24px;
  font-weight: bold;
  text-shadow: 2px 2px 5px black;
}

button {
  padding: 12px 35px;
  font-size: 22px;
  border: none;
  border-radius: 12px;
  color: white;
}

#startBtn {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: red;
}

#resetBtn {
  position: fixed;
  top: 60%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: black;
  display: none;
}
</style>
</head>

<body>

<div id="ui">Score: 0</div>
<button id="startBtn">START</button>
<button id="resetBtn">RESET</button>

<canvas id="game"></canvas>

<script>
const canvas = document.getElementById("game");
const ctx = canvas.getContext("2d");
canvas.width = innerWidth;
canvas.height = innerHeight;

let plane, pipes, frame, score, playing;

// ☁️ NUVENS
let clouds = [];
for(let i=0;i<6;i++){
  clouds.push({x: Math.random()*canvas.width, y: Math.random()*canvas.height, s: Math.random()*2+1});
}

function drawClouds(){
  ctx.fillStyle="white";
  clouds.forEach(c=>{
    ctx.beginPath();
    ctx.arc(c.x, c.y, 20, 0, Math.PI*2);
    ctx.fill();
    c.x -= c.s;
    if(c.x < -40) c.x = canvas.width + 40;
  });
}

// ✈️ AVIÃO
function drawPlane(){
  ctx.fillStyle = "yellow";
  ctx.fillRect(plane.x, plane.y, 40, 15);
  ctx.fillStyle = "red";
  ctx.fillRect(plane.x+10, plane.y-5, 15, 5);
}

// ▶️ START GAME
function startGame(){
  plane = {x: 100, y: canvas.height/2, v: 0};
  pipes = [];
  frame = 0;
  score = 0;
  playing = true;

  document.getElementById("ui").innerText = "Score: 0";
  document.getElementById("startBtn").style.display = "none";
  document.getElementById("resetBtn").style.display = "none";
}

document.getElementById("startBtn").onclick = startGame;
document.getElementById("resetBtn").onclick = startGame;

// TAP / CLICK PARA SUBIR
document.addEventListener("click", ()=>{
  if(playing) plane.v = -10;
});

// 🧱 CANOS
function newPipe(){
  let gap = 180;
  let top = Math.random()*(canvas.height-gap-200)+100;
  pipes.push({x: canvas.width, top: top, scored: false});
}

// 🎮 GAME LOOP
function gameLoop(){
  ctx.clearRect(0,0,canvas.width,canvas.height);
  drawClouds();

  if(!playing){
    requestAnimationFrame(gameLoop);
    return;
  }

  // AVIÃO
  plane.v += 0.6;
  plane.y += plane.v;
  drawPlane();

  // CANOS
  ctx.fillStyle="green";
  pipes.forEach(p=>{
    ctx.fillRect(p.x, 0, 60, p.top);
    ctx.fillRect(p.x, p.top+180, 60, canvas.height);
    p.x -= 3;

    // SCORE
    if(!p.scored && p.x + 60 < plane.x){
      score++;
      p.scored = true;
      document.getElementById("ui").innerText = "Score: " + score;
    }

    // COLISÃO
    if(plane.x < p.x+60 && plane.x+40 > p.x &&
      (plane.y < p.top || plane.y+15 > p.top+180)){
      gameOver();
    }
  });

  // CHÃO / TETO
  if(plane.y > canvas.height || plane.y < 0){
    gameOver();
  }

  if(frame % 120 == 0) newPipe();
  frame++;

  requestAnimationFrame(gameLoop);
}

// 💀 GAME OVER
function gameOver(){
  playing = false;
  document.getElementById("resetBtn").style.display = "block";
}

gameLoop();
</script>

</body>
</html>
