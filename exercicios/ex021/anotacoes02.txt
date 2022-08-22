Existem as Grouping Tags Não Semânticas (antigas, que não tem semântica):
    div
    span
E existem as novas Grouping Tags Semânticas (que são vistas como div porém possuem semântica e ajudam o navegador de busca):
    header -> Cabeçalho (OBS -> NÃO CONFUNDIR COM AS CONFIGURAÇÕES DO SITE (head/cabeça))

    main -> Conteúdo principal do site

    footer -> Rodapé

    nav -> Menu de Navegação / Links

    section -> Seção (uma parte do conteúdo que contém outras partes, ex: como as salas de cinema) OBS -> Nas sections é necessário o uso do id especificando o nome da seção dentro da tag

    article -> Artigo

    aside -> Conteúdo Relativo ao Artigo, como se fosse uma complementação

        OBS -> Todas essas tags não possuem ordem de organização, eu que escolho aonde elas vão ficar, quem vai ficar dentro de quem, quem vem primeiro ou depois, tudo é o desenvolvedor que escolhe com a necessidade do site.

        Com isso eu consigo trabalhar em CSS com os seletores dessas tags e personalizar partes bem mais específicas do conteúdo, que agora tem semântica/faz sentido para o navegador.

Em CSS toda tag que tiver dentro de outra tag eu coloco no seletor primeiro a tag mãe, depois > e depois a tag filho e abro os colchetes do seletor normalmente, isso indica somente as tags com o nome da tag filho dentro da tag mãe serão personalizadas.

