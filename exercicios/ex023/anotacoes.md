Tag: <table></table>
    Para criar uma tabela é necessário usar essa tag!

Tag: <tr></tr>
    Significa "TABLE ROW" (linha de tabela) e serve para criar uma linha da tabela, como o próprio nome já diz!

Tag: <td></td>
    Significa "TABLE DATA" (dado de tabela) e basicamente toda celula preenchida vai receber uma tag td

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