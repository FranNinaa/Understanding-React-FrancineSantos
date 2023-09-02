## Anotações das aula de CSS


#### Anotações gerais CSS
**Funções:**  Estilizar elementos HTML, controle de layout, animações e transições, pseudoclasses e pseudoelementos, estilos de formulários, transformações e efeitos 2D/3D, controle de impressão


#### CSS básico
é colocado <style> dentro do head 

Aonde é colocado os nomes das classes: 
```
{
    <h1 id="idTituloPrincipal" name="" class="clTituloPrincial" >Titulo Teste</h1>

    <h2 class="clTituloPrincial sublinhado">Titulo 2</h2>

    <div class="clDiv1">
}
```
CSS estilo externo : <link rel="stylesheet" href="style.css">

Aonde se coloca o CSS: Cascateamento: 
- CSS Padrão Navegador
- CSS Folhas de estilo interno e externo (interno é quando a gente abre o style com o *,#,etc e externo é um arquivo separado .css)
- CSS Inline

Sites cores:   [Color Wheel](https://color.adobe.com/pt/create/color-wheel)   
[ColorPalletes](https://coolors.co/) 



O CSS tem seletores que são colocados no style para encontrar os elementos para estilizar. Existem 5 tipos de seletores: simples, combinadores, de pseudoclasse, de pseudoelementos e de atributos.
- [Seletores simples](#seletores-simples)  
- [Seletores combinadores](#seletores-combinadores)


##### Seletores simples
Selecionam os elementos com base no id, nome, classe, etc. 
```
{
    <style>
        /* Seletor Universal*/  <!--seleciona toda a pagina-->
        *{
            margin: 0;
            padding: 0;
            border: 0;
            
        }

        /* Seletor de classe */
        .clTituloPrincial{
            color: blue;
        }

        .clDiv1{
            background-color: beige;
        }

        .clSpan1{
            background-color: brown;
        }
        .sublinhado{
            text-decoration: underline;
        }

        /* Seletor de ID */
        #idTituloPrincipal{
            color : red; 
            background-color: aqua;
        }

        /* Seletor de Tag */
        h3{
            color: blueviolet;
        }

        .linha {
            border: 1px solid black;
            display: flex; <!--transforma linha em coluna-->
        }

        .coluna1{
            border: 1px solid black;
            width: 30%;
        }

    </style>
}
```
##### Seletores combinadores
Seleciona os elementos com base em uma relação específica entre eles


#### Comandos que estilizam a página no CSS
Comandos gerais: 
- padding -> px -> 
- margin -> px -> margem 
- background-color -> cor do background do item selecionado
- border ->
  - 
- width e height -> 
- display -> 

Comandos de lista: 
- list-style-type -> muda o pontinho da frente da lista  
- list-style-image -> coloca uma imagem no lugar dos pontinhos da frente  
- list-style-position -> muda o local do pontinho ou imagem