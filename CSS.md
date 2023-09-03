# Anotações das Aula de CSS

## Exemplos de como adiciona o CSS no código HTML

#### Para adicionar estilos CSS a um arquivo HTML, você tem três opções principais:

#### Folha de Estilos Externa:

- Esta é a abordagem mais comum e recomendada. Você cria um arquivo CSS separado e, em seguida, vincula esse arquivo ao seu HTML usando o elemento < link > na seção < head > do seu documento HTML.

```html
<link rel="stylesheet" href="assets/estilos.css">
```
- O arquivo CSS externo (style.css) pode conter todas as regras de estilo que você deseja aplicar ao seu HTML.

#### Folha de Estilos Interna:

- Você também pode incluir regras de estilo diretamente em seu documento HTML, dentro da seção < style > na seção < head >. Isso é chamado de "folha de estilos interna".

No exemplo, as regras de estilo internas estão dentro do elemento < style >:

```html
<style>
    /* Suas regras de estilo aqui */
</style>
```
#### Estilos Inline:

- Você pode aplicar estilos diretamente a um elemento HTML usando o atributo style. Isso é chamado de "estilo inline".

- No exemplo, o estilo inline é aplicado ao elemento < h1 > desta maneira:

```html
<h1 style="color: beige;">Testes</h1>
```
- O estilo inline é útil quando você deseja aplicar um estilo específico a um único elemento HTML.

### A ordem de prioridade dos estilos é geralmente a seguinte (do mais específico ao menos específico):

- Estilos Inline (mais específicos)
- Folha de Estilos Interna
- Folha de Estilos Externa (menos específicos)
  
### Certifique-se de organizar seus estilos de acordo com a hierarquia e a especificidade necessárias para seu projeto. O uso de folhas de estilos externas é recomendado para manter seu código mais organizado e facilitar a manutenção.

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

## Background 

#### A propriedade background no CSS é usada para definir o plano de fundo (background) de um elemento HTML, como uma < div >, < section >, ou qualquer outro elemento que você deseje estilizar. Ela permite que você controle a cor de fundo, a imagem de fundo, a repetição da imagem, a posição, o tamanho e outros aspectos relacionados ao plano de fundo de um elemento. Aqui estão os principais usos e propriedades associadas à propriedade background:

- Definir a cor de fundo: Você pode usar background-color para definir uma cor sólida de fundo para o elemento. Por exemplo:
```css
background-color: lightblue;
```
- Adicionar uma imagem de fundo: A propriedade background-image permite que você insira uma imagem de fundo. Isso é frequentemente usado para criar layouts atraentes. Por exemplo:
```css
background-image: url('imagens/fundo.png'); /*URL*/
```
- Controlar a repetição da imagem de fundo: Com background-repeat, você pode definir se a imagem de fundo deve se repetir, não se repetir (no-repeat), ou repetir apenas na horizontal ou vertical. Por exemplo:
```css
background-repeat: repeat-x;/*Repete na horizontal, vertical ou ambas.*/
```
- Posicionar a imagem de fundo: A propriedade background-position permite que você defina a posição inicial da imagem de fundo. Por exemplo:

```css
background-position: center top ;/*Posição do fundo em relação ao topo e esquerda da tela.*/
```
- Fixar o plano de fundo: Com background-attachment, você pode controlar se o plano de fundo rola com o conteúdo da página ou permanece fixo enquanto a página é rolada. Por exemplo:
```css
background-attachment: fixed;/*Fica fixa no scroll.*/
```
- Definir o tamanho da imagem de fundo: Use background-size para controlar o tamanho da imagem de fundo em relação ao elemento. Por exemplo:
```css
background-size: cover;/*Tamanho de imagem para o background ser ajustado automaticamente.*/
```
- Definir o tamanho da imagem de fundo: Use background-size para controlar o tamanho da imagem de fundo em relação ao elemento. Por exemplo:
```css
background-clip: border-box;/*Define se o conteúdo será recortado com base nos limites das bordas (border)
```

- Controlar a opacidade do plano de fundo: A opacidade do plano de fundo pode ser ajustada usando a propriedade opacity. No entanto, lembre-se de que isso afetará não apenas o plano de fundo, mas todo o elemento e seu conteúdo. A propriedade background também permite agrupar várias configurações relacionadas ao plano de fundo em uma única declaração, tornando o código CSS mais conciso e legível. Por exemplo:
```css
background: url('imagem.jpg') center top no-repeat fixed;
```
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
## Textos

