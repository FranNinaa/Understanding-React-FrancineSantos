# Anotações das Aula de CSS

## Introdução 

#### O Cascading Style Sheets, mais conhecido como CSS, é uma linguagem de estilo utilizada na web para controlar a apresentação e o design de páginas da internet. CSS desempenha um papel essencial na criação de experiências visuais atraentes e funcionais na web, permitindo que os desenvolvedores e designers controlem a formatação, o layout e a aparência de elementos HTML em um site.

#### Esta linguagem de estilo oferece uma ampla gama de recursos e propriedades que permitem personalizar cores, fontes, espaçamentos, posicionamentos e muitos outros aspectos do conteúdo da web. Com CSS, é possível criar layouts responsivos que se adaptam a diferentes dispositivos, tornando a experiência do usuário mais consistente e agradável em smartphones, tablets e computadores desktop.

#### Além disso, o CSS segue o princípio da separação de preocupações, o que significa que você pode manter o conteúdo (HTML), a apresentação (CSS) e a interatividade (JavaScript) separados, facilitando a manutenção e a escalabilidade do seu projeto web.

#### Neste contexto, vamos explorar os conceitos fundamentais, propriedades e técnicas avançadas do CSS, ajudando a criar páginas web visualmente atraentes e funcionais. O CSS desempenha um papel crucial na web moderna, permitindo que as páginas se destaquem, transmitam informações de maneira eficaz e proporcionem uma experiência de usuário memorável.
#### Para adicionar estilos CSS a um arquivo HTML, você tem três opções principais:

#### Folha de Estilos Externa:

- Esta é a abordagem mais comum e recomendada. Você cria um arquivo CSS separado e, em seguida, vincula esse arquivo ao seu HTML usando o elemento < link > na seção < head > do seu documento HTML.

```html
<link rel="stylesheet" href="assets/estilos.css">
```

</br>

- O arquivo CSS externo (style.css) pode conter todas as regras de estilo que você deseja aplicar ao seu HTML.

#### Folha de Estilos Interna:

- Você também pode incluir regras de estilo diretamente em seu documento HTML, dentro da seção < style > na seção < head >. Isso é chamado de "folha de estilos interna".

No exemplo, as regras de estilo internas estão dentro do elemento < style >:

```html
<style>
    /* Suas regras de estilo aqui */
</style>
```
</br>

#### Estilos Inline:

- Você pode aplicar estilos diretamente a um elemento HTML usando o atributo style. Isso é chamado de "estilo inline".

- No exemplo, o estilo inline é aplicado ao elemento <h1> desta maneira:

```html
<h1 style="color: beige;">Testes</h1>
```
</br>

- O estilo inline é útil quando você deseja aplicar um estilo específico a um único elemento HTML.

### A ordem de prioridade dos estilos é geralmente a seguinte (do mais específico ao menos específico):

- Estilos Inline (mais específicos)
- Folha de Estilos Interna
- Folha de Estilos Externa (menos específicos)
  
### Certifique-se de organizar seus estilos de acordo com a hierarquia e a especificidade necessárias para seu projeto. O uso de folhas de estilos externas é recomendado para manter seu código mais organizado e facilitar a manutenção.

</br>

### Exemplo passado na aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="assets/estilos.css"> <!--Folha De estilos Externa-->
    
    <!--Folha De estilos Interna-->
    <style>  
        *{
            padding: 0;
        }
        h1{
            padding: 0;
        }

        .classe1{
            background-color: aquamarine;
        }

        #id1{
            padding: 0;
        }
    </style>
</head>
<body>
    <div id="id1" class="classe1"> 
        <h1 style="color: beige; ">Testes</h1> <!-- Estilos Inline -->
    </div>   

    <div id="id2">
        <h1 class="classe2">Teste 2</h1>
    </div>

    <p>Lorem ipsum dolor sit amet.</p>

</body>
</html>
```
</br>

## Background 

#### A propriedade background no CSS é usada para definir o plano de fundo (background) de um elemento HTML, como uma < div >, < section >, ou qualquer outro elemento que você deseje estilizar. Ela permite que você controle a cor de fundo, a imagem de fundo, a repetição da imagem, a posição, o tamanho e outros aspectos relacionados ao plano de fundo de um elemento. Aqui estão os principais usos e propriedades associadas à propriedade background:

- Definir a cor de fundo: Você pode usar background-color para definir uma cor sólida de fundo para o elemento. Por exemplo:
```css
background-color: lightblue;
```
</br>

- Adicionar uma imagem de fundo: A propriedade background-image permite que você insira uma imagem de fundo. Isso é frequentemente usado para criar layouts atraentes. Por exemplo:
```css
background-image: url('imagens/fundo.png'); /*URL*/
```
</br>

- Controlar a repetição da imagem de fundo: Com background-repeat, você pode definir se a imagem de fundo deve se repetir, não se repetir (no-repeat), ou repetir apenas na horizontal ou vertical. Por exemplo:
```css
background-repeat: repeat-x;/*Repete na horizontal, vertical ou ambas.*/
```
</br>

- Posicionar a imagem de fundo: A propriedade background-position permite que você defina a posição inicial da imagem de fundo. Por exemplo:

```css
background-position: center top ;/*Posição do fundo em relação ao topo e esquerda da tela.*/
```
</br>

- Fixar o plano de fundo: Com background-attachment, você pode controlar se o plano de fundo rola com o conteúdo da página ou permanece fixo enquanto a página é rolada. Por exemplo:
```css
background-attachment: fixed;/*Fica fixa no scroll.*/
```
</br>

- Definir o tamanho da imagem de fundo: Use background-size para controlar o tamanho da imagem de fundo em relação ao elemento. Por exemplo:
```css
background-size: cover;/*Tamanho de imagem para o background ser ajustado automaticamente.*/
```
</br>

- Definir o tamanho da imagem de fundo: Use background-size para controlar o tamanho da imagem de fundo em relação ao elemento. Por exemplo:
```css
background-clip: border-box;/*Define se o conteúdo será recortado com base nos limites das bordas (border)
```

</br>

- Controlar a opacidade do plano de fundo: A opacidade do plano de fundo pode ser ajustada usando a propriedade opacity. No entanto, lembre-se de que isso afetará não apenas o plano de fundo, mas todo o elemento e seu conteúdo. A propriedade background também permite agrupar várias configurações relacionadas ao plano de fundo em uma única declaração, tornando o código CSS mais conciso e legível. Por exemplo:
```css
background: url('imagem.jpg') center top no-repeat fixed;
```
</br>

### O uso adequado da propriedade background é fundamental para criar designs atraentes e personalizados em suas páginas da web, adicionando profundidade e estilo aos elementos. Ela oferece grande flexibilidade para estilizar o fundo de elementos HTML de acordo com suas necessidades de design.
## Anotações Gerais CSS
**Funções:** Estilizar elementos HTML, controle de layout, animações e transições, pseudoclasses e pseudoelementos, estilos de formulários, transformações e efeitos 2D/3D, controle de impressão.

### Exemplo passado na aula 
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .bgFoto {
            background-color: beige;
            background-image: url("assets/fundo.png");
            background-repeat: no-repeat;
            background-position: center top;
            background-attachment: fixed;
            background-size: 1000px;
            opacity: 30%;
            /*
            background-size: auto 1000px;
            background-size: cover;
            
            */
        }

        .bgColor{
            background-color: beige;
            height: 100vh;
        }

    

 

        #titulo2{
            background-color: aqua;
        }
    </style>

</head>

<body>
    <section class="bgFoto" >
        <h1>teste</h1>

        <h1>Meu Titulo Exemplo</h1>

        <h1 id="titulo2">Meu Titulo Exemplo</h1>

        <h1 id="titulo3">Meu Titulo Exemplo</h1>

        <h1 id="titulo4">Meu Titulo Exemplo</h1>

        <h1 id="titulo5">Meu Titulo Exemplo</h1>

        <h1>The background-attachment Property</h1>

        <p id="idPgr">The background-attachment property specifies whether the background image should scroll or be
            fixed (will not scroll with the rest of the page).</p>

        <p><strong>Tip:</strong> If you do not see any scrollbars, try to resize the browser window.</p>

        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>
        <p>The background-image scrolls. Try to scroll down the page.</p>


    </section>
    <section class="bgColor">
        <h1>Titulço session 2</h1>
    </section>


</body>

