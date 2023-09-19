# Introdução ao JavaScript
JavaScript é uma poderosa linguagem de programação amplamente utilizada no desenvolvimento web para tornar as páginas da web interativas e dinâmicas. Ela permite a manipulação e modificação dos elementos de uma página, interação com o usuário, envio de requisições assíncronas ao servidor e muito mais.

### O que é JavaScript?
O JavaScript é uma linguagem de programação de alto nível, orientada a objetos e interpretada. Ela foi originalmente desenvolvida para adicionar interatividade a páginas da web, possibilitando a manipulação do DOM (Document Object Model) e a resposta a eventos do usuário.

## História
JavaScript foi originalmente desenvolvido pela Netscape em 1995 e inicialmente chamado de "LiveScript". Mais tarde, foi renomeado para "JavaScript" para capitalizar a popularidade da linguagem Java. No entanto, é importante notar que JavaScript e Java são linguagens diferentes, com sintaxe e propósitos distintos.

## Características Principais
- Linguagem Baseada em Scripts: JavaScript é uma linguagem de script que é interpretada diretamente no navegador do usuário, proporcionando funcionalidades dinâmicas e interatividade nas páginas web.

- Multiplataforma: Pode ser executado em uma variedade de plataformas, incluindo navegadores web modernos, servidores e dispositivos móveis.

- Tipagem Dinâmica: As variáveis em JavaScript não têm um tipo de dados fixo e podem mudar de tipo durante a execução do programa.

- Orientado a Objetos: É uma linguagem orientada a objetos, onde quase tudo é considerado um objeto, facilitando a organização e reutilização do código.

- Ampla Comunidade e Ecossistema: JavaScript possui uma vasta comunidade de desenvolvedores e uma grande quantidade de bibliotecas e frameworks que facilitam o desenvolvimento de aplicativos complexos.

## Utilização Comum
 - Desenvolvimento Web: JavaScript é essencial para criar páginas web interativas, validação de formulários, animações, efeitos visuais e muito mais.

- Aplicativos Web Avançados: É usado para desenvolver aplicativos web robustos e dinâmicos, muitas vezes por meio de frameworks populares como Angular, React e Vue.js.

- Desenvolvimento de Servidor: Com a introdução do Node.js, JavaScript pode ser usado para desenvolver aplicativos do lado do servidor, permitindo a construção de servidores escaláveis e eficientes.


### Exemplo Básico:
Aqui está um exemplo simples de código JavaScript que exibe uma mensagem em um alerta:

```javascript
alert("Olá, Mundo!");
```
Este alerta será exibido quando a página for carregada ou quando o código for executado.

### Como Incluir JavaScript em uma Página HTML:
Você pode incluir JavaScript em um arquivo HTML de várias maneiras, sendo as mais comuns através das tags < script >:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de JavaScript</title>
</head>
<body>

<script>
    // Seu código JavaScript aqui
    alert("Olá, Mundo!");
</script>
</body>
</html>
```
O JavaScript é uma ferramenta poderosa e essencial para qualquer desenvolvedor web que deseja criar aplicativos interativos e dinâmicos.

### Exemplo feitos em aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de JavaScript</title>
</head>
<body>

<script>
    // Seu código JavaScript aqui
    alert("Olá, Mundo!");
</script>
</body>
</html>
```
# DOM (Document Object Model) em JavaScript
O Document Object Model (DOM) é uma representação hierárquica e estruturada de um documento HTML/XML que o navegador interpreta para renderizar páginas web. O DOM é uma interface que permite ao JavaScript acessar e manipular o conteúdo e a estrutura de uma página web enquanto ela está sendo exibida.

## Estrutura Hierárquica do DOM
O DOM organiza elementos HTML em uma árvore hierárquica, onde cada elemento é um nó. A raiz dessa árvore é o nó document, que representa todo o documento HTML. A partir daí, outros nós representam os elementos HTML, seus atributos, texto e outros componentes.

### Por exemplo, considere o seguinte HTML:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Exemplo de DOM</title>
</head>
<body>
  <div id="conteudo">
    <p>Olá, mundo!</p>
  </div>
</body>
</html>
```

### O DOM para este HTML seria representado de forma hierárquica assim:

```less
document
└── html
    ├── head
    │   └── title
    │       └── #text ("Exemplo de DOM")
    └── body
        └── div#conteudo
            └── p
                └── #text ("Olá, mundo!")
