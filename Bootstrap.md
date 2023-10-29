# Bootstrap: Um Framework de Desenvolvimento Front-End

O **Bootstrap** é um dos frameworks de desenvolvimento front-end mais populares e amplamente utilizados na web. Desenvolvido inicialmente pela equipe do Twitter, o Bootstrap é uma ferramenta que permite aos desenvolvedores criar sites e aplicativos web de forma rápida e eficiente. Neste documento, exploraremos a funcionalidade do Bootstrap, forneceremos exemplos de código e explicaremos como funciona.

## Funcionalidade do Bootstrap

O Bootstrap é um conjunto de recursos de HTML, CSS e JavaScript pré-projetados que simplificam a criação de interfaces de usuário atraentes e responsivas. Suas principais funcionalidades incluem:

**1. Grade Responsiva:** O Bootstrap fornece uma grade flexível que se adapta a diferentes tamanhos de tela. Isso facilita a criação de layouts que funcionam bem em dispositivos de desktop, tablet e celular.

**2. Componentes Prontos para Uso:** O Bootstrap oferece uma ampla gama de componentes prontos para uso, como botões, formulários, navegação, alertas e muito mais. Isso economiza tempo e esforço no desenvolvimento.

**3.Personalização:** Embora o Bootstrap forneça estilos e componentes prontos, ele também permite personalização. Os desenvolvedores podem ajustar as configurações para corresponder à identidade visual de seu projeto.

**4.JavaScript Interativo:** O Bootstrap inclui bibliotecas JavaScript para adicionar interatividade a elementos da página, como modais, carrosséis e abas.

**5. Suporte a Navegadores:** O Bootstrap é compatível com a maioria dos navegadores modernos, garantindo que os sites e aplicativos sejam acessíveis a um amplo público.

### Exemplos de Código<br>
**1. Grade Responsiva**

```html
<div class="container">
    <div class="row">
        <div class="col-md-4">Coluna 1</div>
        <div class="col-md-4">Coluna 2</div>
        <div class="col-md-4">Coluna 3</div>
    </div>
</div>
```
### Neste exemplo, criamos uma grade responsiva com três colunas que se ajustam automaticamente ao tamanho da tela.

**2. Botão**
```html
<button class="btn btn-primary">Botão Primário</button>
<button class="btn btn-secondary">Botão Secundário</button>
```

### Estes são exemplos de botões com estilos pré-definidos. O Bootstrap oferece classes para diferentes estilos de botão, como primário, secundário e perigo.

**3. Navegação**

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
    <a class="navbar-brand" href="#">Meu Site</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Alternar navegação">
        <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
            <li class="nav-item active">
                <a class="nav-link" href="#">Página Inicial</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="#">Sobre</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="#">Contato</a>
            </li>
        </ul>
    </div>
</nav>

```

#### Este é um exemplo de um menu de navegação responsivo criado com o Bootstrap.

## Como Funciona
O Bootstrap funciona incluindo seu código CSS e JavaScript em seu projeto. Você pode baixar os arquivos diretamente do site oficial do Bootstrap ou usar um CDN (Content Delivery Network) para acessá-los. Após a inclusão desses recursos, você pode começar a usar as classes e componentes do Bootstrap em seu código HTML.

Além disso, o Bootstrap é altamente personalizável. Você pode modificar as variáveis de estilo e, se necessário, até mesmo criar sua própria versão personalizada do Bootstrap para atender às necessidades específicas do seu projeto.

Em resumo, o Bootstrap é uma ferramenta poderosa para o desenvolvimento front-end que permite a criação de sites e aplicativos web com rapidez e eficiência, graças aos seus recursos prontos para uso e à flexibilidade de personalização. Ele é amplamente adotado na comunidade de desenvolvimento web e continua a evoluir para acompanhar as tendências da web moderna.

## Exemplo feito em aula

```html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>

    <input type="button" value="testar" onclick="testar()">
    <script>

        function testar() {
            //Operador lógico "E": basta uma das condições ser FALSA para que 
            //a expressão inteira seja falsa. 

            //Faz avaliação de curto circuito,ou seja, a segunda expressão 
            //não é executada se a primeira expressão retornar false
            if (retornaFalse() && retornaTrue()) {
                console.log("Entrou no IF (&&) - bloco True");
            } else {
                console.log("Entrou no IF (&&) - bloco False");
            }


            //Faz avaliação de circuito completo, independente do resultado 
            //da segunda expressão, a segunda também será executada! 
            if (retornaFalse() & retornaTrue()) {
                console.log("Entrou no IF (&) - bloco True");
            } else {
                console.log("Entrou no IF (&) - bloco False");
            }

            //Operador lógico "OU": basta uma das condições ser VERDADEIRA para que 
            //a expressão inteira seja VERDADEIRA. 
            
            //Faz avaliação de curto circuito,ou seja, a segunda expressão 
            //não é executada se a primeira expressão retornar true
            if (retornaTrue() || retornaFalse()) {
                console.log("Entrou no IF (||) - bloco True");
            } else {
                console.log("Entrou no IF (||) - bloco False");
            }

            //Faz avaliação de circuito completo, independente do resultado 
            //da segunda expressão, a segunda também será executada! 
            if (retornaTrue() | retornaFalse()) {
                console.log("Entrou no IF (|) - bloco True");
            } else {
                console.log("Entrou no IF (|) - bloco False");
            }


            console.log("------------------------------------------------");
            var num = 9 & 3 
            console.log(num);

            var num = 9 | 3 
            console.log(num);

            var numBinario = 0b11
            console.log(numBinario);

            var numOctal = 0o11 
            console.log(numOctal);
            
            var numHexadecimal = 0xff;
            console.log(numHexadecimal);

            var numExponencial = 2e3;
            console.log(numExponencial);
/*
                       1001 9
                       0011 3
                       1011 

*/
        }


        function retornaFalse() {
            console.log("passou False");
            return false
        }
        function retornaTrue() {
            console.log("Passou True");
            return true
        }

    </script>
</body>

</html>
```

![imagem exemplo bootstrap](https://blog.mastertech.com.br/wp-content/uploads/2017/10/bootstrap.png)