</html>
```

</br>

## Textos

#### O CSS (Cascading Style Sheets) oferece várias propriedades que permitem estilizar e formatar texto em uma página da web. Essas propriedades permitem controlar a cor do texto, o tamanho da fonte, o espaçamento entre linhas e palavras, o estilo da fonte, entre outras características. Aqui estão algumas das propriedades CSS mais comuns para estilizar textos:

- color: Define a cor do texto. Você pode usar nomes de cores, códigos de cores em hexadecimal, RGB, RGBA ou HSL para especificar a cor do texto. Exemplo:

```css
color: blue;
```
</br>

- font-family: Especifica a família de fontes a ser usada para o texto. Você pode fornecer uma lista de fontes em ordem de preferência, separadas por vírgulas, para que o navegador escolha a primeira fonte disponível. Exemplo:
```css
font-family: 'Times New Roman', Times, serif; /* fonte padrão */
```

</br>

- font-size: Define o tamanho da fonte. Você pode usar unidades como pixels, ems ou porcentagens para definir o tamanho. Exemplo:

```css
font-size: 16px;
```
</br>

- font-weight: Controla a espessura da fonte, como "normal", "bold", "lighter" ou valores numéricos como 100, 200, etc. Exemplo:

```css
font-weight: bold;
```
</br>

- font-style: Define o estilo da fonte, como "normal", "italic" ou "oblique" Exemplo:
```css
font-style: italic;
```
</br>

- text-align: Especifica o alinhamento horizontal do texto dentro de seu contêiner, com opções como "left", "right", "center" ou "justify". Exemplo:

```css
text-align: center;
```
</br>

- line-height: Controla a altura da linha, que é a distância vertical entre as linhas de texto. Você pode definir um valor específico ou usar unidades como "em" ou porcentagens. Exemplo:

```css
line-height: 1.5;
```
</br>

- text-decoration: Define decorações de texto, como "underline" (sublinhado), "overline" (sobrescrito) e "line-through" (riscado). Você também pode especificar a cor e o estilo da linha. Exemplo:

```css
text-decoration: underline dotted red;
```
</br>

- text-transform: Controla a transformação do texto, como "uppercase" (maiúsculas), "lowercase" (minúsculas) ou "capitalize" (a primeira letra de cada palavra em maiúscula). Exemplo:

```css
text-transform: uppercase;
```
</br>

- letter-spacing: Define o espaçamento entre as letras do texto. Isso pode ser usado para ajustar o rastreamento do texto. Exemplo:

```css
letter-spacing: 2px;
```
</br>

#### Essas são apenas algumas das propriedades CSS que podem ser usadas para estilizar textos em uma página da web. Ao combinar essas propriedades, você pode criar uma ampla variedade de estilos de texto para atender às necessidades de design do seu site.

#### Exemplo feito na aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
    <style>

        .altura100{
            height: 100px;
            background-color: bisque;
        }

        h1{
            background-color: aquamarine;
            color: red;
            /*Alinhamento */
            text-align: center; /*left, right, center*/

            /*Text Decoration*/
            text-decoration-line: overline line-through;
            text-decoration-color: black;
            text-decoration-style: double;
            text-decoration-thickness: 1px;
            text-decoration: underline red wavy 1px;

            /*Transformações de Texto*/
            text-transform: capitalize;/*uppercase; lowercase*/
            
        }

        h2{
            /*text-shadow: 2px 2px 5px red;*/
            text-shadow: 0 0 3px #ff0000, 0 0 5px #0000ff;
        
        }

        p{
            text-align: justify; /*left, right, center, justify*/
            /*direction: rtl;*/

            /*Espaçamento */
            text-indent: 30%;
            letter-spacing: 3px;
            line-height: 20px;
            word-spacing: 15px;
            white-space: nowrap; /*impede quebra de linha forçando o scroll horizontal*/

        }

        a{
            text-decoration: none;
        }

    </style>

</head>
<body>
    <div class="altura100" id="idUnico">
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Deserunt, iusto?</p>
        
    </div>
    <h1>titulo teste</h1>

    <h2>Teste Titulop 2</h2>

    <p><a href="">link qualquer</a></p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Accusamus quisquam ad expedita numquam! Officia, libero sint? Beatae assumenda quis aliquid maxime consequuntur quam aperiam minus odit incidunt, enim autem ipsam?</p>

</body>
</html>
```
</br>

## Propriedade color no CSS

#### No CSS (Cascading Style Sheets), a propriedade color é usada para definir a cor do texto de um elemento HTML. Essa propriedade é fundamental para controlar a aparência dos textos em uma página da web. Aqui está uma explicação detalhada sobre a propriedade color no CSS:

#### A propriedade color permite especificar a cor do texto dentro de um elemento HTML. Você pode usar várias formas de definir cores, incluindo:

- Nomes de Cores: Você pode usar nomes de cores predefinidos, como "red" (vermelho), "blue" (azul), "green" (verde) e muitos outros. Aqui estão alguns exemplos:

```css
color: red;
color: blue;
color: green;
```
</br>

- Códigos de Cores em Hexadecimal: Os códigos de cores em hexadecimal são representados por uma combinação de seis caracteres, que podem incluir números (0-9) e letras (A-F). Por exemplo:

```css
color: #FF0000; /* Vermelho */
color: #0000FF; /* Azul */
```
</br>

- Valores RGB (Red, Green, Blue): Você pode especificar uma cor usando valores RGB, onde você define a intensidade de vermelho (R), verde (G) e azul (B). Cada valor varia de 0 a 255. Por exemplo:

```css
color: rgb(255, 0, 0);   /* Vermelho */
color: rgb(0, 0, 255);   /* Azul */
```
</br>

- Valores RGBA (Red, Green, Blue, Alpha): Os valores RGBA são semelhantes aos valores RGB, mas incluem um quarto valor para a transparência (alfa) da cor, variando de 0 a 1. Isso permite que você crie cores semitransparentes. Por exemplo:
```css
color: rgba(255, 0, 0, 0.5); /* Vermelho com 50% de transparência */
```
</br>

- A propriedade color pode ser aplicada a qualquer elemento HTML, como < p >, < h1 >, < a >, e assim por diante. Ela afeta a cor do texto dentro desse elemento e também pode ser herdada por elementos filhos, a menos que sejam substituídas por outra definição de cor. Exemplo de uso da propriedade color:

```css
p {
  color: #333; /* Define a cor do texto de todos os parágrafos para um tom de cinza */
}

a {
  color: blue; /* Define a cor dos links para azul */
}

h1 {
  color: rgba(255, 0, 0, 0.8); /* Define a cor do texto de cabeçalho H1 como vermelho com 80% de transparência */
}
```
</br>

#### A propriedade color é uma das ferramentas fundamentais para estilizar textos e criar layouts visualmente atraentes em uma página da web. Ela permite uma ampla variedade de opções de design, dependendo das necessidades do seu projeto.

#### Exemplo feito na aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>

        .rgb_d{
     
            color: rgba(156, 192, 66, 0.708); 
        }

        
        .rgb_h{                                    
            color: #ff0000;
        }
        
        .hsl{
            color: hsl(0, 38.05%, 38%);
        }

        .hsla{
            color: hsla(0, 38.05%, 38%, 0.5);

            color: hwb(0, 50%, 25%);

            color: lab(0, 50%, 25%);

        }


    </style>
</head>
<body>
    <p class="rgb_d">Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam, veniam!</p>

    <p class="rgb_h">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat, harum.</p>

    <p class="hsl">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Similique provident autem impedit nostrum, expedita accusamus recusandae, cum cupiditate commodi soluta voluptate eligendi harum consequuntur neque incidunt asperiores voluptates! Iste, at.</p>
    <p class="hsla">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Similique provident autem impedit nostrum, expedita accusamus recusandae, cum cupiditate commodi soluta voluptate eligendi harum consequuntur neque incidunt asperiores voluptates! Iste, at.</p>


