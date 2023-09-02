# Anotações das Aula de CSS

## Anotações Gerais CSS
**Funções:** Estilizar elementos HTML, controle de layout, animações e transições, pseudoclasses e pseudoelementos, estilos de formulários, transformações e efeitos 2D/3D, controle de impressão.

## CSS Básico

- O CSS básico é colocado dentro da tag `<style>` dentro do elemento `<head>` do HTML.

 Exemplos de como aplicar estilos a elementos HTML:


```html
<h1 id="idTituloPrincipal" name="" class="clTituloPrincial">Titulo Teste</h1>

<h2 class="clTituloPrincial sublinhado">Titulo 2</h2>

<div class="clDiv1"></div>
```
## CSS Externo
- Você pode vincular um arquivo CSS externo usando a seguinte linha em seu HTML:
```html
<link rel="stylesheet" href="style.css">
```
## Cascateamento CSS
#### A ordem de aplicação de estilos no CSS é a seguinte:

- CSS padrão do navegador.
CSS em folhas de estilo internas e externas (interno quando se usa elementos como *, #, etc., e externo quando é um arquivo separado .css).
- CSS inline (dentro dos próprios elementos HTML).
Sites para Cores
Color Wheel
Color Palettes
Seletores CSS
- O CSS utiliza seletores para encontrar elementos a serem estilizados. Existem cinco tipos de seletores: simples, combinadores, pseudoclasse, pseudoelementos e atributos.

### Seletores Simples
- Selecionam elementos com base em IDs, nomes, classes, etc.

```css

/* Seletor Universal - Seleciona toda a página */
* {
    margin: 0;
    padding: 0;
    border: 0;
}

/* Seletor de Classe */
.clTituloPrincial {
    color: blue;
}

.clDiv1 {
    background-color: beige;
}

.sublinhado {
    text-decoration: underline;
}

/* Seletor de ID */
#idTituloPrincipal {
    color: red;
    background-color: aqua;
}

/* Seletor de Tag */
h3 {
    color: blueviolet;
}

.linha {
    border: 1px solid black;
    display: flex;
}

.coluna1 {
    border: 1px solid black;
    width: 30%;
}
```
## Seletores Combinadores
- Selecionam elementos com base em uma relação específica entre eles.

### Comandos CSS para Estilização
#### Aqui estão alguns comandos CSS para estilização:

- padding: Define o espaçamento interno de um elemento em pixels (px).
- margin: Define a margem de um elemento em pixels (px).
- background-color: Define a cor de fundo de um elemento.
- border: Define a borda de um elemento.
- width e height: Define a largura e a altura de um elemento.
- display: Define como um elemento é exibido.
#### Comandos para Listas
- list-style-type: Define o estilo do marcador de lista (pontinho).
- list-style-image: Define uma imagem como marcador de lista.
- list-style-position: Define a posição do marcador de lista.

## Comandos CSS para Texto
- color: Define a cor do texto.
- font-family: Define a família da fonte a ser usada.
- font-size: Define o tamanho da fonte.
- font-weight: Define a espessura da fonte (por exemplo, negrito).
- text-align: Define o alinhamento do texto (por exemplo, left, right, center, justify).
- text-decoration: Define a decoração do texto (por exemplo, underline, overline, line-through).
- line-height: Define a altura da linha de texto.
- letter-spacing: Define o espaçamento entre caracteres.
- word-spacing: Define o espaçamento entre palavras.
- text-transform: Transforma o texto (por exemplo, uppercase, lowercase, capitalize).
## Comandos CSS para Bordas
- border-radius: Define o raio das bordas de um elemento.
- border-color: Define a cor das bordas de um elemento.
- border-width: Define a largura das bordas de um elemento.
- border-style: Define o estilo das bordas (por exemplo, solid, dotted, dashed).
## Comandos CSS para Posicionamento
- position: Define o método de posicionamento de um elemento (por exemplo, relative, absolute, fixed, static).
- top, right, bottom, left: Define a posição de um elemento quando o posicionamento é absolute ou fixed.
- z-index: Define a ordem de empilhamento de elementos posicionados.
## Comandos CSS para Fundo
- background-image: Define uma imagem de fundo.
- background-repeat: Define como a imagem de fundo se repete (por exemplo, repeat, no-repeat).
- background-size: Define o tamanho da imagem de fundo.
- background-position: Define a posição da imagem de fundo.
## Comandos CSS para Espaçamento
- padding-top, padding-right, padding-bottom, padding-left: Define o espaçamento interno de um elemento em direções específicas.
- margin-top, margin-right, margin-bottom, margin-left: Define a margem de um elemento em direções específicas.
## Comandos CSS para Exibição
- visibility: Define a visibilidade de um elemento (visible, hidden).
- display: Define como um elemento é exibido (block, inline, inline-block, none, entre outros).
- overflow: Define o comportamento do conteúdo que transborda o elemento (hidden, auto, scroll).
## Comandos CSS para Opacidade
- opacity: Define a opacidade de um elemento (um valor entre 0 e 1).
## Comandos CSS para Sombra
- box-shadow: Define uma sombra para um elemento.
## Comandos CSS para Transformações
transform: Aplica transformações 2D ou 3D a um elemento (por exemplo, translate, rotate, scale).
