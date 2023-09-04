# Anotações da aula de HTML do Entra 21

### Introdução 

#### HTML, ou HyperText Markup Language, é a linguagem fundamental utilizada para criar páginas da web. É uma linguagem de marcação que permite a estruturação e a formatação de conteúdo na internet. Ao escrever HTML, os desenvolvedores definem a estrutura de uma página da web, como títulos, parágrafos, imagens, links e muito mais, que os navegadores da web interpretam para exibir o conteúdo visualmente aos usuários.

#### O HTML é uma linguagem relativamente simples de aprender, composta por elementos (ou tags) que são utilizados para descrever diferentes partes de uma página da web. Cada elemento HTML é identificado por uma tag que é colocada entre colchetes angulares (< >). A estrutura básica de um documento HTML inclui elementos essenciais, como < html >, < head >, < title >, e < body >, que definem a estrutura e o conteúdo da página.

#### Aqui está um exemplo de código HTML básico que cria uma página da web simples:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minha Página Web</title>
</head>
<body>
    <header>
        <h1>Bem-vindo à Minha Página Web</h1>
    </header>
    
    <nav>
        <ul>
            <li><a href="#inicio">Início</a></li>
            <li><a href="#sobre">Sobre</a></li>
            <li><a href="#contato">Contato</a></li>
        </ul>
    </nav>

    <main>
        <section id="inicio">
            <h2>Seção de Início</h2>
            <p>Este é o conteúdo da seção de início.</p>
        </section>

        <section id="sobre">
            <h2>Sobre Nós</h2>
            <p>Conheça mais sobre nós nesta seção.</p>
        </section>

        <section id="contato">
            <h2>Entre em Contato</h2>
            <p>Use este formulário para nos enviar uma mensagem.</p>
        </section>
    </main>

    <footer>
        <p>&copy; 2023 Minha Página Web</p>
    </footer>
</body>
</html>
```
</br>

#### Este exemplo representa uma página da web simples com um cabeçalho (< header >), um menu de navegação (< nav >), um conteúdo principal (< main >) dividido em seções (< section >), e um rodapé (< footer >). As tags HTML são usadas para estruturar e organizar o conteúdo, enquanto os atributos como href, charset, e lang fornecem informações adicionais e configurações para a página.

#### O HTML é a espinha dorsal da web, permitindo que os desenvolvedores criem uma ampla variedade de sites e aplicações. À medida que você aprende mais sobre HTML, poderá adicionar formatação, estilos, interatividade e outros elementos para criar páginas da web mais complexas e dinâmicas.
</br>

### Tags Textuais

#### As tags textuais em HTML são elementos utilizados para estruturar e apresentar texto em uma página da web. Elas não adicionam formatação visual significativa, mas fornecem uma estrutura semântica que ajuda os navegadores e mecanismos de busca a entenderem o conteúdo do texto. Aqui estão algumas das tags textuais mais comuns em HTML:

- < p > (Parágrafo): A tag < p > é usada para criar parágrafos de texto. Ela é frequentemente usada para dividir o conteúdo em blocos lógicos. Exemplo:

```html
<p>Este é um parágrafo de exemplo.</p>
```

- < h1 >, < h2 >, < h3 >, < h4 >, < h5 >, < h6 > (Títulos e Subtítulos): Essas tags são usadas para criar títulos e subtítulos com diferentes níveis de importância, onde < h1 > é o mais importante e < h6 > o menos importante. Exemplo:

```html
<h1>Título Principal</h1>
<h2>Subtítulo Importante</h2>
<h3>Subtítulo Menos Importante</h3>
```

- < blockquote > (Citação): A tag < blockquote > é usada para criar citações ou trechos de texto que devem ser destacados. Exemplo:

```html
<blockquote>
  Esta é uma citação importante que deve se destacar do texto principal.
