# jogo--nave
jogo de nave , relembrando bons momentos de diversão 

//////// Código HTML ///////

 <! DOCTYPE html>
<html lang="pt-br">
<cabeça>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="css/estilos.css" rel="stylesheet" tipo="text/css">
    <título>Resgate</título>
</cabeça>
<corpo>
    <div id="container"> <!-- !--> de contêiner div
        <div id="fundoGame"> <!-- div fundoGame !-->
        
            <div id="inicio" onclick="start()"><h1> Resgate </h1> 
            <p>Utilize a tecla W para movimentar o helicóptero para cima, a tecla S para movimentar o helicóptero para baixo e a tecla D para atirar. </p>
            <p> Clique aqui para iniciar!! </p>
            </div> 
            
        </div>
 
 </div> <!-- !--> 

    <!-- Sons do jogo !-->
    <audio src="sons/som.mp3" preload="auto" id="somDisparo"></audio>
    <audio src="sons/explosao.mp3" preload="auto" id="somExplosao"></audio>
    <audio src="sons/musica_fundo.mp3" preload="auto" id="musica"></audio>
    <audio src="sons/gameover.mp3" preload="auto" id="somGameover"></audio>
    <audio src="sons/perdido.mp3" preload="auto" id="somPerdido"></audio>	
    <audio src="sons/resgate.mp3" preload="auto" id="somResgate"></audio>

    !--> de roteiro <!--
 <script tipo="texto/javascript" src="js/jquery-1.11.1.min.js"></script>
 <script tipo="texto/javascript" src="js/js.js"></script> 
 <script tipo="text/javascript" src="js/jquery-collision.min.js"></script>
 
 
 ////// Código CSS /////
 
 @font-face {
	font-family:Titulo;
	src:url(.. /fontes/ANODETONOONA. TTF);
}
h1 {
	font-family:Titulo;
	tamanho da fonte:40px;
	cor:#603A03;
}
corpo {
	imagem de fundo:url(.. /imgs/fundo.jpg);
}
#recipiente{
	largura:950px;
	altura:auto;
	posição:relativo;
	margem-esquerda:auto;
	margem-direita:auto;
}
#fundoGame {
	largura:950px;
	altura:630px;
	imagem de fundo:url(.. /imgs/fundo_game.jpg);
	cor da borda:#FFF;
	estilo de fronteira:sólido;
}
#jogador {
	largura:256px;
	altura:66px;
	posição:absoluto;
	esquerda:8px;
	topo:179px;
    imagem de fundo:url(.. /imgs/apache.png);
}
#inimigo1 {
	largura: 256px;
	altura: 66px;
	posição: absoluta;
	esquerda: 689px;
	topo: 253px;
	imagem de fundo:url(.. /imgs/inimigo1.png);
	
}
#inimigo2 {
	largura: 165px;
	altura: 70px;
	posição: absoluta;
	esquerda: 775px;
	topo: 447px;
	imagem de fundo: url(.. /imgs/inimigo2.png);
}
#amigo {
	largura: 44px;
	altura: 51px;
	posição: absoluta;
	esquerda: 10px;
	topo: 464px;
	imagem de fundo:url(.. /imgs/amigo.png);
}
#inicio {
	largura:350px;
	altura:200px;
	cor de fundo:#FFF;
 	margem-esquerda:auto;
    margem-direita:auto;
 	margem-topo:100px;
	alinhamento de texto:centro;
	preenchimento:10px;
}
. anima1 {
	imagem de fundo:url(.. /imgs/helicoptero.png);
	animação:reproduzir passos .5s(2) infinitos;
       -webkit-animação: reproduzir passos .5s(2) infinito;
       -moz-animation: reprodução passos .5s(2) infinito;
       -ms-animação: reproduzir passos .5s(2) infinitos;
       -o-animação: reproduzir passos .5s(2) infinitos;
}
@keyframes jogo {
	de {posição de fundo:0px;}
	para {posição de fundo:-512px;}
}
@-webkit-keyframes reprodução {
	de { posição de fundo:0px; }
	  para { posição de fundo: -512px; }
 }
 
 @-moz-keyframes play {
	de { posição de fundo:0px; }
	  para { posição de fundo: -512px; }
 }
 
 @-ms-keyframes play {
	de { posição de fundo:0px; }
	  para { posição de fundo: -512px; }
 }
 
 @-o-keyframes play {
	de { posição de fundo:0px; }
	  para { posição de fundo: -512px; }
 }
 . anima2 {
    imagem de fundo:url(.. /imgs/inimigo1.png);
    animação: reproduzir passos .5s(2) infinitos;
    -webkit-animação: reproduzir passos .5s(2) infinito;
	   -moz-animation: reprodução passos .5s(2) infinito;
		-ms-animação: reproduzir passos .5s(2) infinitos;
		 -o-animação: reproduzir passos .5s(2) infinitos; 
}
. anima3 {
	imagem de fundo:url(.. /imgs/amigo.png);
	animação:passos play2 .9s(12) infinitos;
	-webkit-animação: passos play2 .9s(12) infinitos;
       -moz-animação: passos play2 .9s(12) infinitos;
        -ms-animation: passos play2 .9s(12) infinitos;
         -o-animação: passos play2 .9s(12) infinitos;
}
@keyframes play2 {
	de {posição de fundo:0px;}
	para {posição de fundo:-528px;}
}
@-webkit-keyframes play2 {
   de { posição de fundo: 0px; }
     para { posição de fundo: -528px; }
}
@-moz-keyframes play2 {
   de { posição de fundo: 0px; }
     para { posição de fundo: -528px; }
}
@-ms-keyframes play2 {
   de { posição de fundo: 0px; }
     para { posição de fundo: -528px; }
}
@-o-keyframes play2 {
   de { posição de fundo: 0px; }
     para { posição de fundo: -528px; }
}
#disparo {
	largura: 50px;
	altura: 8px;
	posição: absoluta;
	imagem de fundo: url(.. /imgs/disparo.png);
}
#explosao1 {
	largura:15px;
	altura:87px;
	posição:absoluto;
}
#explosao2 {
	largura:15px;
	altura:87px;
	posição:absoluto; 
}
#explosao3 {
	largura:44px;
	altura:51px;
	posição:absoluto;
}
. anima4 {
	largura:44px;
	altura:51px;
	imagem de fundo:url(.. /imgs/amigo_explosao.png);
	animação:play3 passos .5s(7) infinito;
	-webkit-animação: passos play3 .5s(7) infinitos;
       -moz-animação: passos play3 .5s(7) infinitos;
        -ms-animação: passos play3 .5s(7) infinitos;
         -o-animação: passos play3 .5s(7) infinitos;
}
@keyframes play3 {
	de {posição de fundo:0px;}
	para {posição de fundo:-308px;}
}
@-webkit-keyframes play3 {
   de { posição de fundo: 0px; }
     para { posição de fundo: -308px; }
}
@-moz-keyframes play3 {
   de { posição de fundo: 0px; }
     para { posição de fundo: -308px; }
}
@-ms-keyframes play3 {
   de { posição de fundo: 0px; }
     para { posição de fundo: -308px; }
}
@-o-keyframes play3 {
   de { posição de fundo: 0px; }
     para { posição de fundo: -308px; }
}
#placar {
	largura: 450px;
	altura: 50px;
	posição: absoluta;
	esquerda: 5px;
	topo: 590px;
}
h2 {
	font-family:Titulo;
	tamanho da fonte:20px;
	cor:#FFF
}
#energia {
	largura: 140px;
	altura: 38px;
 posição: absoluta;
 esquerda: 750px;
 topo: 7px; 
}