```

### Acesso e Manipulação do DOM com JavaScript
O JavaScript permite que os desenvolvedores acessem e manipulem o DOM para criar páginas web interativas e dinâmicas. Isso é feito usando métodos e propriedades fornecidos pelo navegador.

### Acesso a Elementos do DOM
Para acessar elementos do DOM em JavaScript, você pode usar métodos como document.getElementById(), document.querySelector(), ou navegando pelos nós da árvore DOM.

Exemplo usando getElementById:

```javascript
const elemento = document.getElementById('conteudo');
console.log(elemento.textContent); // Exibe o texto dentro do elemento
```

### Manipulação de Elementos do DOM
Você pode alterar o conteúdo, os estilos, os atributos e até mesmo adicionar/remover elementos do DOM usando JavaScript.

### Exemplo de alteração de texto:

```javascript
const elemento = document.getElementById('conteudo');
elemento.textContent = 'Novo texto aqui'; // Altera o texto do elemento
```

### Eventos e Interação com o DOM
O JavaScript permite associar funções a eventos (como clique do mouse, pressionamento de tecla, etc.) em elementos HTML. Isso permite interatividade com o usuário.

### Exemplo de associação de evento de clique:

```javascript
const botao = document.getElementById('meuBotao');
botao.addEventListener('click', () => {
  alert('Botão clicado!');
});
```
O DOM é uma parte fundamental do desenvolvimento web e é essencial para a criação de aplicativos web interativos.

### Exemplo feitos em aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

    <input type="text" id="idNome">

    <output id="idOut"></output>

    <p id="idParagrafo"></p>

    <script>
        //pegando elementos
        document.getElementById("idOut").value = "Teste"

        document.getElementById("idOut").innerText = "Teste 1234..."

        document.getElementById("idParagrafo").innerText = "Atribuindo texto ao paragrafo"
    </script>
</body>
</html>
```
# Tipos de Dados em JavaScript
JavaScript é uma linguagem de programação que possui diversos tipos de dados, que podem ser classificados em dois grupos principais: tipos de dados primitivos e tipos de dados de referência.

### Tipos de Dados Primitivos
Os tipos de dados primitivos são os mais básicos e fundamentais na linguagem. Eles são imutáveis e são armazenados diretamente no local de alocação de memória. Em JavaScript, os tipos de dados primitivos incluem:

### Number: Representa números, inteiros ou em ponto flutuante.

- Exemplo:

```javascript
let numero = 42;
let pi = 3.14;
```

### String: Representa uma sequência de caracteres.

- Exemplo:

```javascript
let texto = "Olá, mundo!";
```

### Boolean: Representa um valor lógico, true (verdadeiro) ou false (falso).

- Exemplo:

```javascript
let isAtivo = true;
```

### Undefined: Representa uma variável que foi declarada, mas não foi inicializada com um valor.

- Exemplo:

```javascript
let x;
console.log(x); // Output: undefined
```

### Null: Representa a ausência intencional de qualquer valor ou objeto de valor.

- Exemplo:

```javascript
let y = null;
```

### Symbol: Introduzido no ECMAScript 6, representa um valor único e imutável usado como chave de propriedade.

- Exemplo:

```javascript
const meuSimbolo = Symbol('descrição opcional');
```

### BigInt: Introduzido no ECMAScript 11, representa inteiros maiores do que 2^53 - 1.

- Exemplo:

```javascript
const bigIntValue = 1234567890123456789012345678901234567890n;
```