</blockquote>
```

- < q > (Citação Curta): A tag  < q > é usada para criar citações curtas dentro de um parágrafo. Ela adiciona automaticamente aspas ao redor do texto. Exemplo:

```html
<p>Albert Einstein disse <q>E=mc²</q> em sua famosa equação.</p>
```

- < abbr > (Abreviação): A tag  < abbr > é usada para definir abreviações ou siglas, fornecendo uma dica de ferramenta (tooltip) opcional com a descrição completa. Exemplo:

```html
<p>HTML é uma <abbr title="Hypertext Markup Language">linguagem de marcação</abbr> usada para criar páginas da web.</p>
```

- < em > (Ênfase) e < strong > (Destaque): Essas tags são usadas para enfatizar ou destacar o texto. O < em > geralmente é renderizado como itálico, enquanto o < strong > é renderizado como negrito. Exemplo:

```html
<p><em>Isso é importante</em>, e isso é <strong>ainda mais importante</strong>.</p>
```

- < span > (Span): A tag < span > é uma tag genérica usada para aplicar estilos ou scripts a partes específicas do texto sem adicionar significado semântico. Exemplo:

```html
<p>Este é um <span style="color: red;">texto com cor vermelha</span>.</p>
```

- < code > (Código): A tag < code > é usada para envolver código de programação ou texto que deve ser exibido em uma fonte monoespaçada Exemplo:

```html
<p>Para imprimir "Hello, World!" em Python, use <code>print("Hello, World!")</code>.</p>
```

#### Essas são algumas das tags textuais mais comuns em HTML. Elas ajudam a estruturar e apresentar o conteúdo de maneira semântica, tornando-o mais acessível e compreensível para os usuários e os mecanismos de busca. É importante escolher as tags adequadas com base na função e no significado do texto que você está criando em sua página da web.

#### Exemplo feito em aula
```html
<!DOCTYPE html>
<html lang="en">

    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">

        <title>Nome do Site</title>
        <!--Favicon-->
        <link rel="icon" type="image/x-icon" href="../000-Exercícios/assets/rocket.gif">
    </head> 

   

    <body>
        <!-- Exemplos de Titulos -->
        <h1 id="titulo1">Titulo h1</h1>
        <h2>Titulo h2</h2>
        <h3 id="titulo3">Titulo h3</h3>
        <h4>Titulo h4</h4>
        <h5>Titulo h5</h5>
        <h6>Titulo h6</h6>
	    
         <!-- Exemplos de parágrafos -->
	    <p>isso é um parágrafo ....</p>

        <p>Lorem <b> ipsum,</b> dolor sit amet <br> consectetur adipisicing elit. Qui deleniti architecto, distinctio ducimus aliquam nemo delectus sapiente minima modi. Quasi, soluta nihil voluptate distinctio sit doloremque! Obcaecati culpa aliquid illo?</p>

        <!-- Formatação em HTML -->
        <p><b>Negrito</b></p>  
        <p><strong>Enfase</strong></p>
        <p><i>Italico</i></p>
        <p><em>Enfatizado</em></p>
        <p><mark>Grifado</mark> </p>
        <p><small>Texto pequeno</small></p>
        <p><big>Texto Grande</big></p>
        <p><s>texto taxado</s></p>
        <p><del>Taxado</del></p>
        <p>H<sub>2</sub>O</p>
        <p>x<sup>2</sup></p>

        <!-- Cotação e elementos de Citação-->

        <p><q>Texto cotado</q></p>
        <p><blockquote>Texto testesdfsdfsdfsdfsdfsdfsdfsdfsdf</blockquote></p>


        <p>Here is a quote from WWF's website:</p>
        <blockquote cite="http://www.worldwildlife.org/who/index.html">
        For 60 years, WWF has worked to help people and nature thrive. As the world's leading conservation organization, WWF works in nearly 100 countries. At every level, we collaborate with people around the world to develop and deliver innovative solutions that protect communities, wildlife, and the places in which they live.
        </blockquote>

        <p>The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.</p>

        <address>
            Written by John Doe.<br>
            Visit us at:<br>
            Example.com<br>
            Box 564, Disneyland<br>
            USA
        </address>

        <p><cite>The Scream</cite> by Edvard Munch. Painted in 1893.</p>

        <bdo dir="rtl">This text will be written from right to left</bdo>


        <!-- Exemplos de listas -->
        <ul> 
            <li>item 1</li> 
            <li>item 2</li>
            <li>item 3</li>
        </ul>

        <ol> 
            <li>item A</li>
            <li>item B</li>
            <li>item C</li>
        </ol>

        <dl>
            <dt>Chrome</dt>
            <dd>
                o chrome foi desenvolvido pelo google...
            </dd>

            <dt>IE</dt>
            <dd>
                o ie foi desenvolvido pela Microsoft...
            </dd>

            <dt>Safari</dt>
            <dd>
                o safari foi desenvolvido pela Apple...
            </dd>
        </dl>

        <details>
            <summary>Como posso acessar meu curso?</summary>
            <p>vc poderá acessar seu curso atravéws do youtubo pelo link ...</p>
        </details>
        
        <details>
            <summary>Como posso acessar meu curso?</summary>
            <p>vc poderá acessar seu curso atravéws do youtubo pelo link ...</p>
            <table>
                <tr>
                    <td>teste</td>
                    <td>teste2</td>
                </tr>
            </table>
        </details>
