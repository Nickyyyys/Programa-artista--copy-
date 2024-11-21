# Programa-artista--copy-
let xCirculo; //cordenada da horizontal
let yCirculo; //cordenada vertical
let corciculo; //cor inicial dos circulos
let corfundo; //cor do fundo 


function setup() {
  createCanvas(600, 400);
  xCirculo = [0, 0, 0];
  yCirculo = [random(height),                                random(height), random(height)];
  corcirculo = color(random(0, 255),random(0, 255),random(0,255));
  corfundo = color(random(0, 255),random(0, 255),random(0,255));
  background(corfundo);
}

function draw() {
  fill(corcirculo);
  
  for (let contador in xCirculo) {
    circle(xCirculo[contador], yCirculo [contador], 50);
    xCirculo[contador] += random(0, 3);
    yCirculo [contador] += random(-5, 5);
    
    if (xCirculo [contador]>width){
      xCirculo[contador] = 0;
    
    }
  } 
}
    