</body>
</html>
```
</br>

## Propriedade Fonte 

#### A propriedade font permite definir várias características da fonte, como a família da fonte, o tamanho da fonte, o estilo da fonte (negrito ou itálico) e outras propriedades relacionadas à fonte. Vamos explorar as principais partes da propriedade font:

#### A propriedade font pode ser dividida em várias partes, separadas por espaços, e cada parte controla um aspecto diferente da fonte. A ordem das partes não é rígida, mas é recomendável seguir a ordem convencional para facilitar a leitura e a manutenção do código. Aqui estão as partes comuns da propriedade font:

- font-style: Define o estilo da fonte, como "normal", "italic" (itálico) ou "oblique" (obliqua).

- font-variant: Controla se a fonte deve ser exibida em versão pequena de maiúsculas ("small-caps").

- font-weight: Define a espessura da fonte, como "normal", "bold" (negrito), "bolder", "lighter" ou valores numéricos (por exemplo, 100, 200, 300, etc.).

- font-size: Especifica o tamanho da fonte. Você pode usar unidades como pixels, ems ou porcentagens para definir o tamanho da fonte.

- line-height: Define a altura da linha, que é a distância vertical entre as linhas de texto. Pode ser especificado como um valor numérico, uma unidade de medida ou uma porcentagem.

- font-family: Especifica a família de fontes a ser usada. Você pode fornecer uma lista de fontes em ordem de preferência, separadas por vírgulas. O navegador usará a primeira fonte disponível na lista.

##### Aqui está um exemplo de uso da propriedade font:

```css
p {
  font: italic small-caps bold 16px/1.5 "Helvetica Neue", Arial, sans-serif;
}
```
</br>

##### Neste exemplo:

- font-style é definido como "italic" (itálico).
- font-variant é definido como "small-caps" (versão pequena de maiúsculas).
- font-weight é definido como "bold" (negrito).
- font-size é definido como "16px".
line-height é definido como "1.5" (1,5 vezes a altura da fonte).
- font-family é definido como "Helvetica Neue", "Arial" e, se nenhuma dessas fontes estiver disponível, a família sans-serif genérica será usada como uma alternativa.

#### A propriedade font oferece uma maneira conveniente de definir várias características da fonte em uma única linha de código. Você pode ajustar essas partes de acordo com as necessidades de design do seu projeto para garantir que o texto seja estilizado da maneira desejada.

### Podemos utilizar font do Google Fontes

#### O Google Fonts é uma ótima maneira de incorporar fontes personalizadas em seu site usando CSS. Ele oferece uma ampla variedade de fontes gratuitas que podem ser usadas para melhorar a tipografia e o design do seu site. Aqui estão os passos básicos para usar fontes do Google Fonts em seu projeto:

#### Escolher Fontes: 
- Visite o site do Google Fonts.
- Explore a coleção de fontes disponíveis e escolha as que você deseja usar em seu site. 
- Você pode adicionar várias fontes ao seu projeto.

#### Adicionar Fontes ao seu Projeto:
- Clique no botão "Selecionar Este Estilo" ao lado da fonte que você deseja usar.
- Na parte inferior da página, você verá um painel que mostra as fontes selecionadas.
- Clique no ícone de carrinho de compras no painel para abrir a barra lateral "Famílias Selecionadas".

#### Personalizar Opções (opcional):
- Na barra lateral "Famílias Selecionadas", você pode personalizar as opções, como pesos e estilos específicos das fontes.
#### Incorporar as Fontes no seu HTML:

- No mesmo painel, você verá um trecho de código CSS para incorporar as fontes ao seu projeto. Ele se parece com isto:

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=NOME_DA_FONTE">
```
</br>

##### Substitua "NOME_DA_FONTE" pelo nome da fonte que você selecionou.

#### Adicionar Estilos de Fonte ao seu CSS:

- Agora que você incorporou a fonte no seu HTML, você pode usá-la em seu CSS, definindo a fonte para os elementos desejados. Por exemplo:
```css
body {
  font-family: 'NOME_DA_FONTE', sans-serif;
}
```
</br>

##### Lembre-se de substituir "NOME_DA_FONTE" pelo nome real da fonte que você escolheu.

#### Atualizar seu Site:
- Com as fontes incorporadas e os estilos aplicados, atualize seu site. As fontes personalizadas do Google Fonts agora devem estar visíveis em seu design.

#### Usar fontes do Google Fonts é uma maneira eficaz de tornar seu site mais atraente e distinto, além de melhorar a legibilidade do texto. Certifique-se de que as fontes escolhidas se adequem ao estilo e ao propósito do seu site, e ajuste o tamanho e outros estilos conforme necessário para obter o resultado desejado.

#### Exemplo feito pelo professor na aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Qwitcher+Grypen:wght@700&display=swap" rel="stylesheet">


    
    <style>
        div{
            font-size: 25px;
        }

        .font01{
            font-style: italic;
            font-variant: normal;
            font-weight: 800;
            font-size: 0.5em;
            font-family: 'Courier New', Courier, 'lucida console', monospace;
        }
        
        .font02{
            font-family: 'Roboto', sans-serif;
            font-weight: lighter;
        }

        .font03{
            font-family: 'Qwitcher Grypen', cursive;
        }

        .font04{
            font: italic small-caps lighter 25px/30px 'Shadows Into Light', cursive;
        }
        

        
    </style>
</head>
<body>
    <div>
        <p class="font01">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ducimus, alias.</p>
    </div>
    <p class="font02">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ducimus, alias.</p>
    <p class="font03">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ducimus, alias.</p>
    <p class="font04">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ducimus, alias.</p>


</body>
</html>
```
</br>

## CSS Box Model
#### O Modelo de Caixa (Box Model) é um conceito fundamental no CSS (Cascading Style Sheets) que descreve como os elementos HTML são renderizados e ocupam espaço em uma página da web. O Modelo de Caixa trata cada elemento HTML como se estivesse contido dentro de uma caixa retangular, e essa caixa é composta por várias partes principais, cada uma com sua própria função. As principais partes do Modelo de Caixa são:

- Conteúdo (Content): O conteúdo de um elemento, como texto, imagens, vídeos, ou outros elementos HTML, é a parte central da caixa. É onde o conteúdo real do elemento é exibido.
Padding:

- O preenchimento (padding) é uma área transparente ao redor do conteúdo, entre o conteúdo e a borda da caixa. Ele é usado para criar espaço interno dentro do elemento e separar o conteúdo das bordas.

- Borda (Border): A borda é uma linha que envolve o conteúdo e o preenchimento. Ela é opcional e pode ser estilizada com cores, estilos e larguras diferentes para criar efeitos visuais.

- Margem (Margin): A margem é uma área transparente ao redor da borda da caixa. Ela é usada para criar espaço entre elementos e controlar o espaçamento entre caixas adjacentes.

#### Quando você aplica estilos CSS a um elemento HTML, esses estilos afetam diretamente o Modelo de Caixa do elemento. Por exemplo, você pode definir a largura e a altura da caixa, adicionar preenchimento, criar bordas e controlar a margem ao redor do elemento. Aqui estão algumas propriedades CSS comuns que afetam o Modelo de Caixa:

- width e height: Define a largura e a altura da caixa de conteúdo.
- padding: Define o preenchimento da caixa, controlando a distância entre o conteúdo e a borda.
- border: Define a aparência da borda da caixa.
- margin: Define a margem ao redor da caixa, controlando o espaço entre caixas adjacentes.

![Box Model CSS](https://miro.medium.com/v2/resize:fit:720/format:webp/1*kGMWtZihmaUhxZI5ZVicLA.png)


#### Além disso, o Modelo de Caixa pode ser influenciado por outras propriedades CSS, como box-sizing, que controla como as dimensões (largura e altura) da caixa são calculadas, levando em consideração ou não o preenchimento e a borda.

É importante entender o Modelo de Caixa ao trabalhar com CSS, pois ele afeta a aparência e o layout de todos os elementos na página da web. Ao controlar as dimensões e espaçamento das caixas, você pode criar layouts responsivos e designs atraentes para o seu site.
### Exemplo feito na aula 

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>

        *{
            border: 0;
            margin: 0;
            padding: 0;
        }

        p{
            border-style: dashed;
            border-color: blue;
            border-width: 10px;


            border-top-style: solid;
            border-bottom-style: dotted;

            border-left-color: blueviolet;
            border-right-width: 2px;

            padding: 15px;
            padding-left: 30px;
            padding-top: 50px;
            padding-bottom: 60px;
            padding-right: 40px;

            margin: 30px;


            outline-style: solid;
            outline-color: red;
            outline-width: thin;

        }


        div{
            height: 100px; 
            width: 100px;

            border-color: brown;
            border-style: solid;
            border-width: 5px;
            border-radius: 50%;

            border-top-style: dotted;

            margin: 30px;

        }

        section{
            height: 100px;
            width: 100px;
            border: 5px solid red; 
            border-radius: 15px;

            margin: 50px;
        }

    </style>
</head>
<body>
    <p>lorem ipsum et</p>

    <div></div>

    <section></section>
</body>
</html>
```
</br>
## Propriedade Link 

#### A propriedade a é usada para estilizar os links em uma página da web. Essa propriedade permite que você controle a aparência de links de hipertexto, incluindo a cor do texto, a decoração do link (como sublinhado), o estilo do cursor quando o mouse passa sobre o link e outros aspectos relacionados à aparência dos links.

#### Aqui estão algumas das propriedades CSS mais comuns que podem ser aplicadas aos links:

- color: Define a cor do texto do link. Você pode usar nomes de cores, códigos de cores em hexadecimal, RGB ou outras notações de cores. Exemplo:

```css
a {
  color: blue;
}
```
</br>
- text-decoration: Controla a decoração do link, como sublinhado ou riscado. Você pode usar valores como "none" (nenhum), "underline" (sublinhado) ou "line-through" (riscado). Exemplo:

```css
a {
  text-decoration: none; /* Remove a decoração de sublinhado padrão */
}
```
</br>
- font-weight: Define a espessura da fonte para links. Você pode usar valores como "normal", "bold" (negrito) ou "bolder".

```css
a {
  font-weight: bold;
}
```
</br>

- cursor: Controla o estilo do cursor quando o mouse passa sobre o link. Isso pode ser usado para indicar que um link é clicável. Exemplo:

```css
a {
  cursor: pointer; /* Altera o cursor para uma mãozinha quando passar sobre o link */
}
```
</br>

- :hover: O pseudo-classe :hover permite que você aplique estilos específicos quando o mouse passa sobre o link. Isso é útil para criar efeitos visuais interativos. Exemplo:

```css
a:hover {
  color: red; /* Muda a cor do texto para vermelho quando o mouse passa sobre o link */
}
```
</br>

- visited: O pseudo-classe :visited permite estilizar links que já foram visitados pelo usuário. Isso pode ser útil para indicar visualmente os links já acessados. Exemplo:

```css
a:visited {
  color: gray; /* Define a cor para cinza para links visitados */
}
```
</br>

- active: O pseudo-classe :active estiliza um link quando ele está sendo clicado ou ativado. Isso pode ser usado para dar feedback imediato ao usuário quando ele clica em um link. Exemplo:

```css
a:active {
  background-color: yellow; /* Define o fundo como amarelo quando o link é clicado */
}
```
</br>

#### Essas são algumas das propriedades e pseudo-classes CSS comuns usadas para estilizar links em uma página da web. Personalizar a aparência dos links é importante para a usabilidade e a estética do seu site, além de tornar a experiência do usuário mais agradável e informativa.

#### Exemplo feito na aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        .menu {
            display: flex;
        }

        .menu li {
            margin: 5px;
            list-style: none;
        }

        a:link, a:visited {
            background-color: white;
            color: black;
            border: 2px solid green;
            padding: 10px 20px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
        }

        a:hover, a:active {
            background-color: green;
            color: white;
        }


        /*
        a:link{
            color: red;
            text-decoration: none;

        }

        a:visited{
            color:aquamarine;

        }

        a:hover{
            color: rgb(97, 159, 165);
            text-decoration: underline;

        }

        a:active{
            color: greenyellow;
            background-color: aqua;

        }

        */
    </style>

</head>
<body>

    <header>
        <nav>
            <ul class="menu">
                <li><a href="#1">Home</a></li>
                <li><a href="#2">Contato</a></li>
                <li><a href="#3">Sobre</a></li>
            </ul>
        </nav>
    </header>
    
</body>
</html>
```

</br>

## Listas

#### Você pode estilizar listas HTML, como listas ordenadas (< ol >) e listas não ordenadas (< ul >), bem como os itens de lista (< li >). Isso permite que você personalize a aparência das listas em sua página da web de acordo com as necessidades de design do seu projeto. Aqui estão algumas das propriedades CSS comuns usadas para estilizar listas:

#### list-style-type: Define o estilo dos marcadores (para listas não ordenadas) ou dos números/letras (para listas ordenadas). Alguns valores comuns incluem:

- disc: Marcadores de pontos (padrão para listas não ordenadas).
- circle: Círculos vazios.
square: Quadrados vazios.
- decimal: Números decimais (padrão para listas ordenadas).
- lower-roman: Números romanos minúsculos em ordem.
- upper-alpha: Letras maiúsculas em ordem alfabética.
##### Exemplo:

```css
ul {
  list-style-type: square; /* Define marcadores de quadrados para listas não ordenadas */
}

ol {
  list-style-type: upper-roman; /* Define números romanos maiúsculos para listas ordenadas */
}
```
</br>

- list-style-image: Permite usar uma imagem personalizada como marcador de lista. Você pode fornecer o URL da imagem desejada. Exemplo:

```css
ul {
  list-style-image: url('icone.png'); /* Usa uma imagem personalizada como marcador */
}
```
</br>

- list-style-position: Controla a posição dos marcadores em relação ao texto dos itens de lista. Pode ser inside (dentro do espaço da margem) ou outside (fora do espaço da margem). Exemplo:

```css
ul {
  list-style-position: outside; /* Coloca os marcadores fora do espaço da margem */
}
```
</br>

- padding-left: Define o espaço à esquerda dos itens de lista. Isso permite controlar o recuo dos itens de lista em relação à margem esquerda. Exemplo:

```css
ul {
  padding-left: 20px; /* Define um recuo de 20 pixels para a lista não ordenada */
}
```
</br>

- margin: Define as margens ao redor da lista. Isso permite controlar o espaçamento entre a lista e os elementos vizinhos. Exemplo:

```css
ul {
  margin: 10px 0; /* Define margens superior e inferior de 10 pixels e margens laterais de 0 */
}
```
</br>

- border: Define uma borda ao redor da lista. Isso pode ser usado para criar separadores visuais entre listas e outros conteúdos. Exemplo:

```css
ul {
  border: 1px solid #ccc; /* Cria uma borda sólida cinza ao redor da lista não ordenada */
}
```
</br>

color e font: Você também pode aplicar propriedades de cores e fontes aos itens de lista e ao texto dentro deles para personalizar ainda mais a aparência das listas. Exemplo:

```css
li {
  color: blue; /* Define a cor do texto dos itens de lista para azul */
  font-size: 16px; /* Define o tamanho da fonte dos itens de lista */
}
```
</br>

#### Estas são algumas das propriedades CSS comuns usadas para estilizar listas em HTML. Personalizar a aparência das listas pode melhorar a legibilidade e a estética de seu conteúdo, tornando-o mais atraente e adaptado ao estilo do seu site.

#### Exemplo feito na aula 

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>

        .menu{
            display: flex;
            list-style-type: none;
        }
        
        .menu li{
            margin: 5px;  
        }

        .lista{
            list-style-type: lower-greek;
            list-style-image: url("assets/index.gif");
            list-style-position: inside;

            padding: 25px;
            margin: 10px;
            background-color: violet;

        }

        .lista li{
            background-color: thistle;
            padding: 3px;
            margin: 5px;
        }

    </style>

</head>
<body>

    <header>
        <nav>
            <ul class="menu">
                <li>menu-1</li>
                <li>menu-2</li>
                <li>menu-3</li>
            </ul>
        </nav>
    </header>


    <ul class="lista">
        <li>item-1</li>
        <li>item-2</li>
        <li>item-3</li>
        <li>item-4</li>
        <li>item-5</li>
    </ul>
    
</body>
</html>
```
## Tabelas 

#### Você pode estilizar tabelas HTML para personalizar a aparência delas em uma página da web. As tabelas são uma parte fundamental do layout e do design de muitos sites, e o CSS oferece uma ampla variedade de propriedades que permitem controlar a estética e o comportamento das tabelas. Aqui estão algumas das propriedades CSS mais comuns usadas para estilizar tabelas:

- border-collapse: Controla a forma como as bordas das células da tabela são renderizadas. O valor padrão é separate, que cria espaços entre as bordas das células. Você pode definir como collapse para que as bordas se fundam, criando uma aparência mais limpa e consistente Exemplo:

```css
table {
  border-collapse: collapse;
}
```

</br>

- border: Define a espessura, o estilo e a cor das bordas das células da tabela. Isso permite criar tabelas com bordas personalizadas. Exemplo:

```css
table, th, td {
  border: 1px solid #ccc; /* Define uma borda sólida cinza para a tabela e suas células */
}
```
</br>

- background-color: Define a cor de fundo da tabela, das células da tabela ou de células individuais. Exemplo:

```css
table {
  background-color: #f2f2f2; /* Define um fundo cinza claro para a tabela */
}
th {
  background-color: #333; /* Define um fundo preto para os cabeçalhos da tabela */
  color: white; /* Define a cor do texto para branco nos cabeçalhos */
}
```
</br>


- text-align: Controla o alinhamento horizontal do texto nas células da tabela, incluindo os cabeçalhos e o conteúdo das células. Exemplo:

```css
th, td {
  text-align: center; /* Centraliza o texto nas células da tabela */
}
```
</br>

- padding: Define o espaçamento entre o conteúdo das células e suas bordas. Isso pode ser usado para controlar o espaçamento interno das células. Exemplo:

```css
td {
  padding: 10px; /* Define 10 pixels de espaço interno em todas as células de dados */
}
```
</br>

- width e height: Especificam a largura e a altura da tabela ou de células individuais. Isso permite controlar o dimensionamento das tabelas. Exemplo:

```css
table {
  width: 100%; /* Define a largura da tabela como 100% da largura do contêiner pai */
}

td {
  width: 50px; /* Define a largura de todas as células de dados como 50 pixels */
}
```
</br>

- color e font: Você também pode aplicar propriedades de cores e fontes às células da tabela e ao texto dentro delas para personalizar ainda mais a aparência das tabelas. Exemplo:

```css
td {
  color: #333; /* Define a cor do texto nas células de dados */
  font-size: 14px; /* Define o tamanho da fonte nas células de dados */
}
```
</br>

#### Estas são algumas das propriedades CSS comuns usadas para estilizar tabelas em HTML. Personalizar a aparência das tabelas é importante para melhorar o layout e a legibilidade do conteúdo da sua página da web, tornando-a mais atraente e alinhada com o design geral do site.

#### Exemplo feito na aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>

        table {
            empty-cells: hide;
        }

        table, th, td{
            border-style: solid;
            border-top-style: dotted;
        }

        th{
            padding-left: 25px;
            padding-right: 25px;
            line-height: 25px;
            background-color: black;
            color: antiquewhite;
            border-color: brown;
        }

        tr{
            background-color: chartreuse;
        }

        td:hover{
            background-color: thistle;
        }

        tr:nth-child(odd){ /*even, odd, 3n, 4, 2n + 1...*/
            background-color: bisque;
        }

        td{
            height: 50px;
            width: 200px;
            text-align: center;
            vertical-align: top;
        }

        .tabs{
            width: 100vw;
            height: 30vh;
            overflow-y: auto;
            overflow-x: auto;
        }


    </style>


</head>
<body>
    <h1>titulo 1</h1>
    
    <div class="tabs">
        <table>
            <tr>
                <th>Firstname</th>
                <th>Lastname</th>
                <th>Firstname</th>
                <th>Lastname</th>
                <th>Firstname</th>
                <th>Lastname</th>
                <th>Firstname</th>
                <th>Lastname</th>
                <th>Firstname</th>
                <th>Lastname</th>
                <th>Firstname</th>
                <th>Lastname</th>
                <th>Firstname</th>
                <th>Lastname</th>
            </tr>
            <tr>
                <td></td>
                <td></td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Lois</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Lois</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Lois</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Lois</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Lois</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Lois</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Lois</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Lois</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Lois</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Lois</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Lois</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Lois</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
        </table>
    </div>

    <div class="tabs">
        <table cellspacing="15px">
            <tr>
                <th>Firstname</th>
                <th>Lastname</th>
                <th>Firstname</th>
                <th>Lastname</th>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
            <tr>
                <td>Peter</td>
                <td>Griffin</td>
                <td>Peter</td>
                <td>Griffin</td>
            </tr>
        </table>
    </div>

    <h2>titulo 2</h2>
</body>
</html>
```

## Filtros 

#### Filtros em CSS são propriedades que permitem aplicar efeitos visuais a elementos HTML, como imagens, usando efeitos de processamento de imagem. Eles são úteis para criar efeitos de imagem, como ajuste de cores, desfoque, nitidez e muito mais, diretamente no navegador, sem a necessidade de software de edição de imagem. Aqui estão algumas das propriedades de filtro mais comuns em CSS:

</br>

- blur(): Esta função aplica um desfoque à imagem, criando uma aparência desfocada. O valor determina o grau de desfoque aplicado. Exemplo:

```css
img {
  filter: blur(5px); /* Aplica um desfoque de 5 pixels à imagem */
}
```
</br>

- brightness(): Esta função ajusta o brilho da imagem. Um valor de 100% mantém o brilho original, valores menores tornam a imagem mais escura e valores maiores tornam a imagem mais brilhante. Exemplo:

```css
img {
  filter: brightness(150%); /* Aumenta o brilho da imagem em 50% */
}
```
</br>

- contrast(): Esta função ajusta o contraste da imagem. Um valor de 100% mantém o contraste original, valores menores reduzem o contraste e valores maiores aumentam o contraste. Exemplo:

```css
img {
  filter: contrast(150%); /* Aumenta o contraste da imagem em 50% */
}
```
</br>

- grayscale(): Esta função converte a imagem em tons de cinza. Um valor de 0% mantém a imagem colorida, enquanto 100% a transforma em uma imagem em preto e branco. Exemplo:

```css
img {
  filter: grayscale(100%); /* Converte a imagem em preto e branco */
}
```
</br>

- hue-rotate(): Esta função ajusta o matiz (cor) da imagem em graus. Ela permite que você faça a imagem parecer ter cores diferentes. Exemplo:

```css
img {
  filter: hue-rotate(90deg); /* Rotaciona a matriz de cores da imagem em 90 graus (torna-a mais verde) */
}
```
</br>

- invert(): Esta função inverte as cores da imagem, criando um efeito de negativo Exemplo:

```css
img {
  filter: invert(100%); /* Inverte as cores da imagem */
}
```
</br>

- opacity(): Esta função ajusta a opacidade da imagem. Um valor de 0% torna a imagem completamente transparente, enquanto 100% a torna totalmente visível. Exemplo:

```css
img {
  filter: opacity(50%); /* Torna a imagem 50% transparente */
}
```
</br>

- saturate(): Esta função controla a saturação da imagem. Valores menores reduzem a saturação, enquanto valores maiores aumentam a saturação. Exemplo:

```css
img {
  filter: saturate(200%); /* Aumenta a saturação da imagem em 100% */
}
```
</br>

#### Esses filtros podem ser aplicados a uma ampla variedade de elementos, não apenas a imagens, e podem ser usados em combinação para criar efeitos visuais complexos. Lembre-se de que a compatibilidade do navegador pode variar, portanto, é importante verificar se os navegadores que você deseja atingir suportam os filtros CSS que você está usando.

#### Exemplo feito em aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        img{
            width: 400px;
        }

        label{
            display: block;
        }

        .clOpacity{
            opacity: 0.3;
        }

        .clBlur{
            filter: blur(5px);
        }

        .clBrightness{
            filter: brightness(2);
        }

        .clContrast{
            filter: contrast(1.2);
        }

        .clGrascale{
            filter:grayscale(0.2);
        }

        .clInvert{
            filter:invert();
        }

        .clSaturate{
            filter:saturate(2);
        }

        .clSepia{
            filter:sepia(0.5);
        }

        .clDropShadow{
            filter: drop-shadow(15px 25px 25px rgb(127, 125, 127))
        }

        .clHueRotate{
            filter: hue-rotate(240deg);
        }

        .clCombo{
            filter: blur(5px) opacity(0.5) grayscale(0.8);
        }



    </style>

</head>
<body>
    <div>
        <label for="">Opacity...</label>
        <img src="assets/Foto1.JPG" alt="Voando de Parapente" class="clOpacity">
    </div>
    <div>
        <label for="">Blur...</label>
        <img src="assets/Foto2.JPG" alt="Caiaque" class="clBlur">
    </div>
    <div>
        <label for="">Brightness...</label>
        <img src="assets/Foto1.JPG" alt="Voando de Parapente" class="clBrightness">
    </div>
    <div>
        <label for="">Contrast...</label>
        <img src="assets/Foto2.JPG" alt="Caiaque" class="clContrast">
    </div>
    <div>
        <label for="">Grascale...</label>
        <img src="assets/Foto1.JPG" alt="Voando de Parapente" class="clGrascale">
    </div>
    <div>
        <label for="">Invert...</label>
        <img src="assets/Foto2.JPG" alt="Caiaque" class="clInvert">
    </div>
    <div>
        <label for="">Saturate...</label>
        <img src="assets/Foto1.JPG" alt="Voando de Parapente" class="clSaturate">
    </div>
    <div>
        <label for="">Sepia...</label>
        <img src="assets/Foto2.JPG" alt="Caiaque" class="clSepia">
    </div>
    <div>
        <label for="">DropShadow...</label>
        <img src="assets/Foto1.JPG" alt="Voando de Parapente" class="clDropShadow">
    </div>
    <div>
        <label for="">HueRotate...</label>
        <img src="assets/Foto2.JPG" alt="Caiaque" class="clHueRotate">
    </div>   
    <div>
        <label for="">Combo...</label>
        <img src="assets/Foto1.JPG" alt="Voando de Parapente" class="clCombo">
    </div>   
</body>
</html>
```
</br>

## Flexbox