```
</br>

### Links

#### Em HTML, os links são elementos que permitem que os usuários naveguem entre diferentes páginas da web ou recursos da internet. Os links são criados usando a tag < a > (Âncora) e geralmente têm um atributo href (Hypertext Reference) que especifica o URL (Uniform Resource Locator) da página ou recurso de destino.

#### Aqui está a estrutura básica de um link HTML:

```html
<a href="URL_DO_DESTINO">Texto do Link</a>
```

#### Aqui estão alguns exemplos de como criar links em HTML:

- Link para uma Página Externa:

```html
<a href="https://www.exemplo.com">Visitar Exemplo.com</a>
```

- Link para uma Página Interna (arquivo HTML na mesma pasta):

```html
<a href="pagina-interna.html">Página Interna</a>
```

- Link para um Endereço de E-mail:

```html
<a href="mailto:seu-email@example.com">Enviar um E-mail</a>
```

- Link para um Número de Telefone:

```html
<a href="tel:+551234567890">Ligar para Nós</a>
```

- Link para um Arquivo para Download (por exemplo, um PDF):

```html
<a href="arquivo.pdf" download>Baixar Arquivo PDF</a>
```

- Link para um Ancoragem Interna (link para uma seção na mesma página):

```html
<a href="#secao-destino">Ir para a Seção de Destino</a>
```

- Para criar uma âncora interna, você deve adicionar um id à seção de destino:

```html
<section id="secao-destino">
    <!-- Conteúdo da seção de destino -->
</section>
```

#### Lembre-se de que os links em HTML podem ter propriedades adicionais, como target (para abrir o link em uma nova janela ou guia) e rel (para especificar a relação entre a página atual e a página de destino).

#### Exemplo de link com target para abrir em uma nova guia:

```html
<a href="https://www.exemplo.com" target="_blank">Abrir em Nova Guia</a>
```

#### Os links desempenham um papel fundamental na navegação na web e na interação do usuário com o conteúdo online. Eles são uma parte essencial de qualquer página da web e são usados para conectar recursos e informações em toda a internet.

#### Exemplo feito em aula

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>

    <h1 id="titulo1">Titulo do Site</h1>

    <!-- link para outro site -->
    <p>O <a href="https://www.entra21.com.br/" target="_self">Entra21</a> é um programa de empregabilidade e formação
        profissional</p>

    <!-- link para um bookmark da própria página-->
    <p><a href="#titulo1">Link para o topo da página</a></p>

    <!-- link para um bookmark de outra página-->
    <p><a href="https://www.proway.de/#colophon" target="_blank">rodapá no site da proway</a></p>

    <!-- link para uma página do próprio site-->
    <p><a href="contato.html">Página de contato</a></p>

    <!-- Link em uma imagem/figura/tag -->
    <a href="https://pt.wikipedia.org/wiki/HTML" target="_black">
        <img src="assets/brazil-flag.png" width="150" alt="fundo js">
    </a>

    <!-- Link para E-mail-->
    <p>Gostou de nossa oferta? entre em <a href="mailto:ivan.borchardt.cobol@gmail.com?subject=Contato&body=estou entrando em contato referente a oferta...">contato</a></p>

    <!-- Link de Download-->
    <p>baixe a <a href="assets/brazil-flag.png" download>bandeira do brasil</a></p>


    
    <!-- Atributo Target -->
    <h2>Exemplos com Atributo Target</h2>

    <!-- _self - é o Default - Abre na mesma aba -->
    <p><a href="https://www.entra21.com.br/" target="_self">Target Self</a></p>

    <!-- Abre em uma nova aba -->
    <p><a href="https://www.entra21.com.br/" target="_blank">Target Blank</a></p>

    <!-- _parent _top _nomeFrame -->
    <iframe src="002A_Exemplo_Links_iFrame_top.html" frameborder="0" name="frameAvo" height="500" width="600"></iframe>
    <iframe src="" frameborder="0" name="frameAlvo" height="500" width="600"></iframe>
  
    


</body>

</html>
```
</br>

