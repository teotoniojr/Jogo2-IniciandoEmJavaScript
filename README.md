# Jogo2-IniciandoEmJavaScript Aula 01

Iniciando o seungundo curso de JavaScrip. Recriação do jogo de atravesar a rua do Atari

Nessa primeira aula vimos:

* Como criar variáveis (let);
* carregar imagens 
* function preload(){}
* comando loadImage("nomeDoArquivo.png")
* function background(){}, 
* comando image(variavel, x, y, x.px, y.px));
* movimentar o ator;
* movimentar o carro.

## Instruções

### Carregar as imagens no p5
 
* Para inserir as imagens que farão parte do nosso jogo, é necessário, primeiramente, adicionar os arquivos no p5
* Para isso, ao lado de sketch.js clicamos na flecha ">" e em arquivos do Esboço criamos uma pasta "imagem", para armazenar os arquivos.
* Então, na seta para baixo ao lado da pasta, vamos em "carregar arquivos". Selecionamos as imagens e pronto. Os arquivos agora aparecem no p5.

###  Para carregar a imagem no programa.

* Usamos a função "function preload(){}" para chamar as imagens carregadas no p5.
* Criamos uma variável para a imagem que queremos chamar 
* Então adicionamos a variável da imagem na função e igualamos ao comando "loadImage("localização/imagem.png")"
* Então, para desenhar a imagem na tela, vamos para a função draw e substituimos a cor do comando background(0) pelo nome da nossa variavel.
* Para as outras imagens vamos repetir as 3 primeiras linhas. Mas não colocaremos ela como fundo ("background"), e sim como uma imagem. Para isso, na função draw(){} inserimos o comando image(variavel, x, y, tamanhoX, tamanhoY)


### Organizando em Funções

* Para que nosso código fique com uma estética melhor e mais fácil de vizualizar, usamos as funções para renderizar.
* Podemos criar uma função que mostra o ator e uma que mostra o carro..
* Ex.
 function mostrarAtor(){
  image(imagemDoAtor, 120, 368, 30, 30)
 }
* depois chamamos as funções na função draw()  

### Movimento do carrinho
  
* Como nosso carro está na posição x = 540, podemos movimentalo fazendo uma subtração dessa posição. Podemos colocar nosso carrinho para fora da tela, para que ele faça o movimento. Para isso, criamos uma variavél para a posiçãoX do carrinho "let xCarro". 
* Agora, criamos uma função movimentaCarro(){}
* Adicionamos a operação de subtração na função
* xCarro = xCarro - 2 OU xCarro -= 2
* Trocamos o valor x, na função de mostrar imagem do carro, pela nossa variável "xCarro"

### Movimento do Ator
  
* Para o movimento do ator, precissamos  dar movimento ao eixo y
* Usando a condição If(){}, podemos fazer com que se a tecla da seta para cima estiver precionada subtraia algum número da posição que ela se encontra.
* Para tanto, criamos uma variável para a posição y do Ator "let yAtor = 368". Sendo o 368 o número onde coloquei o meu ator no começo
* Então usamos o comando...
  function movimentarAtor(){
  if(keyIsDown(UP_ARROW))
    yAtor -= 3
* Onde o comando keyIsDown(TECLA) é para sabermos quando a tecla esta precionada.. Podemos ver diferentes teclas usando as referências.. Mas por agora utilizaremos a "tecla para cima" -> "UP_ARROW"
* Assim, subtraimos 3 da posição y do ator quando a tecla está precionada "yAtor -= 3". Quanto maior o número.. Mais rápido o ator andará. Agora, faça o movimento para baixo;
