### Atualização de repositório
Atualizado a 21 de janeiro de 2026

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

---

### Determinar a função de uma imagem

Num sítio web as imagens são utilizadas de três formas:

1. Como veículo de **transmissão de informação** importante;
2. Para tornar o **conteúdo visualmente mais legível e atraente** mas não transmitindo conteúdo adicional;
3. Para **ligar a outras áreas** do sítio web.

O texto alternativo mais apropriado a uma imagem depende da forma como a mesma é utilizada. Na realidade uma mesma imagem pode ser utilizada por diferentes razões e sob diferentes circunstâncias, e cada ocorrência desta imagem poderá ter diferentes textos alternativos.

> **Nota:** O texto alternativo mais apropriado comunica o propósito da imagem, e não a sua aparência.

---

### Imagem como veículo de transmissão de informação importante

Se a imagem ou gráfico contém informação que é relevante para a compreensão do conteúdo do site então o atributo `alt` deve também fornecer esse conteúdo, de uma forma que seja coerente com o propósito da imagem. Estão nesta categoria menus gráficos (ver figura 1), lettering gráfico usado quando se pretende um tipo de letra fora do leque disponível na web (ver figura 2).

#### 3.1. Imagens usadas num menu

![Portal das Compras Públicas: um exemplo de um menu feito com imagens](https://www.acessibilidade.gov.pt/wp-content/uploads/2020/04/1_imagens_1.jpg)
*Figura 1: Exemplo de um menu gráfico.*

Figura 1: note-se no uso explícito do atributo `alt`: `<img ...="" alt="Programa Nacional">` retirado de http://www.compras.gov.pt

#### 3.2. Imagens usadas para aumentar o leque das fontes web disponíveis

![Um exemplo de lettering gráfico: compromisso com a ciência para o futuro de Portugal](https://www.acessibilidade.gov.pt/wp-content/uploads/2020/04/1_imagens_2.jpg)
*Figura 2: exemplo de um elemento de lettering gráfico.*

Figura 2: `<img ....="" alt="Compromisso com a ciência para o futuro de portugal">` retirado de http://www.mctes.pt

#### 3.3. O caso das fotografias

Uma imagem, quando afixada numa página web pode ter múltiplos propósitos. Vamos imaginar que um professor numa aula de fotografia coloca esta imagem (figura 3) a par de outras para mostrar a diferença entre a qualidade de uma fotografia tirada no início do século XX de uma outra tirada no final do século XX.

*Figura 3: Como legendar uma fotografia?*

![Fotografia do início do século XX](https://www.acessibilidade.gov.pt/wp-content/uploads/2020/04/1_imagens_3.jpg)


Provavelmente, no caso desta fotografia bastaria um texto alternativo com: "Fotografia do início do século XX". E, provavelmente, se quiséssemos descrever com mais detalhe a fotografia, daríamos uma descrição aprofundada dos aspectos técnicos que caracterizam uma fotografia do início do século XX.

Vamos imaginar que se trata de uma aula de História de Portugal e que o professor colocava esta mesma fotografia integrada num menu, do tipo galeria de fotos, a cuja página dava o título "Presidentes da República Portuguesa". Provavelmente iria legendar esta imagem como "1º presidente da república (início do mandato em 1911 e fim em 1915)". E esse link poderia ir dar a uma página em que, de novo, aparecia a fotografia, mas agora com o texto alternativo "Manuel de Arriaga Brum da Silveira", na qual se fornecia também uma descrição mais longa com algumas notas biográficas. Esta última exigência coloca-nos outra questão: como colocar uma descrição longa?

### 3.4. Como colocar uma descrição longa

Pegando ainda na fotografia do 1º presidente da República Portuguesa, a descrição longa poderia ser implementada de várias formas:

- Incorporada no próprio documento onde ela se encontra afixada;
- No atributo `longdesc`;
- Usando um link [D] no lado direito da imagem;
- E, ainda, poderíamos recorrer à técnica de fazer da própria imagem um link para a sua descrição.

#### 3.4.1. Exemplo 1: Descrição longa incorporada no próprio documento


*Figura 4: Descrição longa incorporada no próprio documento*

![Manuel de Arriaga (1º presidente da República Portuguesa)](https://www.acessibilidade.gov.pt/wp-content/uploads/2020/04/1_imagens_3.jpg)

Manuel de Arriaga Brum da Silveira  
Horta, Faial, 8/7/1840 - Lisboa, 5/3/1917.  
Advogado, professor liceal, político, poeta e escritor. O primeiro Presidente da República foi eleito em 1911 e demitiu-se em 1915, sem ter completado o mandato, após a fracassada ditadura do general Pimenta de Castro. Com 71 anos, era um histórico do movimento republicano. O seu mandato presidencial foi controverso desde a eleição, quando, declaradamente, se iniciou o confronto entre as facções que compunham o Partido Republicano.

#### 3.4.2. Exemplo 2: Descrição longa incorporada no atributo longdesc

```html
<img ...="" alt="Manuel de Arriaga (1º presidente da república portuguesa)" longdesc="1_presidente.htm">
```

E na página "1_presidente.htm" colocaria a descrição longa.

#### 3.4.3. Exemplo 3: Descrição longa usando o convencionado link D
```html
<img ...="" alt="Manuel de Arriaga (1º presidente da república portuguesa)">[<a href="1_presidente.htm">D</a>]
```
Note a adição no texto alternativo ".... ## contém link com descrição".
Poderíamos continuar com diferentes cenários mas pensamos que estes dois exemplos são suficientes para compreender que não existe uma única forma correcta de atribuir um texto alternativo a uma imagem. Tudo depende do contexto e do propósito da imagem. Trata-se de um julgamento que o autor da página tem de fazer.

---

## Imagem para tornar o conteúdo visualmente mais legível e atraente mas não transmitindo conteúdo adicional

### 4.1 Imagens decorativas
A Web tornou-se um ambiente gráfico no qual os criadores de páginas adicionam frequentemente imagens apenas para melhorar o apelo estético das suas criações. Por exemplo, a imagem que se mostra abaixo pode ser utilizada como parte integrante de uma caixa apenas com o propósito de arredondar os seus cantos.

![Exemplo de uma imagem decorativa: canto superior direito arredondado para uma caixa](https://www.acessibilidade.gov.pt/wp-content/uploads/2020/04/1_imagens_5.gif)

### Figura 5: Os cantos arredondados de uma caixa.

Este é um exemplo que deverá levar um texto alternativo nulo, i.e. sem conteúdo algum, como mostra o código seguinte:

```html
<img src="corner.gif" alt="">
```

### 4.2 Espaçadores gráficos para alinhar elementos
Quem concebe páginas web usa com frequência imagens transparentes, geralmente com 1 píxel de dimensão, que servem de espaçadores para gerar espaços entre os elementos de uma página. É uma técnica rudimentar de alinhar elementos e que deve ser substituída com vantagens por técnicas em CSS, mas actualmente ela ainda está muito presente. Os utilizadores que usam a visão para navegar na web não as vêem, uma vez que estas são transparentes. Mas quem usa tecnologias de apoio ou mesmo navegadores web de base texto estas pequenas imagens não passam despercebidas. Há, no entanto, formas de as tornar totalmente inofensivas a quem usa tecnologias de apoio. Basta, para isso, legendá-las, colocando o conteúdo do atributo `alt` completamente vazio (`alt=""`).

### 4.3 Imagens redundantes
Com frequência, quem desenvolve páginas web, adiciona texto alternativo a uma imagem que é exactamente igual ao texto que se lhe segue, como se mostra no exemplo abaixo:

Figura 6: Não repita no texto alternativo da imagem o texto que lhe está adjacente

![Exemplo de uma imagem com texto adjacente redundante](https://www.acessibilidade.gov.pt/wp-content/uploads/2020/04/1_imagens_6.jpg)

Figura 6: a imagem repete o texto que lhe está adjacente: "Proposta de Lei do Orçamento de Estado para 2007". retirado de [http://www.min-financas.pt](http://www.min-financas.pt) em Outubro 2006.

Esta imagem deveria também estar legendada com um texto alternativo vazio (`alt=""`):
```html
<img ....="" alt="">
```

### 4.4. Imagens para bullets de listas
Alguns designers usam elementos gráficos para destacar, ou ilustrar, cada um dos itens de enumeração constantes de uma lista. A técnica mais correcta será sempre a de colocar estes elementos gráficos na folha de estilo em cascata, mas quando tal não acontece e estes elementos gráficos são posicionados no HTML, então deverão ter um texto alternativo que faça também parecer, em modo texto, que estamos perante um elemento de enumeração de uma lista.

Assim deveremos colocar como texto alternativo algo como `alt="-"` ou `alt="*"`.

Figura 7: O exemplo de bullets gráficos.

![Exemplo de bullets gráficos](https://www.acessibilidade.gov.pt/wp-content/uploads/2020/04/1_imagens_8.jpg)

---
## Imagem para ligar a outras áreas do sítio web
### 5.1. O caso do mapa de imagem
No exemplo que se segue existe apenas uma imagem, mas há 5 áreas activas. Cada uma destas áreas activas (hot spot) conduz o utilizador a diferentes secções do sítio web.

Cada uma das áreas activas é um link que importa descortinar o seu propósito. O texto alternativo para cada uma destas áreas activas deve ser exactamente igual ao texto que se encontra na imagem. No exemplo que se segue, o texto alternativo para cada área activa deve ser respectivamente: Entrada, Produtos, Serviços, Comprar e Contactos. Fica assim definido o texto alternativo para cada uma das áreas activas.

Para além da definição do texto alternativo das áreas activas é necessário também definir o texto alternativo para a imagem, no seu global. Neste caso deveremos definí-lo com o nome que corresponde ao significado deste elemento, ou seja, algo como alt="Menu Principal".

Figura 8: O caso dos textos alternativos para um mapa de imagem.

![Menu feito com um mapa de imagem](https://www.acessibilidade.gov.pt/wp-content/uploads/2020/04/1_imagens_7.jpg)

O código que formata este elemento é:
```html
<img src="imagemap.jpg" alt="Menu Principal " width="199" height="303" usemap="#mapaimagem"/>
<map name="mapaimagem">
    <area shape="rect" coords="7,9,191,54" href="entrada.htm" alt="Entrada">
    <area shape="rect" coords="7,68,191,114" href="produtos.htm" alt="Produtos">
    <area shape="rect" coords="7,127,190,172" href="servicos.htm" alt="Serviços">
    <area shape="rect" coords="6,186,190,229" href="comprar.htm" alt="Comprar">
    <area shape="rect" coords="7,245,189,289" href="contactos.htm" alt="Contactos">
</map>
    ```