```html
<h2>frame Pai do Pai</h2>
<iframe src="002B_Exemplo_Links_iFrame_parent.html" frameborder="0" height="500" width="1200"></iframe>

```
</br>

```html
<h2>frame pai</h2>
<iframe src="002C_Exemplo_Links_iFrame_link.html" frameborder="0" height="500" width="1200"></iframe>

```

</br>

```html
<h2>frame onde os links estão</h2>

<!-- Abre no Frame Pai-->
<p><a href="https://www.entra21.com.br/" target="_parent">Target parent</a></p>

<!-- Abre no Frame Topo-->
<p><a href="https://www.entra21.com.br/" target="_top">Target top</a></p>

<!-- Abre no Frame nomeado-->
<p><a href="https://www.entra21.com.br/" target="frameAlvo">Target NameFrame</a></p>
```
</br>

### Eelemntos Estruturais em HTML

#### Os elementos estruturais em HTML são tags que definem a estrutura básica de uma página da web, organizando o conteúdo em diferentes partes ou seções. Eles não apenas tornam a página mais organizada, mas também têm implicações semânticas, o que ajuda os navegadores e mecanismos de busca a entenderem a hierarquia do conteúdo. Aqui estão alguns dos principais elementos estruturais em HTML5:

- < header >: O elemento < header > é usado para representar a introdução de uma página ou de uma seção da página. Geralmente contém elementos como logotipos, títulos principais, menus de navegação e outras informações de identificação.

- < nav >: O elemento < nav > é usado para criar menus de navegação, sejam eles na parte superior da página, no rodapé ou em outros locais. Ele ajuda os leitores a encontrar diferentes seções ou páginas do site.

- < main >: O elemento < main > envolve o conteúdo principal da página. Deve haver apenas um elemento < main > por página, e ele é usado para identificar o conteúdo central da página, excluindo cabeçalhos, rodapés e barras laterais.

- < article >: O elemento < article > é usado para envolver conteúdo independente e autocontido que faz sentido por si só, como um post de blog, um artigo de notícias ou um widget de comentários.

- < section >: O elemento < section > é usado para agrupar conteúdo relacionado dentro do < main >. Ele não implica nenhuma relação específica com o conteúdo de fora da seção.

- < aside >: O elemento < aside > é usado para conteúdo que é tangencial ou relacionado ao conteúdo principal da página, mas que pode ser considerado separado. Isso é comumente usado para barras laterais, anúncios ou conteúdo relacionado.

- < footer >: O elemento < footer > representa a seção de rodapé de uma página ou de uma seção. Geralmente contém informações de contato, links para páginas relacionadas, direitos autorais e outras informações semelhantes.

- < hgroup >: Embora não seja amplamente utilizado, o elemento < hgroup > costumava ser usado para agrupar vários títulos (< h1 >, < h2 >, etc.) que eram parte de um cabeçalho. No entanto, foi considerado obsoleto no HTML5.

- < figure > e < figcaption> : Esses elementos são usados juntos para marcar imagens ou outros elementos multimídia e fornecer uma legenda. O elemento < figure > envolve a mídia, enquanto < figcaption > fornece a legenda.

- < mark >: O elemento < mark > é usado para destacar parte do texto em uma página, geralmente com uma cor de fundo amarela, para chamar a atenção do usuário.

#### Esses elementos estruturais fornecem uma maneira semântica de organizar o conteúdo de uma página da web, tornando-o mais acessível e compreensível para os navegadores, mecanismos de busca e leitores de tela. Ao usar essas tags corretamente, você ajuda a melhorar a legibilidade e a usabilidade do seu site, além de aprimorar a otimização de mecanismos de busca (SEO).

