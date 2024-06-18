# domenico-pong

let xBolinha = 300;
let yBolinha = 200;
let diametro = 30;
let raio = diametro / 2;

let velocidadeXBolinha = 6;
let velocidadeYBolinha = 6;

function setup() {
    createCanvas(500, 300);
}

function draw() {
    background("#FF69B4");
    mostraBolinha();
    movimentaBolinha();
    verificaColisaoBorda();
  rect(5, 150, 10, 90);
}

function mostraBolinha() {
    circle(xBolinha, yBolinha, diametro)
}

function movimentaBolinha() {
    xBolinha += velocidadeXBolinha;
    yBolinha += velocidadeYBolinha;
}

function verificaColisaoBorda() {
    if (xBolinha + raio > width || xBolinha - raio < 0) {
    velocidadeXBolinha *= -1;
}
if (yBolinha + raio > height || yBolinha - raio < 0) {
    velocidadeYBolinha *= -1;
}
}
