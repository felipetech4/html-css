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

    background-position -> define a posição do fundo da imagem, aceita 9 valores: 
        esquerda em cima / left top; 
        esquerda no centro / left center;
        esquerda em baixo / left bottom;
        centralizado em cima / center top;
        centro no centro / center center;
        centro em baixo / center bottom;
        direita em cima / right top;
        direita no centro / right center;
        direita em baixo / right bottom;

IMPORTANTE -> Quando o navegador não aceitar o comando do background-position, observar a altura do seletor. Normalmente é necessario utilizar uma declaração de height com um valor de altura em vh (tamanho da viewport (tela)) ex:
    height: 100vh; -> esta declarando que vai ocupar 98% da tela (viewport). -> ESSA DECLARAÇÃO VAI SER NECESSÁRIA NA MAIORIA DAS VEZES.
    Depois dessa declaração eu posso acrescentar um:
        background-repeat: no-repeat;
        background-size: 100%;
    Isso vai fazer com que a imagem de fundo fique ocupando 100% da tela de qualquer dispositivo e com a imagem única, sem repetição (para essa declaração funcionar é necessária a declaração de ''height: 100vh;'' também).
    OBS -> No entanto essa tecnica de deixar o fundo totalmente preenchido sem repetições, não é a mais correta, pois ela deixa a imagem distorcida.

    Para isso existe uma outra tecnica: manter a declaração 'height: 100vh;', remover a declaração 'background-repeat: no-repeat; (essa parte de remover é opcional)' e alterar somente o valor da declaração 'background-size: 100%;' para um novo valor:

        background-size: cover;

    OBS -> É necessário escolher a posição do fundo com a propriedade 'background-position;'.

    OBS -> Essa tecnica é melhor do que a primeira, porém nenhuma das duas são ideais, pois elas não preenchem o fundo de sites mais longos com apenas uma imagem sem repetição.

    Para deixar o fundo de tela fixo eu uso uma declaração:
        background-attachment: fixed;

        Esse background-attachment já vem com um padrão pre configurado:
            background-attachment: scroll; -> Por esse motivo o fundo rola junto com o conteudo por padrão.

    OBS -> O background-attachment: fixed; e o background-size: cover; fazem uma bela dupla!

Para todas essas propriedades existe uma shorthand na seguinte ordem:
    color > image > position > repeat > attachment
    [size] OBS -> o size ainda não está aplicável na shorthand, por isso vou sempre usar background-size separado da shorthand, como no exemplo abaixo:

    background: black url('imagens/wallpaper002.jpg') center center no-repeat fixed;
    background-size: cover;

AGORA UM CONTEÚDO MUITO IMPORTANTE: CENTRALIZAR VERTICALMENTE (o margin: auto; faz a centralização horizontal)
    Para centralizar verticalmente, é sempre necessário seguir alguns passos:
        -> Fazer 2 divs aninhadas
        -> Uma div recebe um id chamado container
        -> A outra div recebe um id chamado conteudo
        -> criar os seletores dessas divs em style (#container e #conteudo)
        -> no seletor container(container vai ser sempre o bloco que estiver fora):
            -> height: 100vh; (ou qualquer outro tamanho em vh)
            -> uma cor para a caixa
            -> position: relative; (essa declaracao pode ser omitida pois ja vem por padrão)

        -> no seletor conteudo (conteudo sempre vai ser a div que está aninhada/dentro da outra div):
            -> height: 50%; (ou qualquer outro valor em px ou %)
            -> width: 50%; (ou qualquer outro valor em px ou %)
            -> uma cor para a caixa
            -> position: absolute; (quando eu coloco esse posicionamento absoluto eu ganho autoridade para editar duas propriedades muito importante: left e top)
            -> left: 50%; (a distancia lado esquerdo do seletor #conteudo para a borda esquerda do seletor que esta por fora/#container)
            -> top: 50%; (a distancia de cima do seletor #conteudo para a borda de cima do seletor que esta por fora/#container)
                OBS -> essas duas propriedades também aceitam valores em px;
                OBS -> Nesse caso de valores em 50%, a div aninhada vai ficar centralizada, porém o que vai estar exatamente no centro será o canto superior esquerdo dessa div, pois se eu observar é exatamente o que eu coloquei, o left e o top em 50% da div container.
                Para resolver esse problema e deixar a div exatamente centralizada, eu uso mais uma declaração:
            -> transform: translate(-50% -50%); (o transform me permite mexer na caixa/box, aplicanto alguma transformação nela / o translate movimenta a caixa em 2 posicoes: esquerda/direita (com o sinal de - e um valor em px ou % ele vai para esquerda / com um valor "sem sinal ou com sinal +" em px ou % ele vai para direita) cima/baixo (com o sinal de - e um valor em px ou % ele vai para cima / com um valor "sem sinal ou com sinal +" em px ou % ele vai para baixo)