#### Exemplo feito em aula

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <div>
        <!---------------- Area de Cabeçalho ---------------------->
        <header>
                <h1>titulo</h1>
                <nav>
                    <ul>
                        <li><a href="">Home</a></li>
                        <li><a href="">Loja</a></li>
                        <li><a href="">Contato</a></li>
                    </ul>
                </nav>
            </div>
            <div>
                <p>logo da empresa</p>
            </div>
        </header>
        <!---------------- Barra Lateral Esquerda ---------------------->
        <aside>
            <p>aside esquerda</p>
        </aside>
        <!---------------- Sessao Principal ---------------------->
        <main>
            <section>
                <span><p>caixa de uma unica linha</p></span>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    Dolore aperiam, <span>facere modi animi</span> dignissimos maiores? 
                    Eaque enim laudantium libero illum debitis nisi ullam hic 
                    consequatur, quisquam quam aliquam alias mollitia.</p>
                <div>

            </section>

            <section>
                <h2>Titulo</h2>
                <article>
                    <h3>titulo do artigo </h3>
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Illum, ratione repellat praesentium
                        explicabo reiciendis laborum! Quidem quisquam voluptatem, dolor facere, esse debitis harum quod,
                        laboriosam tenetur reiciendis unde sunt praesentium.</p>
                    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptatem in corrupti obcaecati
                        voluptatibus, reprehenderit laboriosam, veritatis minima, saepe vel fuga similique? Ullam,
                        consectetur sunt eum eligendi doloremque velit nemo rerum.</p>
                </article>

            </section>
            <section>
                <figure>
                    <img src="" alt="" title="">
                    <figcaption>créditos: Joao Figueredo</figcaption>
                </figure>
            </section>
        </main>
        <!---------------- Bara Lateral Direita ---------------------->
        <aside>
            <p>aside direita</p>
        </aside>
        <!---------------- Sessão de Rodapé  ---------------------->
        <footer>

        </footer>
    </div>
</body>

</html>
```
</br>

### Tabelas

#### Tabelas em HTML são usadas para organizar dados em linhas e colunas, tornando-as ideais para apresentar informações tabulares de maneira estruturada e legível em páginas da web. As tabelas são compostas por vários elementos, cada um deles com um propósito específico. Vamos explorar os principais elementos e atributos relacionados a tabelas HTML:

- < table >: O elemento  < table > é a tag de nível mais alto que define uma tabela HTML. Ele contém todo o conteúdo da tabela, incluindo linhas, colunas e células.

```html
<table>
    <!-- Conteúdo da tabela -->
</table>
```

- < tr >: O elemento < t r> é usado para criar uma linha em uma tabela. Ele deve estar dentro do elemento < table >. Cada linha contém uma ou mais células.

```html
<tr>
    <!-- Células da linha -->
</tr>
```

- < th >: O elemento  < th > é usado para criar cabeçalhos de coluna em uma tabela. Eles são normalmente exibidos em negrito e centralizados.

```html
<th>Cabeçalho 1</th>
<th>Cabeçalho 2</th>
```

- < td >: O elemento < td > é usado para criar células de dados em uma tabela. Cada célula contém um valor ou conteúdo.

```html
<td>Dado 1</td>
<td>Dado 2</td>
```

- < caption >: O elemento < caption > é usado para adicionar um título ou uma legenda à tabela. Ele deve ser colocado dentro do elemento <table>, mas geralmente é exibido acima ou abaixo da tabela.

```html
<table>
    <caption>Título da Tabela</caption>
    <!-- Conteúdo da tabela -->
</table>
```

- colspan e rowspan: Esses atributos são usados em células específicas para mesclar colunas ou linhas adjacentes. O colspan especifica quantas colunas a célula deve abranger, enquanto o rowspan especifica quantas linhas.

```html
<td colspan="2">Esta célula ocupa duas colunas</td>
<td rowspan="3">Esta célula ocupa três linhas</td>
```


- Tabelas aninhadas: É possível aninhar tabelas dentro de células de uma tabela maior para criar layouts complexos.

```html
<table>
    <tr>
        <td>Tabela 1</td>
        <td>Tabela 2</td>
    </tr>
    <tr>
        <td>
            <table>
                <!-- Conteúdo da tabela 1 -->
            </table>
        </td>
        <td>
            <table>
                <!-- Conteúdo da tabela 2 -->
            </table>
        </td>
    </tr>
