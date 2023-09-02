# Anotações da aula de HTML

## Formatação básica do HTML sem divisões

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Parâmetros -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- Texto -->
    <h1>Título h1</h1>
    <p>Parágrafo</p>
</body>
</html>
```
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Spotyflix</title>
</head>
<body>
    <header>
        <nav>
            <ul>
                <!-- Conteúdo do header -->
            </ul>
        </nav>
    </header>
    <main>
        <section>
            <!-- Conteúdo da primeira seção -->
        </section>
        <section>
            <h2>FAQ</h2>
            <!-- Conteúdo da segunda seção -->
        </section>
    </main>
    <footer>
        <!-- Conteúdo do footer -->
    </footer>
</body>
</html>
```

## Listas HTML
- ul -> unordered list
- ol -> ordered list
- Exemplo de lista não ordenada (unordered list, ul):

```html
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
</ul>
```
- Exemplo de lista ordenada (ordered list, ol):

```html
<ol>
    <li>Item 1</li>
    <li>Item 2</li>
</ol>
```

## Mudanças no Texto (negrito, itálico, etc.)

```html
<p><b>Negrito</b></p>
<p><strong>Ênfase</strong></p>
<p><i>Itálico</i></p>
<p><em>Enfatizado</em></p>
<p><mark>Grifado</mark></p>
<p><small>Texto menor</small></p>
<p><big>Texto maior</big></p>
<p><del>Taxado</del></p>
<p>The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.</p>
```

## Formulários HTML
- Exemplo de um formulário HTML:

```html
<form action="">
    <label for="idTexto">Texto</label><br>
    <input type="text" id="idTexto" name="nmTexto" class="inputTexto">
    <br>
    <!-- Outros campos do formulário -->
    <!-- Checkbox, Radio Button, Select, Textarea, etc. -->
    <br>
    <input type="button" value="Capturar" onclick="capturaTela()">
</form>
```
## Anotações HTML
- html: Páginas de internet, layout de documentos e outros layouts específicos.
- Parte head: Não é visível, são passados parâmetros nesse lugar.
- Parte body: É a parte que se vê.
- Metadados: Dados que descrevem dados.
Exemplo de uso de id:

```html
<footer id="idfooter">
    <p>Siga-nos no Instagram: @Spotyflix</p>
    <p>www.spotyflix.com</p>
</footer>
```
## Toggle:

```html
<details>
    <summary>Pergunta/Título do Toggle</summary>
    <p>Dentro do Toggle</p>
</details>
```
## Estruturação dentro do corpo do HTML:

```html
<body>
    <header>
        <!-- Conteúdo do cabeçalho -->
    </header>
    <aside>
        <!-- Conteúdo da barra lateral esquerda -->
    </aside>
    <main>
        <section>
            <!-- Conteúdo da sessão principal -->
        </section>
    </main>
    <footer>
        <!-- Conteúdo do rodapé -->
    </footer>
</body>
```
## Tabela HTML
- Estrutura de uma tabela:

```html
<table border="1" cellpadding="10" width="100%" align="center">
    <thead>
        <tr>
            <th>Qtd</th>
            <th>Descrição</th>
            <th>Valor</th>
        </tr>
    </thead>
    <tbody>
        <!-- Conteúdo da tabela -->
    </tbody>
    <tfoot>
        <tr>
            <td colspan="2"><b>Total</b></td>
            <td>19,00</td>
        </tr>
    </tfoot>
</table>
```
## Inserindo Links no HTML:

```html
<a href="URL">Texto do Link</a>
```
## Atributos importantes:

- alt: Texto alternativo para imagens.
- target: Define como o link será aberto (por exemplo, "_blank" para abrir em uma nova aba).
- title: Texto que aparece ao passar o mouse sobre o link.
- download: Permite baixar um arquivo ao clicar no link.
## Áudio e Vídeo HTML
- Exemplo de áudio e vídeo:

```html
<audio controls autoplay loop muted>
    <source src="caminho/do/arquivo.mp3" type="audio/mpeg">
    Seu Navegador não é compatível com a tag Audio
</audio>

<video width="320" controls autoplay loop muted>
    <source src="caminho/do/video.mp4" type="video/mp4">
    Seu Navegador não é compatível com a tag Vídeo
</video>
```
## Emmet Abbreviations
#### Conjunto de abreviações de código que ajudam a ganhar produtividade. Alguns exemplos:

- html:5: Gera a estrutura básica do HTML5.
- a:link: Gera um link.
- h1{Titulo}: Cria um cabeçalho < h1 > com o texto "Titulo".
- ul>li*3: Gera uma lista não ordenada com 3 itens.
- div#content: Gera uma <div> com o ID "content".
- div.classname: Gera uma <div> com a classe "classname".
- ul>li.item-$*3: Gera 3 itens de lista com classes diferentes.
#### Para mais abreviações, consulte a documentação do Emmet.
