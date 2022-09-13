Propriedade:
    background-color -> define um valor de uma cor só para o fundo
    background-image -> define valores com mais de uma cor (em gradiente), e também pode definir valores de url:

        linear-gradient(to bottom, green, transparent) -> Esse valor tras uma cor gradiente começando verde em cima, até transparente em baixo.

        url('https://gustavoguanabara.github.io/html-css/imagens/mascote.png') -> esse valor trás uma URL de uma imagem não baixada na máquina local, simplesmente da internet.

        url('imagens/wallpaper004.jpg') -> Esse valor trás uma URL, porém de uma imagem já baixada e já na pasta imagens do projeto

    background-size -> define o tamanho da imagem do background OBS -> Alternando o tamanho da tela, o tamanho da imagem não é alterada.

    background-repeat -> define se a imagem vai se repetir ou não, e de que local ela vai começar. Existem 4 possíveis valores:
        repeat -> ele repete até preencher a tela inteira
        no-repeat -> ele reproduz a imagem somente uma vez
        repeat-x -> ele repete a imagem somente horizontalmente até o final de uma linha somente
        repeat-y -> ele repete a imagem somente verticalmente até o final de uma coluna somente
        OBS -> Por padrão irá sempre começar com o repeat, e sempre pelo canto superior esquerdo.

    