</table>
```

#### Tabelas em HTML são úteis para apresentar dados tabulares, como listas, relatórios e informações organizadas em colunas e linhas. No entanto, é importante notar que tabelas não devem ser usadas para criar layouts de página, pois essa abordagem é considerada obsoleta em favor do uso de CSS para criar layouts responsivos. Em vez disso, as tabelas devem ser reservadas para a apresentação de dados tabulares legítimos.

#### Exemplo feito em aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
    <!-- Estrutura mínima de uma tabela-->
    <table border="1">
        <tr>
            <th>Coluna 1</th>
            <th>Coluna 2</th>
            <th>Coluna 3</th>
        </tr>
        <tr>
            <td>Linha 1, Coluna 1</td>
            <td>Linha 1, Coluna 2</td>
            <td>Linha 1, Coluna 3</td>
        </tr>
        <tr>
            <td>Linha 2, Coluna 1</td>
            <td>Linha 2, Coluna 2</td>
            <td>Linha 2, Coluna 3</td>
        </tr>
        <tr>
            <td>Linha 3, Coluna 1</td>
            <td>Linha 3, Coluna 2</td>
            <td>Linha 3, Coluna 3</td>
        </tr>
    </table>

    <br>

    <!-- Estrutura completa de uma tabela-->
    <table border="1" cellpadding="10" width="100%" align="center">
        <thead>
            <tr>
                <th>Qtd</th>
                <th>Descrição</th>
                <th>Valor</th>
            </tr>
        </thead>
        <tbody>
            <tr align="center">
                <td>1</td>
                <td>Lápis</td>
                <td>1,00</td>
            </tr>
            <tr bgcolor="red">
                <td align="right">2</td>
                <td>Caneta</td>
                <td>3,00</td>
            </tr>
            <tr>
                <td>4</td>
                <td>Caderno</td>
                <td>10,00</td>
            </tr>
            <tr>
                <td>2</td>
                <td>Borracha</td>
                <td>5,00</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td colspan="2"><b>Total</b></td>
                <td>19,00</td>
            </tr>
        </tfoot>

    </table>

    <br><br>
    <!-- Mesclando linhas e colunas -->

    <table border="1" cellspacing="0" >
        <tr>
            <th>coluna 1</th>
            <th>coluna 2</th>
            <th>coluna 3</th>
        </tr>
        <tr>
            <td rowspan="2"> linha 1, coluna 1</td>
            <td> linha 1, coluna 2</td>
            <td> linha 1, coluna 3</td>
        </tr>
        <tr>
            <td> linha 2, coluna 1</td>
            <td> linha 2, coluna 2</td>
        </tr>
        <tr>
            <td> linha 3, coluna 1</td>
            <td> linha 3, coluna 2</td>
            <td> linha 3, coluna 3</td>
        </tr>
        <tr>
            <td> linha 4, coluna 2</td>
            <td colspan="2"> linha 4, coluna 3</td>
        </tr>
    </table>


</body>
</html>
```

</br>

### Audio Visual

#### Em HTML, você pode incorporar áudio e vídeo em suas páginas da web usando as tags < audio > e < video >. Isso permite que você forneça uma experiência multimídia aos visitantes do seu site. Aqui estão os detalhes sobre como usar essas tags:

#### < audio > (Áudio)
- A tag < audio > é usada para incorporar conteúdo de áudio em uma página da web. Você pode incluir arquivos de áudio, como músicas, podcasts ou efeitos sonoros. Aqui está um exemplo básico de como usar a tag < audio >:

```html
<audio controls>
    <source src="exemplo.mp3" type="audio/mpeg">
    Seu navegador não suporta o elemento de áudio.
</audio>
```

#### Neste exemplo, a tag <audio> possui um atributo controls, que exibe controles de reprodução padrão (como play, pause, volume) para o áudio. A tag <source> é usada para especificar a fonte do arquivo de áudio e o tipo MIME (type). É uma boa prática fornecer vários formatos de arquivo (por exemplo, MP3, Ogg) para maior compatibilidade com navegadores.

#### < video > (Vídeo)
A tag <video> é usada para incorporar conteúdo de vídeo em uma página da web. Você pode incluir vídeos como parte do seu conteúdo, como tutoriais, clipes ou apresentações. Aqui está um exemplo de como usar a tag <video>:

```html
<video controls width="400">
    <source src="exemplo.mp4" type="video/mp4">
    Seu navegador não suporta o elemento de vídeo.
</video>
```

#### Neste exemplo, a tag < video > também possui o atributo controls para exibir controles de reprodução. O atributo width define a largura do vídeo em pixels. Assim como com o áudio, é importante fornecer diferentes formatos de vídeo (por exemplo, MP4, WebM) para garantir compatibilidade com diversos navegadores.

#### Além disso, ambas as tags < audio > e < video > suportam outros atributos e opções, como autoplay (reprodução automática), loop (repetição), preload (pré-carregamento) e muito mais. Você pode personalizar a aparência e o comportamento do áudio e do vídeo usando CSS e JavaScript, conforme necessário.

#### Lembre-se de que, ao usar áudio e vídeo em uma página da web, é importante considerar o tamanho dos arquivos e a experiência do usuário, especialmente em dispositivos móveis, para garantir que o conteúdo seja acessível e adequado ao contexto da página.

