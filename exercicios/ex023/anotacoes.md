Tag: <table></table>
    Para criar uma tabela é necessário usar essa tag!

Tag: <caption></caption>
    É usada para adicionar uma legenda a tabela (para ser mais claro é o título da tabela)
    Dentro dessa tag não adiciono nenhuma outra tag, somente o texto (sem parágrafo).

Tag: <tr></tr>
    Significa "TABLE ROW" (linha de tabela) e serve para criar uma linha da tabela, como o próprio nome já diz!

Tag: <td></td>
    Significa "TABLE DATA" (dado de tabela) e basicamente toda celula preenchida com um dado (uma informação) vai receber uma tag td

Tag: <th></th>
    Significa "CABEÇALHO DA TABELA" é usada para adicionar o título da coluna ou da linha.
    É EXTREMAMENTE NECESSÁRIO USAR ESCOPOS ESPECÍFICOS NA TAG TH:
        No caso de título da coluna, se usa:
            <th scope="col"></th>
        No caso de título da linha, se usa:
            <th scope="row"></th>
        Esses atributos não mudam em nada visualmente, no entanto tem uma enorme importância na semântica do conteúdo.

OBS -> A hierarquia das tabelas DEVE ser obedecida, conforme a ordem das tags acima... Caso contrário o conteúdo irá aparecer ou antes ou depois da tabela.

ORDEM:  Dentro da table eu tenho tr e dentro da tr eu tenho td

Propriedade CSS: 
    border-collapse:
        2 valores mais usados:
            separate; -> deixa as bordas separadas uma das outras em ralação a outras caixas
            collapse; -> deixa as bordas unidas uma nas outras em ralação a outras caixas

ALINHAMENTO:
    Propriedade CSS:
        text-align: left/center/right;   -> para alinhar um elemento da tabela de forma horizontal

    Propriedade CSS:
        vertical-align: top/middle/bottom;  -> para alinhar células de uma tabela de forma vertical

ANATOMIA PARA TABELAS GRANDES:
    Primeiro:
        Tag: <table></table>
            Significa que será usado uma tabela dentro dessa tag. 

    Segundo:         
        Tag: <thead></thead>
            Significa que essa parte é a cabeça da tabela.
            É usado dentro do table
            Aceita as tags <tr> <td> e <th>

    Terceiro:
        Tag: <tbody></tbody>
            Siginifica que essa parte é o corpo da tabela.
            É usado dentro do table
            Aceita as tags <tr> <td> e <th>

    Quarto:
        Tag: <tfoot></tfoot>
            Significa que essa parte é o pé da tabela
            É usado dentro do table
            Aceita as tags <tr> <td> e <th>

LARGURA DE COLUNAS:
    Propriedade CSS:
        width: px;
    Essa declaração é usada normalmente com style inline/estilo pontual (aplicando o estilo dentro da tag específica)

Pseudo Classe CSS:
    :nth-child() 
        -> É usado para definir uma sequência de estilo nas linhas da tabela
        -> Dentro dos parenteses eu escolho a opção de sequências a ser seguida, alguns dos possiveis valores de dentro dos parenteses são:
            :nth-child(odd) -> Todas as linhas de número ÍMPAR serão selecionadas
            :nth-child(even) -> Todas as linhas de número PAR serão selecionadas
            :nth-child(2n-1) -> Causa o mesmo resultado do odd
            :nth-child(2n) -> Causa o mesmo resultado do even
            :nth-child(5n) -> Vai selecionar uma a cada 5 linhas OBS -> Esse exemplo foi usado com o número 5, mas posso usar qualquer outra valor e as linhas tabela serão selecionadas de acordo com esse valor.

        -> Depois de escolher a ordem da sequência, basta abrir os colchetes do seletor e personalizá-lo.

Fixar Cabeçalho em tabelas grandes:
    Para deixar o cabeçalho fixado ao rolar a tela, eu tenho que seguir 2 passos:
        1 - No seletor table, adicionar:
            position: relative;

        2 - Criar um seletor:
             thead > tr > th {
                    position: sticky;
                    top: -1px;

                            }


Mesclagem de células HTML:
    Para fazer uma mesclagem é necessário expandir a célula desejada
    Para expandir uma célular eu tenho 2 formas diferentes:
        Para linhas eu uso dentro da tag da célula desejada:
            colspan="aqui eu coloco o numero de quantidade de celulas a serem mescladas"
        Para colunas eu uso dentro da tag da célula desejada:
            rowspan="aqui eu coloco o numero de quantidade de celulas a serem mescladas"

Mais sobre ESCOPO:
    Quando eu uso os títulos de tabela (th) eu preciso adcionar uma semântica em cada th
        No caso de título de uma coluna, se usa:
            <th scope="col"></th>
        Caso haja mais de uma coluna para o mesmo título , se usa:
            <th scope="colgroup"></th>
        No caso de título de uma linha, se usa:
            <th scope="row"></th>
        Caso haja mais de uma linha para o mesmo título , se usa:
            <th scope="rowgroup"></th>

Para personalizar uma coluna inteira, eu uso uma tag específica:
    <colgroup>
        <col class="nome1">   OBS -> col não tem fechamento
        <col class="nome2">
    </colgroup>
        OBS -> Essa tag é usada dentro da tag TABLE e eu posso usar quantas col for necessário
            Depois é só criar o seletor em style e dar o estilo desejado