#### O CSS (Cascading Style Sheets) oferece várias propriedades que permitem estilizar e formatar texto em uma página da web. Essas propriedades permitem controlar a cor do texto, o tamanho da fonte, o espaçamento entre linhas e palavras, o estilo da fonte, entre outras características. Aqui estão algumas das propriedades CSS mais comuns para estilizar textos:

- color: Define a cor do texto. Você pode usar nomes de cores, códigos de cores em hexadecimal, RGB, RGBA ou HSL para especificar a cor do texto. Exemplo:

```css
color: blue;
```

- font-family: Especifica a família de fontes a ser usada para o texto. Você pode fornecer uma lista de fontes em ordem de preferência, separadas por vírgulas, para que o navegador escolha a primeira fonte disponível. Exemplo:
```css
font-family: 'Times New Roman', Times, serif; /* fonte padrão */
```

- font-size: Define o tamanho da fonte. Você pode usar unidades como pixels, ems ou porcentagens para definir o tamanho. Exemplo:

```css
font-size: 16px;
```

- font-weight: Controla a espessura da fonte, como "normal", "bold", "lighter" ou valores numéricos como 100, 200, etc. Exemplo:

```css
font-weight: bold;
```

- font-style: Define o estilo da fonte, como "normal", "italic" ou "oblique" Exemplo:
```css
font-style: italic;
```

- text-align: Especifica o alinhamento horizontal do texto dentro de seu contêiner, com opções como "left", "right", "center" ou "justify". Exemplo:

```css
text-align: center;
```

- line-height: Controla a altura da linha, que é a distância vertical entre as linhas de texto. Você pode definir um valor específico ou usar unidades como "em" ou porcentagens. Exemplo:

```css
line-height: 1.5;
```

- text-decoration: Define decorações de texto, como "underline" (sublinhado), "overline" (sobrescrito) e "line-through" (riscado). Você também pode especificar a cor e o estilo da linha. Exemplo:

```css
text-decoration: underline dotted red;
```

- text-transform: Controla a transformação do texto, como "uppercase" (maiúsculas), "lowercase" (minúsculas) ou "capitalize" (a primeira letra de cada palavra em maiúscula). Exemplo:

```css
text-transform: uppercase;
```

- letter-spacing: Define o espaçamento entre as letras do texto. Isso pode ser usado para ajustar o rastreamento do texto. Exemplo:

```css
letter-spacing: 2px;
```

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

## Propriedade color no CSS

#### No CSS (Cascading Style Sheets), a propriedade color é usada para definir a cor do texto de um elemento HTML. Essa propriedade é fundamental para controlar a aparência dos textos em uma página da web. Aqui está uma explicação detalhada sobre a propriedade color no CSS:

#### A propriedade color permite especificar a cor do texto dentro de um elemento HTML. Você pode usar várias formas de definir cores, incluindo:

- Nomes de Cores: Você pode usar nomes de cores predefinidos, como "red" (vermelho), "blue" (azul), "green" (verde) e muitos outros. Aqui estão alguns exemplos:

```css
color: red;
color: blue;
color: green;
```

- Códigos de Cores em Hexadecimal: Os códigos de cores em hexadecimal são representados por uma combinação de seis caracteres, que podem incluir números (0-9) e letras (A-F). Por exemplo:

```css
color: #FF0000; /* Vermelho */
color: #0000FF; /* Azul */
```

- Valores RGB (Red, Green, Blue): Você pode especificar uma cor usando valores RGB, onde você define a intensidade de vermelho (R), verde (G) e azul (B). Cada valor varia de 0 a 255. Por exemplo:

```css
color: rgb(255, 0, 0);   /* Vermelho */
color: rgb(0, 0, 255);   /* Azul */
```

- Valores RGBA (Red, Green, Blue, Alpha): Os valores RGBA são semelhantes aos valores RGB, mas incluem um quarto valor para a transparência (alfa) da cor, variando de 0 a 1. Isso permite que você crie cores semitransparentes. Por exemplo:
```css
color: rgba(255, 0, 0, 0.5); /* Vermelho com 50% de transparência */
```

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
##### Substitua "NOME_DA_FONTE" pelo nome da fonte que você selecionou.

#### Adicionar Estilos de Fonte ao seu CSS:

- Agora que você incorporou a fonte no seu HTML, você pode usá-la em seu CSS, definindo a fonte para os elementos desejados. Por exemplo:
```css
body {
  font-family: 'NOME_DA_FONTE', sans-serif;
}
```
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