#### Exemplo feito em aula

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>

    <!-- Imagens -->
    <img src="../000-Exercícios/assets/States_of_Brazil.png" alt="Mapa do Brasil" title="Mapa dos estados do brasil"
        width="150" height="150">

    <!-- Tipos de imagem jpeg, png, gif, svg, ico -->
    <figure>
        <img src="assets/brazil-flag.png" alt="" width="100" title="Bandeira do Brasil">
        <figcaption>Créditos: Algum Artista Qualquer</figcaption>
    </figure>

    <!-- Vídeo mp4, ogg, WebM-->
    <video width="320" controls autoplay loop muted>
        <source src="assets/20230513_160933.mp4">
        <source src="assets/20230513_160933.ogg">
        Seu Navegador não é compatível com a tag Vídeo
    </video>

    <!-- Vídeo do Youtube -->
    <iframe width="420" height="315" src="https://www.youtube.com/embed/SsqXAP0EeEI">
    </iframe>

    <!-- Audio -->
    <audio controls autoplay loop muted>
        <source src="assets/bad_to_the_bone.mp3" type="audio/mpeg">
        <source src="assets/bad_to_the_bone.ogg" type="audio/ogg">
        Seu Navegador não é compatível com a tag Audio
    </audio>
    <p>download</p>

</body>

</html>
```
</br>

## Formulários

#### Formulários em HTML são elementos que permitem a coleta de informações de usuários por meio de campos interativos, como caixas de texto, botões de opção, caixas de seleção e botões de envio. Eles desempenham um papel fundamental na interatividade de sites da web, permitindo que os visitantes insiram dados, façam escolhas e enviem informações para processamento em servidores web. Abaixo, vou abordar os principais elementos e conceitos relacionados a formulários em HTML:

Elemento < form >:
O elemento < form > é usado para criar um formulário HTML. Ele envolve todos os elementos de entrada (como campos de texto, botões, etc.) que fazem parte do formulário. O atributo action especifica para onde os dados do formulário serão enviados quando o usuário o enviar. O atributo method define o método HTTP a ser usado para o envio dos dados, como GET ou POST. Exemplo:

```html
<form action="processar.php" method="post">
  <!-- campos de entrada aqui -->
</form>
```
#### Elementos de Entrada (< input >, < textarea >, < select >): 

- < input >: Este elemento é usado para criar diversos tipos de campos de entrada, como caixas de texto, botões de opção, caixas de seleção, etc. O atributo type define o tipo de campo de entrada. Exemplo de caixa de texto:

```html
<input type="text" name="nome" id="nome">
```

- <textarea>: Usado para criar campos de texto multilinha. Exemplo:

```html
<textarea name="comentario" id="comentario" rows="4" cols="50"></textarea>
```

- <select>: Cria uma lista suspensa (dropdown) ou uma caixa de seleção. Exemplo:

```html
<select name="cidade" id="cidade">
  <option value="nova-york">Nova York</option>
  <option value="londres">Londres</option>
  <!-- outras opções -->