#### O Flexbox, ou "Flexible Box Layout," é um modelo de layout em CSS que foi projetado para facilitar o posicionamento e o dimensionamento de elementos em um contêiner de forma mais eficiente e previsível. Ele é especialmente útil para criar layouts responsivos e complexos em páginas da web. O Flexbox introduz uma maneira poderosa de organizar e alinhar elementos em uma única dimensão (linha) ou em duas dimensões (linha e coluna), proporcionando um controle significativo sobre o espaço disponível.

#### Aqui estão os principais conceitos e propriedades do Flexbox:

- Flex Container (Contêiner Flex): Um elemento que contém os itens flexíveis (filhos) e é definido como um contêiner flex usando display: flex; ou display: inline-flex;.

```css
.flex-container {
  display: flex; /* Torna este elemento um contêiner flexível */
}
```
</br>

- Flex Items (Itens Flex): Os elementos contidos dentro do contêiner flexível são chamados de itens flexíveis. Os itens flexíveis são automaticamente dimensionados para preencher o espaço dentro do contêiner.

```css
.flex-item {
  /* Estilos para itens flexíveis */
}
```
</br>

- Flex Direction (Direção Flex): Controla a direção principal na qual os itens flexíveis são dispostos dentro do contêiner. Os valores possíveis são row (padrão), row-reverse, column e column-reverse.

```css
.flex-container {
  flex-direction: row; /* Itens flexíveis são dispostos na horizontal (padrão) */
}
```
</br>

- Flex Wrap (Quebra de Linha Flex): Define se os itens flexíveis podem ser distribuídos em várias linhas ou colunas dentro do contêiner. Os valores possíveis são nowrap (padrão), wrap e wrap-reverse.

```css
.flex-container {
  flex-wrap: wrap; /* Itens flexíveis podem quebrar para a próxima linha se não couberem */
}
```
</br> 

Justify Content (Justificar Conteúdo): Controla o alinhamento dos itens flexíveis ao longo do eixo principal. Ele permite que você distribua os itens ao longo da linha ou da coluna, adicionando espaço entre ou ao redor deles.

```css
.flex-container {
  justify-content: center; /* Centraliza os itens flexíveis ao longo do eixo principal */
}
```
</br>

- Align Items (Alinhar Itens): Define como os itens flexíveis são alinhados ao longo do eixo cruzado. Isso permite ajustar verticalmente os itens dentro do contêiner.

```css
.flex-container {
  align-items: center; /* Centraliza verticalmente os itens flexíveis */
}
```
</br>

- Align Content (Alinhar Conteúdo): Controla o alinhamento dos grupos de itens flexíveis quando há espaço extra na direção da linha ou coluna. Isso é útil quando há várias linhas de itens flexíveis.

```css
.flex-container {
  align-content: space-between; /* Distribui o espaço igualmente entre as linhas de itens flexíveis */
}
```
</br>

- Flex (Flexibilidade): A propriedade flex é uma combinação das propriedades flex-grow, flex-shrink, e flex-basis. Ela permite especificar a flexibilidade de um item flexível em relação aos outros itens.

```css
.flex-item {
  flex: 1 0 auto; /* Flexibilidade igual para todos os itens, não pode diminuir e tamanho automático */
}
```
</br>

#### O Flexbox é uma ferramenta poderosa para criar layouts de página da web responsivos e complexos. Ele simplifica o design de layouts que se adaptam ao tamanho da tela ou ao conteúdo, economizando tempo e tornando o código mais legível e fácil de manter. O Flexbox é amplamente suportado pelos navegadores modernos, tornando-o uma escolha sólida para o desenvolvimento web.
</br>

#### Exemplo feito em aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .linha{
            border: 1px solid red;
            margin: 15px;
            display: flex;
            height: 300px;

            flex-direction: row;  /*column; column-reverse; row; row-reverse;*/

            
            /*Alinhamento Horizontal*/
            justify-content: flex-end;/*center; space-around; space-between; space-evenly;*/

            
            /*Alinhamento Vertical sem wrap ligado*/
            /*align-items: center;*//*center; flex-start; flex-end; stretch; baseline;*/

            /*Alinhamento Vertical com o wrap ligado*/
            align-content: space-evenly; /*center; space-between; space-around; stretch; flex-start; flex-end;*/

            /*Modo de Encapsulamento dos itens (quebra de linha...)*/
            flex-wrap: wrap; /*wrap; wrap-reverse; nowrap;*/
           
            /*Propriedade abreviada para definir as propriedades flex-directione flex-wrap.*/
           /* flex-flow: row wrap; */
        }

        .coluna{
            border: 1px solid blue;
            margin: 5px;
            padding: 15px;
        }

        /*Esxemplo 2*/
        .linha1{
            border: 1px solid red;
            margin: 15px;
            display: flex;
        }

        .coluna1{
            border: 1px solid blue;
            margin: 5px;
            padding: 15px;
        }

        #item-1{
            order: 3;
            flex-grow: 1;
            flex-shrink: 2;
        }

        #item-2{
            order: 2;
            flex-grow: 1;
            flex-shrink: 1;
            flex-basis: 200px;
        }

    </style>

</head>
<body>
    <div class="linha">
        <div class="coluna">1</div>
        <div class="coluna">2</div>
        <div class="coluna">3</div>
        <div class="coluna">4</div>
        <div class="coluna">5</div>
        <div class="coluna">6</div>
        <div class="coluna">7</div>
        <div class="coluna">8</div>
        <div class="coluna">9</div>
        <div class="coluna">10</div>
    </div>

    <div class="linha1">
        <div class="coluna1" id="item-1">Static 1</div>
        <div class="coluna1" id="item-2">Static 2</div>
        <div class="coluna1" id="item-3">Static 3</div>
    </div>

</body>
</html>
```
</br>

## Variáveis

#### Variáveis em CSS, também conhecidas como variáveis personalizadas ou "custom properties," são um recurso que permite definir valores reutilizáveis em um arquivo CSS. Essas variáveis tornam o CSS mais dinâmico, facilitando o ajuste de valores em vários lugares do seu código com facilidade. Aqui está como você pode usar variáveis em CSS:

#### Definindo Variáveis
- Para definir uma variável em CSS, use a notação --nome-variavel seguida pelo valor desejado. As variáveis CSS começam com dois hifens (--):

```css
:root {
  --cor-primaria: #3498db;
  --tamanho-fonte: 16px;
}
```

#### Neste exemplo, definimos duas variáveis: --cor-primaria com o valor #3498db e --tamanho-fonte com o valor 16px. O :root se refere ao elemento raiz do documento (geralmente o elemento < html >), onde as variáveis globais são definidas.

#### Usando Variáveis
- Depois de definir as variáveis, você pode usá-las em qualquer lugar do seu arquivo CSS usando a função var():

```css
body {
  background-color: var(--cor-primaria);
  font-size: var(--tamanho-fonte);
}
```

#### Neste exemplo, usamos as variáveis --cor-primaria e --tamanho-fonte para definir a cor de fundo do corpo e o tamanho da fonte.

#### Benefícios das Variáveis CSS
Reutilização de Valores: As variáveis permitem que você defina valores uma vez e os reutilize em todo o seu CSS. Se você precisar alterar a cor principal ou o tamanho da fonte, basta fazer a alteração em um único lugar.

#### Maior Legibilidade: O uso de variáveis torna o código mais legível e compreensível, pois os valores têm nomes descritivos em vez de valores codificados.

#### Manutenção Simplificada: As alterações de design são mais fáceis de implementar e manter, já que você só precisa atualizar os valores das variáveis em vez de percorrer todo o código em busca de valores específicos.

#### Escopo Local: As variáveis podem ser definidas em diferentes escopos, o que permite personalizar valores para componentes individuais, sem afetar o estilo global.

#### Compatibilidade com Navegadores
A maioria dos navegadores modernos suporta variáveis CSS, mas é importante verificar a compatibilidade antes de usá-las em projetos que precisam funcionar em navegadores mais antigos. Geralmente, a compatibilidade pode ser tratada com fallbacks ou polyfills para navegadores mais antigos.

#### Exemplo feito em aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* Palheta de Cores*/
        :root {
            --corPrincipal: #04C4D9;
            --corComplementar: #2E3159;
            --corComplementar2: #2e31597d;
            --corContraste1: #D94A64;
            --corContraste2: #A62F03;
            --corNeutro1: white;
            --corNeutro2: black;
            --corFundo1: #26262b;
            --corFundo2: azure;
        }

        h1 {
            color: var(--corPrincipal);
        }

        div{
            background-color: var(--corFundo1);
        }

    </style>
</head>
<body>

    <div>
        <h1>teste variáveis CSS</h1>
    </div>
    
</body>
</html>
```
</br>

