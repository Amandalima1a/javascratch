// fantasia, aventura, drama

// a viagem de chihiro, LIVRE, fantasia, aventura
// paddington, LIVRE, fantasia, aventura

// as aventuras de pi, 10, drama, fantasia, aventura
// depois da chuva, 10, drama
// guardiões da galáxia, 12, fantasia, aventura
// ladrões de bicicleta, 12, drama
// o menino que descobriu o vento, 14, drama

let campoIdade;
let campoFantasia;

function setup() {
  createCanvas(800, 400);
  createElement("h2", "Recomendador de filmes");
  createSpan("Sua idade:");
  campoIdade = createInput("5");
  campoFantasia = createCheckbox("Gosta de fantasia?");
}

function draw() {
  background("white");
  let idade = campoIdade. value();
  let gostaDeFantasia = campoFantasia.checked();
  let recomendacao = geraRecomendacao(idade, gostaDeFantasia);
  
  fill(color(76,0,115));
  textAlign(CENTER, CENTER);
  textSize(38);
  text(recomendacao, width/2, height/2);
}

function geraRecomendacao(idade, gostaDeFantasia) {
  if(idade >= 10) {
    if(idade >= 14)
      return "o menino que descobriu o vento";
   } else {
     if(idade >= 12) {
       if(gostadeFantasia) {
       return "Homem-aranha: no aranhaverso";
       } else {
       return "Ladrões de bicicleta";   
     }
    if(gostaDeFantasia) {
     return  "as aventuras de pi";
   } else {
        return "Depois da chuva";
      }
     }
  } else {
     if(gostaDeFantasia) {
     return "A viagem de chihiro";
      } else { 
       return "O feitiço do tempo";
     }
   }