</select>
```

#### Botões de Envio (< input type="submit" >, < input type="reset" >):

- < input type="submit" >: Cria um botão que, quando clicado, envia os dados do formulário para o servidor.
Exemplo:

```html
<input type="submit" value="Enviar">
```

 - < input type="reset" >: Cria um botão que redefine todos os campos do formulário para seus valores padrão. Exemplo:

```html
<input type="reset" value="Limpar">
```

#### Rótulos (< label >):
- Os elementos <label> são usados para associar um texto descritivo a um campo de entrada. Isso melhora a acessibilidade e a usabilidade, permitindo que os usuários cliquem no rótulo para selecionar o campo correspondente. Exemplo:

```html
<label for="nome">Nome:</label>
<input type="text" name="nome" id="nome">
```


#### Campos Ocultos (< input type="hidden" >):
- Os campos ocultos são usados para armazenar informações no formulário que não são visíveis para o usuário. Esses campos são frequentemente usados para passar dados entre páginas ou manter o estado do formulário. Exemplo:

```html
<input type="hidden" name="pagina_atual" value="formulario.html">
```

#### Validação de Formulário: Você pode adicionar validação de formulário usando JavaScript ou atributos HTML5, como required, pattern, min, max, etc. Isso ajuda a garantir que os dados inseridos pelo usuário estejam no formato correto antes de serem enviados para processamento.

#### Processamento de Formulário: O processamento dos dados do formulário geralmente ocorre no lado do servidor, onde os dados são recebidos, validados e processados. A linguagem de programação comum para esse processamento é o PHP, mas muitas outras linguagens, como Python, Ruby e Node.js, também são usadas.

#### Segurança: É importante tomar medidas de segurança ao lidar com formulários, como validar e escapar dados para evitar ataques de injeção de código (como SQL Injection e Cross-Site Scripting).

#### Lembre-se de que a estrutura e o funcionamento de um formulário podem variar de acordo com as necessidades específicas do seu projeto. É importante criar formulários que sejam intuitivos e amigáveis para os usuários, além de seguros contra possíveis ameaças de segurança.

#### Exemplo feito em aula 

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .etiqueta{
            display: block;
        }


    </style>
</head>
<body>
    <form action="">

        <label for="idIdade" class="etiqueta">Idade</label>
        <input type="text" name="" id="">

        <div>
            <div>
                <label for="idCpf">CPF:</label>
            </div>
            <input type="text" name="" id="">
        </div>

        <label for="idNome">Nome:</label><br>
        <input type="text" id="idNome" name="nmNome" value="Joao" >

        <br><br>
        <label for="idDesc">Descrição</label><br>
        <textarea name="nmDesc" id="idDesc" cols="30" rows="10">innerText</textarea> <!-- o valor do textarea é a propriedade innerText-->
 
        <br><br>
        <button type="reset">Limpar</button>
        <button type="submit">Enviar</button>
        <button type="button">Testar</button>
    </form>
</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .etiqueta{
            display: block;
        }
    </style>

</head>
<body>

    <form action="">
        <!--Campo de texto de um linha-->
        <label for="idNome" class="etiqueta">Nome:</label>
        <input type="text" name="nmNome" id="idNome" value="" placeholder="Nome" required>


        <!--Campo Numérico-->
        <label for="idTemp" class="etiqueta">Temperatura</label>
        <input type="number" name="nmTemp" id="idTemp" min="-5" max="100" step="0.01">


        <!-- Intervalo Numérico-->
        <label for="idInter" class="etiqueta">Intervalo</label>
        <input type="range" name="nmInter" id="idInter" min="0" max="100" value="0">


        <!-- Caixas de Senha -->
        <label for="idSenha" class="etiqueta">Senha</label>
        <input type="password" name="" id="">

        <!-- Caixas para Email-->
        <label for="idEmail" class="etiqueta">E-mail</label>
        <input type="email" name="nmEmail" id="idEmail">


        <!-- Caixas para Datas-->
        <label for="idData" class="etiqueta">Data</label>
        <input type="date" name="nmData" id="idData" min="2022-04-01" max="2022-05-30" >

        <!-- Caixas para Data Hora Local -->
        <label for="idDataHL" class="etiqueta">Data: </label>
        <input type="datetime-local" name="nmDataHL" id="idDataHL">

        <!-- Caixas para Hora -->
        <label for="idHora" class="etiqueta">Hora</label>
        <input type="time" name="nmHora" id="idHOra">

        <!-- Seletor de cores -->
        <label for="idCor" class="etiqueta">Cor</label>
        <input type="color" name="nmCor" id="idCor">

        <!-- Radio Button -->
        <br><br>
        <input type="radio" name="nmGenero" id="idFem" checked>
        <label for="idFem">Feminino</label>
        <br>
        <input type="radio" name="nmGenero" id="idMasc">
        <label for="idFmasc">Masculino</label>
        <br>
        <input type="radio" name="nmGenero" id="idMasc">
        <label for="idFmasc">LGBT</label>

        <!-- Check Box -->
        <br><br>
        <input type="checkbox" name="nmMarcas" id="idFordKa">
        <label for="idFordKa">Ford Ka</label>
        <br>
        <input type="checkbox" name="nmMarcas" id="idGol">
        <label for="idGol">Gol</label>   
        <br>
        <input type="checkbox" name="nmMarcas" id="idFerrari">
        <label for="idGol">Ferrari</label>   


        <br><br>
        <input type="submit" name="" id="">
        <input type="reset" name="" id="" value="Limpar">
        <input type="button" name="" id="" value="Testar">

    </form>



    
</body>
</html>
```

![logo entra 21](https://cdn.sonicadigital.com.br/entra21/storage/header/257/original-61f8610472d4f.png)