## Google Calendario em CSS

#### O Google Calendar é um serviço de gerenciamento de calendário online oferecido pelo Google. Ele permite que os usuários criem eventos, lembretes e compartilhem calendários com outras pessoas. O Google Calendar é uma ferramenta web que não é estilizada diretamente com CSS, mas pode ser incorporada em um site e estilizada por meio de personalização.

#### Aqui estão as etapas gerais para incorporar e personalizar o Google Calendar em um site:

#### Incorporando o Google Calendar:

- Vá para o Google Calendar e acesse a agenda que deseja incorporar em seu site.
- No canto superior direito, clique no ícone de engrenagem e selecione "Configurações da Agenda".
- Role para baixo até a seção "Incorporar Código" e copie o código de incorporação fornecido.
- Cole esse código no HTML do seu site, onde você deseja que o calendário seja exibido.
#### Personalizando o Estilo com CSS:

#### Após incorporar o Google Calendar, você pode personalizar a aparência do calendário em seu site usando CSS. Aqui estão algumas propriedades CSS comuns que você pode usar para personalizar o estilo:

- Seletores CSS: Você pode usar seletores CSS para segmentar elementos específicos dentro do calendário incorporado, como eventos, cabeçalhos de data ou áreas de navegação.

- Propriedades CSS: Use propriedades CSS para definir cores, fontes, margens, preenchimentos e outros estilos visuais. Por exemplo, você pode definir cores de fundo e texto, tamanhos de fonte e espaçamentos.

- Mídia Responsiva: Use consultas de mídia CSS para tornar o calendário responsivo, ajustando seu estilo com base no tamanho da tela ou dispositivo.

#### Integração com a Identidade Visual do Site:

#### Certifique-se de que o estilo do calendário incorporado se alinhe com a identidade visual do seu site. Isso pode incluir o uso de cores, fontes e estilos de acordo com o tema geral do site.

#### Teste e Ajuste:

#### Após aplicar o CSS personalizado, teste o calendário em vários navegadores e dispositivos para garantir que ele seja exibido corretamente e que o estilo esteja consistente em todas as plataformas.

#### Lembre-se de que a personalização do Google Calendar incorporado usando CSS é limitada às opções fornecidas pelo próprio calendário. Você pode personalizar a aparência geral, mas não é possível fazer alterações significativas na funcionalidade do calendário usando apenas CSS. Se você precisar de personalizações mais avançadas, considere a possibilidade de usar a API do Google Calendar para criar uma solução personalizada.

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
    <!-- Google Calendar Appointment Scheduling begin -->
    <iframe src="https://calendar.google.com/calendar/appointments/schedules/AcZssZ3gc9Gj0GTJCz6gUPHhFvmb_oK5fmq6VrCu4Vs9lU9Dsghwrhk8W8x0q09vHpCVlNBRFo_pPd4l?gv=true" style="border: 0" width="100%" height="600" frameborder="0"></iframe>
    <!-- end Google Calendar Appointment Scheduling -->