### Exemplo feito em aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    

    <script>
        /*
            5 tipos de dados 
            -------------------
            - string     -  'isso é uma string'  "isso é uma String" "123"
            - number     -   123  12.5 
            - boolean    -   true  false 
            - Object 
            - function 

            2 - tipos especiais de dados 
            ------------------------------
            - null 
            - undefined 

            6 - Tipos de Objetos 
            -------------------------
            - Object 
            - Date 
            - Array 
            - Number 
            - String 
            - Boolean 

            Operadores para testar tipos de dados 
            -------------------------------------
            typeOf
            isNaN (Not a Number)

        */

        var nomeUsuario = true
        console.log(typeof(nomeUsuario));
        console.log(isNaN(nomeUsuario));

        
        /*
          2 - Formas de fazer conversão de tipos de dados 
          ------------------------------------------------
          - Conversão automática (conversão implícita)

        */

        console.log(5 + "2"); //Conversão para string
        console.log(5 + null); //Conversão para number
        console.log("5" + undefined); //Conversão para string
        console.log("5" + null); //Conversão para string
        console.log("5" - 2); //Conversão para number
        console.log("5" * "2"); //Conversão para number

        /*
          - Conversão usando funções do JS (Conversão Explícita)
          ------------------------------------------------------
          Conversão para String
        */
        var variavel
        var x = 345

        variavel = String(x)
        console.log("tipo: " + typeof(variavel) + " " + variavel);
        variavel = String(123)
        console.log("tipo: " + typeof(variavel) + " " + variavel);

        var salBase = 1000.00;
        console.log("salBase 1 " + typeof(salBase));
                 
        salBase = salBase.toString(); 
        console.log("salBase 2 " + typeof(salBase));

        //Outros métodos que retornam strings 
        var h = 75.345675467;
        console.log("h.tofixed(2) " + h.toFixed(2));
        console.log("h.toExponencial(3) " + h.toExponential(3));
        console.log("h.toPrecision(5) " + h.toPrecision(5));

        /*
         - Conversão para Number
         -----------------------
         - String to Number
        */

        //1. Forma 

        var y = "5"
        var j = + y 

        console.log("j " + typeof(j));

        //2. forma 
        console.log("'3.14' to Number " + Number("3.14"))
        console.log("true to Number " + Number(true))
        console.log("false to Number " + Number(false))
        console.log("'89 90' to Number " + Number("89 90")) //retorna NaN
        console.log("espaço to Number " + Number(" "))
        console.log("vazio to number " + Number(""))

        //3. forma 
        console.log("parseFloat('10.5') " + parseFloat("10.5"));
        console.log("parseFloat('10') " + parseFloat("10"));

        console.log("parseInt('10.5') " + parseInt("10.5"));
        console.log("parseInt('10') " + parseInt("10"));

    </script>
</body>
</html>
```

# Conversão de Tipos em JavaScript
A conversão de tipos, também conhecida como coerção de tipos, é a capacidade de JavaScript de converter automaticamente um tipo de dado em outro quando necessário. Isso ocorre em operações que envolvem diferentes tipos de dados.

Existem dois tipos principais de conversão de tipos em JavaScript: Conversão Implícita e Conversão Explícita.

### Conversão Implícita (Coerção)
A conversão implícita ocorre quando o JavaScript automaticamente converte um tipo de dado para outro sem a intervenção do desenvolvedor.

- Exemplo de conversão implícita:

```javascript
let numero = 10;
let texto = "O número é: " + numero; // Número é convertido para string
console.log(texto); // Output: "O número é: 10"
```
### Conversão Explícita
A conversão explícita é quando o desenvolvedor especifica a conversão de um tipo de dado para outro de forma deliberada.

### Usando Funções de Conversão
JavaScript fornece funções para realizar conversões explícitas entre diferentes tipos de dados:

- parseInt(): Converte uma string em um número inteiro.

- Exemplo:

```javascript
let numero = parseInt("10");
console.log(numero); // Output: 10


```
- parseFloat():  Converte uma string em um número de ponto flutuante.

- Exemplo:

```javascript
let numero = parseFloat("10.5");
console.log(numero); // Output: 10.5

```

- String():  Converte um valor em uma string.
- Exemplo:

```javascript
let numero = 10;
let texto = String(numero);
console.log(texto); // Output: "10"
```

- Number(): Converte um valor em um número.

- Exemplo:

```javascript
let numero = Number("10");
console.log(numero); // Output: 10
```

### Operadores de Conversão
Além disso, existem operadores que podem ser usados para converter tipos de dados:

### Operador '+': Pode ser usado para converter um valor para string.

- Exemplo:

```javascript
let numero = 10;
let texto = numero + ""; // Converte númeropara string
console.log(texto); // Output: "10"
```
 
### Boas Práticas
É importante entender a coerção de tipos para evitar comportamentos inesperados em seu código. Em alguns casos, pode ser útil usar a conversão explícita para garantir que os tipos de dados estejam corretos.

# Operadores em JavaScript
Os operadores em JavaScript são símbolos ou palavras-chave que são usados para realizar operações em variáveis e valores. Eles são fundamentais para a lógica e funcionalidade de qualquer programa JavaScript. Os operadores são classificados em vários tipos, incluindo operadores aritméticos, operadores de atribuição, operadores de comparação, operadores lógicos, operadores bit a bit, entre outros.

### Operadores Aritméticos
Os operadores aritméticos são usados para realizar operações matemáticas básicas, como adição, subtração, multiplicação, divisão e outros.

- Adição (+): Soma dois valores.

- Subtração (-): Subtrai um valor de outro.

- Multiplicação (*): Multiplica dois valores.

- Divisão (/): Divide um valor pelo outro.

- Resto (%): Retorna o resto da divisão entre dois valores.

- Incremento (++): Incrementa o valor de uma variável.

- Decremento (--): Decrementa o valor de uma variável.

- Exemplo:

```javascript
let a = 10;
let b = 5;

