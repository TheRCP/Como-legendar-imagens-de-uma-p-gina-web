## Como legendar imagens de uma página web

### Introdução

A colocação de legendas em imagens, vulgarmente conhecida por "alt text" é seguramente das regras com maior notoriedade no campo da acessibilidade web. Ela é, no entanto, também uma das regras mais violadas nos sítios web. A sua implementação técnica não tem grande coisa para se explicar, mas o seu impacto em termos de acessibilidade é elevado. O não cumprimento desta regra de acessibilidade faz com que muitos utilizadores se confrontem com uma **barreira intransponível**. Estão nesse campo todos os utilizadores de software de leitura de ecrã e todos os que, por um qualquer motivo, necessitem de utilizar navegadores de base texto.

A técnica resume-se a:

> coloque a legenda no atributo `alt` de **todos** os elementos `<img>` existentes na página.

Talvez nesta frase haja que sublinhar "**todos**", porque na verdade todas as imagens precisam do seu alternativo textual. O texto alternativo nas imagens serve um infindável número de utilizadores, incluíndo aqui os que utilizam motores de busca e softwares de indexação. Também estes, como sucede com as pessoas cegas, navegam na página sem recorrer ao sentido da visão. Dito desta forma parece ser fácil compreender que aquilo que pretendemos como resultado final é que os utilizadores compreendam o conteúdo da página quer consigam visualizar, ou não, as imagens.

É importante também compreender que a não colocação de imagens no sítio web é também uma violação das diretrizes de acessibilidade. No seu ponto de verificação 14.2, é possível ler: "Reforce a mensagem texto através de gráficos e/ou áudio na medida em que os mesmos facilitem a compreensão da página". Assim, a versão texto alternativa à versão gráfica, tão vulgar em alguns locais, não pode ser confundida com uma versão mais acessível, permitindo o descuidar da acessibilidade na versão gráfica. Esta última, a versão gráfica, muitas vezes rotulada de "página normal", não pode ser deixada ao abandono só porque no site existe uma versão texto. Mesmo quando a versão gráfica é, de todo, impossível de tratar (p.e. desenvolvida integralmente em flash), o que as diretrizes de acessibilidade dizem é que: "é necessário construir uma página alternativa acessível" (ponto 11.4.), o que **não** é o mesmo que dizer uma versão texto.

A versão texto está muito associada à questão da acessibilidade à informação por parte das pessoas cegas, mas é de notar que as tecnologias de apoio utilizadas por este grupo-alvo, aquilo que fazem é efectuar uma transformação do sítio web para uma base texto que lhes permite (aos softwares de leitura de ecrã) transmitir ao utilizador via sintetizador de fala e/ou linha braille o conteúdo da página. Por isso, mesmo pelas pessoas cegas, **é perfeitamente desnecessário construir uma versão texto**. A versão texto é importante para muitos utilizadores com ou sem deficiência mas por questões de largura de banda de acesso à Internet. Um exemplo disso mesmo ocorreu no 11 de Setembro de 2001, aquando do ataque às Torres Gémeas, em Nova Iorque, em que a comunicação social, principalmente a norte americana, retirou tudo o que eram imagens e estilo das páginas web para permitir um maior número de acessos.

Mas, na verdade a sua leitura é também mais difícil a alguns grupos de utilizadores com deficiência, que precisam mais do que ninguém, de imagens para reforçar a mensagem transmitida pela palavra.

> A ideia da construção web passa assim pela construção de **um só conteúdo que sirva todos os utilizadores**. Deixemos o trabalho de transformação/adequação dos conteúdos às diversas tecnologias de apoio existentes no mercado. Temos que ter a consciência que ao seguirmos as diretrizes de acessibilidade web estamos a facilitar este trabalho de transformação às tecnologias de apoio.

Mas será que legendar um bullet gráfico é o mesmo que legendar uma fotografia? E só haverá uma maneira de legendar uma fotografia? Qual é o texto alternativo mais apropriado a uma determinada imagem? Para responder a estas perguntas temos que analisar como são as imagens utilizadas, ou seja, determinar a sua função.

### Uma síntese das diretrizes para a construção de um texto alternativo:

1. Forneça sempre um **texto alternativo para todas** as imagens.
2. Certifique-se que o **texto alternativo** comunica o propósito da imagem de forma **assertiva** e **concisa** (expressa a função da imagem).
3. Forneça um **texto alternativo nulo** (`alt=""`) para uma imagem que não adicione conteúdo à mensagem (i.e. cuja **função** é meramente **decorativa**).
4. Numa imagem do tipo mapa de imagem (elemento `<map>`) forneça um texto alternativo para a **imagem principal** e um texto alternativo para cada uma das **áreas ativas** que compõem o mapa.
5. Nunca repita no **texto alternativo** de uma imagem o texto adjacente à mesma.
6. Nunca coloque **imagens não decorativas**, que transmitam informação significativa para a compreensão da mensagem, como fundos dos elementos HTML (`background`).
7. Lembre-se sempre que legendar não é descrever! Sempre que a imagem necessite de uma descrição longa use o atributo `longdesc`. A ferramenta [CynthiaSays](http://www.cynthiasays.com/) (validador de conteúdos web) provoca um **alerta sempre que a legenda ultrapassa os 80 carateres**.