</body>
</html>
```
</br>

## Landing Page

#### Uma landing page, também conhecida como página de destino, é uma página da web criada especificamente com o objetivo de converter visitantes em leads ou clientes. Ela é projetada para receber tráfego direcionado de uma fonte específica, como uma campanha de marketing, anúncio, e-mail ou mídia social, e direcionar os visitantes para uma ação desejada, como preencher um formulário, fazer uma compra ou assinar uma newsletter.

#### Aqui estão os principais elementos e características de uma landing page eficaz:

- Clareza e Foco: Uma landing page deve ter uma mensagem clara e focada. Ela deve comunicar imediatamente o que está sendo oferecido e qual é o valor para o visitante.

- Título Impactante: O título é uma parte crucial da landing page. Ele deve ser atraente, conciso e relacionado ao conteúdo da página. Um bom título pode capturar a atenção do visitante imediatamente.

- Descrição Concisa: Uma breve descrição ou subtítulo pode ser usada para expandir a mensagem do título e destacar os benefícios do que está sendo oferecido.

- Call-to-Action (CTA): A ação desejada que você quer que os visitantes realizem deve ser destacada por meio de um CTA. Isso pode ser um botão, link ou formulário de inscrição.

- Design Atraente: O design da landing page deve ser limpo, atraente e coeso com a identidade visual da marca. Use imagens, cores e tipografia de forma eficaz para criar um visual atraente.

- Conteúdo Relevante: Certifique-se de que o conteúdo da landing page seja relevante para o público-alvo. Explique os benefícios do que está sendo oferecido e responda às perguntas comuns dos visitantes.

- Formulários Simples: Se você está coletando informações por meio de um formulário, mantenha-o simples. Peça apenas as informações necessárias para a conversão.

- Depoimentos e Provas Sociais: Depoimentos de clientes satisfeitos, avaliações e logotipos de empresas parceiras podem aumentar a confiança dos visitantes.

- Remoção de Distrações: Evite distrações desnecessárias, como menus de navegação complicados ou links externos, que possam levar os visitantes para longe da página antes de realizar a ação desejada.

- Responsividade: Certifique-se de que a landing page seja responsiva e se adapte a diferentes tamanhos de tela, incluindo dispositivos móveis.

- Testes e Otimização: Realize testes A/B para otimizar elementos da página, como o texto do CTA, cores, imagens e layout, para melhorar a taxa de conversão ao longo do tempo.

- Análise de Dados: Use ferramentas de análise da web para rastrear o desempenho da landing page, como taxas de cliques, taxas de conversão e origem do tráfego. Isso ajudará a entender o que funciona e o que precisa ser ajustado.

- Personalização: Considere a personalização com base no segmento de público. Se possível, adapte a mensagem e os elementos da página de acordo com o perfil do visitante.

#### Landing pages são uma ferramenta valiosa no marketing digital, pois ajudam a direcionar o tráfego de forma eficaz e a converter visitantes em clientes ou leads. Elas são amplamente utilizadas em campanhas de publicidade online, marketing por e-mail, promoções de produtos e serviços, e muito mais. Uma landing page bem projetada e otimizada pode ser fundamental para o sucesso de uma estratégia de marketing digital.

#### Exemplo feito em aula

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Curso React 2023</title>
    <link rel="icon" type="image/x-icon" href="assets/iconmonstr-dashboard-lined-240.png">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
    <style>
        /*CSS Reset e definições Globais*/
        body,
        h1,
        p {
            margin: 0;
            font-family: 'Roboto', sans-serif;
        }

        body{
            background-color: var(--corFundo1);
        }

        /* Palheta de Cores */
        :root{
            --corPrincipal : #04C4D9;
            --corComplementar : #2E3159;
            --corComplementar2 : #2e31597d;
            --corContraste1 : #D94A64;
            --corContraste2 : #A62F03; 
            --corNeutro1: white; 
            --corNeutro2: black;
            --corFundo1: #26262b;
            --corFundo2: azure;
        }



        /* Cabeçalho, Menu, Logo */
        .cabecalho {
            background-color: var(--corPrincipal);
        }

        .barraNav {
            display: flex;
        }

        .logo img {
            width: 75px;
            margin-left: 35px;
        }

        .menu{
            width: 100%;
            margin-right: 100px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: flex-end;
        }

        .menu ul {
            list-style-type: none;
        }

        .menu ul li {
            margin-left: 15px;
            font-size: 1em;
        }

        .linkMenu:link,
        .linkMenu:visited {
            color: var(--corNeutro1);
            text-decoration: none;
            font-weight: 100;
        }

        .linkMenu:hover,
        .linkMenu:active {
            color: var(--corComplementar);
        }

        /* Primeira Dobra - #Home*/
        .secApresentacao {
            height: calc(85vh);

            background-image: url("assets/fundo.png");
            background-repeat: no-repeat;
            background-size: cover;
        }

        .bgFiltro {
            height: 100%;
            width: 100%;
            backdrop-filter: blur(5px) grayscale(0.6);
        }

        #ct3{
            margin-right: 50px;
        }

        #ct3Titulo1 {
            color: var(--corNeutro1);
            font-size: 2em;
            text-shadow: 0 0 3px black;
        }

        #ct3Texto1 {
            color: var(--corNeutro1);
            font-size: 1em;
            text-shadow: 0 0 3px black;
            margin-bottom: 20px;
        }


        /* Segunda Dobra - #Curso*/
        .secCurso {
            background-color: var(--corFundo2);
            padding-top: 70px;
        }

        .card{
           border: 3px solid var(--corComplementar);
           border-radius: 15px;
           background-color: var(--corComplementar2);
    
           color: var(--corNeutro1);
           width: 20%;
           margin: 30px;
           padding-top: 20px;
           padding-bottom: 20px;
           
        }

        .card img{
            width: 70%;
            display: flex;
            margin: 0 auto 0 auto;
        }

        .card h3{
            width: 100%;
            text-align: center;
            
        }

  
        /* Depoimentos*/
        .secDepoimentos{
            background-color: var(--corFundo2);
            padding-top: 60px;
        }

        .card2{
           color: var(--corComplementar);
           width: 20%;
           margin: 30px;
           padding-top: 20px;
           padding-bottom: 20px;
           
        }

        .card2 img{
            width: 70%;
            border-radius: 50%;
            display: flex;
            margin: 0 auto 0 auto;
        }

        .card2 h3{
            width: 100%;
            text-align: center;
        }

        /* Perguntas Frequentes - #faq*/
        .secFaq{
            background-color: var(--corFundo2);
            padding-top: 60px;
            padding-bottom: 60px;
        }

        .secFaq details{
            width: 50%;
            margin-left: 30px;
            margin-bottom: 5px;
            padding: 10px;
            border: 1px groove var(--corComplementar);
            border-radius: 15px;
            background-color: var(--corComplementar2);
            color: var(--corNeutro1);
        }

        #ctFaqDiv3{
            margin-right: 40px;
            background-color: var(--corComplementar2);
            border-radius: 15px;
            border-style: solid;
        }

        #ctFaqTitulo1{
            color: var(--corNeutro1);
            font-size: 2em;
            text-shadow: 0 0 3px black;
        }

        /* Rodapé - #Contato */
        #contato{
            width: 100vw;
            height: 300px;
            background-color: var(--corComplementar2);
            color: var(--corNeutro1);
        }
        
        #ctContatoDiv1{
            height: 100%;
        }

        #ctContatoAddress{
            margin-left: 30px;
            text-align: justify;
        }

        .socialIcon{
            padding: 10px;
            width: 45px;
            filter: invert();
        }

        /* Estilos de uso geral */   
        .linha {
            display: flex;
        }

        .largura1200px{
            width: 1200px;
            margin: 0 auto 0 auto;
        } 

        .largura30 {
            width: 30%;
            height: 100%;
        }

        .largura40 {
            width: 40%;
            height: 100%;
        }

        .largura60 {
            width: 60%;
            height: 100%;
        }

        .largura70 {
            width: 70%;
            height: 100%;
        }
 

        .verticalCentro {
            display: flex;
            flex-direction: column;
            justify-content: center;
            text-align: center;
        }

        .tituloSessao{
            margin-bottom: 30px;
            margin-left: 30px;
            color: var(--corComplementar);
            font-size: 2em;
            text-shadow: 0 0 1px black;
            font-variant: small-caps;
        }


        /* Botões de Chamada de Ação */
        .botao:link,
        .botao:visited {
            border: 1px solid var(--corComplementar);
            border-radius: 15px;
            padding: 8px;
            background-color: var(--corContraste1);
            color: var(--corNeutro1);
            text-decoration: none;
            font-weight: 500;
        }

        .botao:hover,
        .botao:active {
            filter: drop-shadow(0 0 10px var(--corContraste2));
        }


    </style>
</head>

<body>
    
    <!-- Cabeçalho -->
    <header class="cabecalho">
        <nav id="idNav" class="barraNav largura1200px">
            <div class="logo">
                <img src="assets/logo3.png" alt="logo">
            </div>
            <div class="menu">
                <ul class="linha">
                    <li><a class="linkMenu" href="#">Home</a></li>
                    <li><a class="linkMenu" href="#">Curso</a></li>
                    <li><a class="linkMenu" href="#">Depoimentos</a></li>
                    <li><a class="linkMenu" href="#">Contato</a></li>
                </ul>
            </div>
        </nav>
    </header>
    <!-- Principal -->
    <main>
        <!-- home -->
        <section id="home" class="secApresentacao largura1200px">
            <div id="ct1" class="bgFiltro linha">
                <div id="ct2" class="largura60"></div>
                <div id="ct3" class="largura40  verticalCentro">
                    <h1 id="ct3Titulo1">Curso De Programação React</h1>
                    <p id="ct3Texto1">Tudo o que você precisa saber em um só lugar!!!</p>
                    <p><a id="Ct3Botão1" class="botao" href="099-Exemplo google calender.html">Agende uma Aula</a></p>
                </div>
            </div>
        </section>

        <!-- curso -->
        <section id="curso" class="secCurso largura1200px">
            <h2 class="tituloSessao">O que aprenderemos?</h2> 
            <div class="linha">
                <div class="card">
                    <img class="badgeTec" src="assets/html-5.png" alt="">
                    <h3>HTML 5</h3>
                </div>
                <div class="card">
                    <img class="badgeTec" src="assets/css-3.png" alt="">
                    <h3>CSS 3</h3>
                </div>
                <div class="card">
                    <img class="badgeTec" src="assets/JavaScript.png" alt="">
                    <h3>JavaScript</h3>
                </div>
                <div class="card">
                    <img class="badgeTec" src="assets/Bootstrap2.png" alt="">
                    <h3>Bootstrap</h3>
                </div>

            </div>
            <div class="linha">
                <div class="card">
                    <img class="badgeTec" src="assets/PostgreSql.png" alt="">
                    <h3>PostgreSql</h3>
                </div>
                <div class="card">
                    <img class="badgeTec" src="assets/java.png" alt="">
                    <h3>Java</h3>
                </div>
                <div class="card">
                    <img class="badgeTec" src="assets/atom.png" alt="">
                    <h3>React</h3>
                </div>
                <div class="card">
                    <img class="badgeTec" src="assets/typescript.png" alt="">
                    <h3>TypeScript</h3>
                </div>
            </div>


        </section>

        <!-- depoimentos -->
        <section id="depoimentos" class="secDepoimentos largura1200px">
            <h2 class="tituloSessao">O que nossos alunos estão dizendo</h2>
            <div class="linha">
                <div class="card2">
                    <img class="badgeTec" src="assets/aluno1.jpg" alt="">
                    <h3>Regina</h3>
                    <img src="assets/star5.png" alt="">
                </div>
                <div class="card2">
                    <img class="badgeTec" src="assets/aluno2.jpg" alt="">
                    <h3>Augusto</h3>
                    <img src="assets/star5.png" alt="">
                </div>
                <div class="card2">
                    <img class="badgeTec" src="assets/aluno3.jpg" alt="">
                    <h3>Alex</h3>
                    <img src="assets/star5.png" alt="">
                </div>
                <div class="card2">
                    <img class="badgeTec" src="assets/aluno4.jpg" alt="">
                    <h3>Júlia</h3>
                    <img src="assets/star5.png" alt="">
                </div>
            </div>
        </section>

        <!-- Faq -->
        <section id="faq" class="secFaq largura1200px">
            <h2 class="tituloSessao">Perguntas Frequentes</h2>

            <div class="linha">
                <div class="largura60">
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
                </div>
                <div id="ctFaqDiv3" class="largura40 verticalCentro">
                    <h2 id="ctFaqTitulo1">Preparado para dar o próximo passo em direção ao sucesso?</h2>
                    <p id="ctFaqTexto1"><a class="botao" href="099-Exemplo google calender.html">Agende uma Aula agora mesmo!</a></p>
                </div>
            </div>

        </section>

    </main>
    <!-- Rodapé -->
    <footer id="contato" >
        <div id="ctContatoDiv1" class="linha largura1200px">
           <address id="ctContatoAddress" class="largura60 verticalCentro">
                Rua das Palmeiras, 1521 <br>
                Velha, Blumenau, SC <br>
                CEP: 89198-090
           </address>
           <div class="verticalCentro">
                <p>E-mail: contato@meudominio.com.br</p>
                <p>Tel: +55 (47) 2543-3232</p>
                <div class="linha">
                    <a href="#">
                        <img class="socialIcon" src="assets/iconmonstr-whatsapp-5-240.png">
                    </a>
                    <a href="#">
                        <img class="socialIcon" src="assets/iconmonstr-facebook-6-240.png">
                    </a>
                    <a href="#">
                        <img class="socialIcon" src="assets/iconmonstr-linkedin-5-240.png">
                    </a>
                    <a href="#">
                        <img class="socialIcon" src="assets/iconmonstr-github-5-240.png">
                    </a>
                </div>
           </div>
        </div>
    </footer>
</body>

</html>
```
</br>

![logo entra 21](https://cdn.sonicadigital.com.br/entra21/storage/header/257/original-61f8610472d4f.png)