let soma = a + b;       // soma = 15
let subtracao = a - b;  // subtracao = 5
let multiplicacao = a * b;  // multiplicacao = 50
let divisao = a / b;    // divisao = 2
let resto = a % b;      // resto = 0

a++; // incrementa 'a' em 1
b--; // decrementa 'b' em 1
```

### Operadores de Atribuição
Os operadores de atribuição são usados para atribuir valores a variáveis.

- Atribuição simples (=): Atribui um valor a uma variável.

- Atribuição com adição (+=): Adiciona o valor à variável e atribui.

- Atribuição com subtração (-=): Subtrai o valor da variável e atribui.

- Atribuição com multiplicação (*=): Multiplica o valor à variável e atribui.

- Atribuição com divisão (/=): Divide o valor da variável e atribui.

- Exemplo:

```javascript
let a = 10;
let b = 5;

let soma = a + b;       // soma = 15
let subtracao = a - b;  // subtracao = 5
let multiplicacao = a * b;  // multiplicacao = 50
let divisao = a / b;    // divisao = 2
let resto = a % b;      // resto = 0

a++; // incrementa 'a' em 1
b--; // decrementa 'b' em 1
```

### Operadores de Comparação
Os operadores de comparação são usados para comparar dois valores e retornar um valor booleano (verdadeiro ou falso) com base na comparação.

- Igual (==): Verifica se dois valores são iguais.

- Estritamente igual (===): Verifica se dois valores são iguais e do mesmo tipo.

- Diferente (!=): Verifica se dois valores são diferentes.

- Estritamente diferente (!==): Verifica se dois valores são diferentes e/ou de tipos diferentes.

- Maior que (>): Verifica se um valor é maior que outro.

- Menor que (<): Verifica se um valor é menor que outro.

- Maior ou igual a (>=): Verifica se um valor é maior ou igual a outro.

- enor ou igual a (<=): Verifica se um valor é menor ou igual a outro.

- Exemplo:

```javascript
let a = 10;
let b = 5;

console.log(a == b);  // false
console.log(a > b);   // true
console.log(a !== b); // true
```

### Operadores Lógicos
Os operadores lógicos são usados para operações de lógica booleana e retornam um valor booleano.

- E lógico (&&): Retorna verdadeiro se ambas as expressões são verdadeiras.

- OU lógico (||): Retorna verdadeiro se pelo menos uma das expressões é verdadeira.

- Negação lógica (!): Inverte o valor booleano.

- Exemplo:

```javascript
let x = true;
let y = false;

console.log(x && y); // false
console.log(x || y); // true
console.log(!x);     // false
```

### Operadores Bit a Bit
Os operadores bit a bit atuam em nível de bits e são usados para operações bitwise.

- AND bit a bit (&): Retorna 1 se ambos os bits são 1.

- OR bit a bit (|): Retorna 1 se pelo menos um dos bits é 1.

- XOR bit a bit (^): Retorna 1 se os bits são diferentes.

- NOT bit a bit (~): Inverte cada bit.

- Shift à esquerda (<<): Move os bits para a esquerda.

- Shift à direita (>>): Move os bits para a direita.

- Exemplo:
```javascript
let a = 5;  // Representado em binário como 0101
let b = 3;  // Representado em binário como 0011

console.log(a & b);  // 1 (binário: 0001)
console.log(a | b);  // 7 (binário: 0111)
console.log(a ^ b);  // 6 (binário: 0110)
console.log(~a);     // -6 (binário: 11111111111111111111111111111010)
```

### Operador Ternário
O operador ternário é uma forma compacta de expressar uma condição if-else.

- Sintaxe:

```javascript
condicao ? valor_se_verdadeiro : valor_se_falso;
```

- Exemplo:

```javascript
let idade = 20;
let status = (idade >= 18) ? 'Adulto' : 'Menor';
console.log(status); // "Adulto"
```

Estes são alguns dos principais operadores em JavaScript. Eles são essenciais para a lógica e o funcionamento dos programas escritos em JavaScript.
