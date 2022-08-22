OBS-> Quando não tenho um link para minha tag de âncora (a), eu uso # dentro do valor de href (isso é uma boa prática)
    ex:
        <a href="#">exemplo de boa prática do link sem caminho</a>

IMPORTANTE -> user agent é sempre o navegador que ta exibindo o conteúdo

    Propriedade:
        border-width: largura da borda; (em px)

        border-style: estilo da borda; (alguns valores: solid (preenchido) dashed (pontilhado) dotted (pontilhado) double (linha dupla) groove (3d))

        border-color: cor da borda;

A medida do padding é dividida em 4 partes:
    padding-top: medida de cima px
    padding-right: medida da direita px
    padding-bottom: medida de baixo px
    padding-left: medida da esquerda px

    OBS -> É uma boa prática seguir essa ordem em sentido horário ao indicar as partes da padding -> cima direita baixo esquerda

A medida da margin funciona da mesma forma que o padding:
    margin-top: px;
    margin-right: px;
    margin-bottom: px;
    margin-left: px;

    LEMBRAR DE USAR O SENTIDO HORÁRIO

    Para deixar a margin centralizada, usamos:
        margin: auto  (lembrando que essa centralização é usada para caixas. Para texto eu uso text-align: center;)

A medida do outline funciona da mesma forma que o border:
    outline-width: px;
    outline-style: ;
    outline-color: ;


LEMBRANDO:
    height e width (box size) -> altura e largura da caixa

    Propriedades anatômicas da caixa:
    margin -> margem da caixa
    border -> borda da caixa
    outline -> contorno da borda, entre a border e a margin
    padding -> preenchimento do elemento

IMPORTANTÍSSIMO: Podemos abreviar as Propriedades de margin, border, outline, e padding com shorthands:
    Shorthand de border:
        border: largura(px) estilo cor;

    Shorthand de padding:
        padding: cima px direita px baixo px esquerda px; OBS -> Se as 4 medidas forem iguais, basta informar uma só. Se as medidas de cima e de baixo forem iguais, e dos 2 lados forem iguais, eu coloco só 2 valores.

        Se eu quiser centralizar somente um lado, uso o valor -> auto; no lado que quero centralizar

    Shorthand de margin:
        margin: cima px direita px baixo px esquerda px; OBS -> Se as 4 medidas forem iguais, basta informar uma só. Se as medidas de cima e de baixo forem iguais, e dos 2 lados forem iguais, eu coloco só 2 valores.

        Se eu quiser centralizar somente um lado, uso o valor -> auto; no lado que quero centralizar

    Shortline de outline:
        border: largura(px) estilo cor;

OBS: Para transformar em box-level uso a Declaração:
        display: block;

    Para transformar em inline-level:
        display: inline;

    Quando eu uso inline eu não declaro altura e largura.

A propriedade display, muda a característica padrão de um elemento.