h3 {
	font-family:Titulo;
 tamanho da fonte:20px;
 cor:#603A03;
}

#fim {
 largura:350px;
 altura:200px;
 cor de fundo:#FFF;
 margem-esquerda:auto;
 margem-direita:auto;
 margem-superior:100px;
 alinhamento de texto:centro;
 preenchimento:10px;
}
 
 //// Código Javascript /////

início da função() { 
	$("#inicio"). esconder();
	
	$("#fundoGame"). apêndice("<div id='jogador' class='anima1'class='anima1'></div>");
	$("#fundoGame"). apêndice ("<div id='inimigo1' class='anima2'></div>");
	$("#fundoGame"). apêndice ("<div id='inimigo2'></div>");
	$("#fundoGame"). apêndice ("<div id='amigo' class='anima3'></div>");
	$("#fundoGame"). apêndice ("<div id='></div>");
	$("#fundoGame"). apêndice ("<div id='energia'></div>");
	Principais variáveis do jogo
	var podeAtirar=true;
	var fimdejogo=falso;
	var pontos=0;
	var salvos=0;
	var perdidos=0;
	var energiaAtual=3;
	var jogo = {};
	var velocidade=4;
	var posicaoY = parseInt(Matemática. aleatório() * 334);
	var TECLA = {
		W: 87,
		S: 83,
		D: 68
	}

 jogo. pressionou = [];

 var somDisparo=documento. getElementById ("somDisparo");
 var somExplosao=documento. getElementById("somExplosao");
 var musica=documento. getElementById("musica");
 var somGameover=documento. getElementById("somGameover");
 var somPerdido=documento. getElementById("somPerdido");
 var somResgate=documento. getElementById ("somResgate");

	Música em loop
 musica. addEventListener("acabado", função(){ musica. atualTime = 0; musica. jogar(); }, falso);
 musica. jogo();

	Verifica se o usuário pressionou alguma tecla 
 $(documento). keydown(função(e){
 jogo. pressionou[e. que] = verdadeiro;
@@ -113,7 +124,9 @@ function start() { // Inicio da função start()
		}
	} fim da função moveamigo()

	Função disparo
 função disparo() {
 SomDisparo. jogo();
 se (podeAtirar==true) {
 podeAtirar=falso;

@@ -141,6 +154,7 @@ function start() { // Inicio da função start()
		} Fecha executaDisparo()
	} Fecha disparo()

	Função colisão
 colisão de função() {
 var colisao1 = ($("#jogador"). colisão ($("#inimigo1"));
 var colisao2 = ($("#jogador"). colisão($("#inimigo2));
@@ -204,6 +218,7 @@ function start() { // Inicio da função start()
		jogador com o amigo
 se (colisao5. comprimento>0) {
			salvos++;
 somResgate. jogo();
			reposicionaAmigo();
 $("#amigo"). remover();
		}
@@ -223,6 +238,7 @@ function start() { // Inicio da função start()

	Explosão 1
 função explosao1(inimigo1X,inimigo1Y) {
 somExplosao. jogo();
 $("#fundoGame"). apêndice ("<div='explosao1'></div");
 $("#explosao1"). css("imagem de fundo", "url(imgs/explosao.png)";
		var div=$("#explosao1");
@@ -255,7 +271,7 @@ function start() { // Inicio da função start()

	Explosão2
 função explosao2 (inimigo2X,inimigo2Y) {

  somExplosao. jogo();
 $("#fundoGame"). apêndice ("<div='explosao2'></div");
 $("#explosao2"). css("imagem de fundo", "url(imgs/explosao.png)";
		var div2=$("#explosao2");
@@ -288,6 +304,7 @@ function start() { // Inicio da função start()

	Explosão3 
 função explosao3 (amigoX,amigoY) {
 somPerdido. jogo();
 $("#fundoGame"). apêndice ("<div='explosao3' class='anima4'></div");
 $("#explosao3"). css("imagem de fundo", "url(imgs/amigo_morte.png)") ;
		var div3=$("#explosao3");
@@ -307,30 +324,50 @@ function start() { // Inicio da função start()
	} placar fim da função()

	Barra de energia
função energia() {

 se (energiaAtual==3) {
 função energia() {

 $("#energia"). css("imagem de fundo", "url(imgs/energia3.png)";
	}
 se (energiaAtual==3) {

 $("#energia"). css("imagem de fundo", "url(imgs/energia3.png)";
		}

 se (energiaAtual==2) {

 $("#energia"). css("imagem de fundo", "url(imgs/energia2.png)";
	}
  se (energiaAtual==2) {
			
  $("#energia"). css("imagem de fundo", "url(imgs/energia2.png)";
		}

 se (energiaAtual==1) {

 $("#energia"). css("imagem de fundo", "url(imgs/energia1.png)";
	}
 se (energiaAtual==1) {

 $("#energia"). css("imagem de fundo", "url(imgs/energia1.png)";
		}

 se (energiaAtual==0) {

 $("#energia"). css("imagem de fundo", "url(imgs/energia0.png)";

			Fim de jogo
			gameOver();
		}

	} Fim da função energia

 se (energiaAtual==0) {
	Jogo de função acabou
  jogo de funçãoOver() {
		fimdejogo=true;
 musica. pausa();
 somGameover. jogo();

 $("#energia"). css("imagem de fundo", "url(imgs/energia0.png)";
 janela. clearInterval (jogo. temporizador);
 jogo. timer=null;

		Fim de jogo
	}

} Fim da função energia
 $("#jogador"). remover();
 $("#inimigo1"). remover();
 $("#inimigo2"). remover();
 $("#amigo"). remover();

 $("#fundoGame"). apêndice ("<div id='fim'></div>");

 $("#fim"). html("<h1> Jogo sobre </h1><p>Sua pontuação foi: " + pontos + "</p>" + "< idiv id='reinicia' onClick=reiniciaJogo()><h3>Jogar Novo</h3></div>");
	} Fim da função gameOver();

}
 
 
