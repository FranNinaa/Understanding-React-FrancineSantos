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

### Exemplo feito em aula

Estrutura de Seleção Simples em JavaScript
A estrutura de seleção simples é geralmente expressa com a instrução if. Ela permite que você execute um bloco de código se uma condição for verdadeira (true).

```javascript
if (condicao) {
    // Código a ser executado se a condição for verdadeira
}
```

Por exemplo:

```javascript
let idade = 20;

if (idade >= 18) {
    console.log("A pessoa é maior de idade.");
}
```

Estrutura de Seleção Composta em JavaScript
A estrutura de seleção composta é frequentemente expressa usando if, else if e else. Permite executar diferentes blocos de código dependendo das condições.

```javascript
if (condicao1) {
    // Código a ser executado se a condição1 for verdadeira
} else if (condicao2) {
    // Código a ser executado se a condição2 for verdadeira
} else {
    // Código a ser executado se nenhuma das condições anteriores for verdadeira
}
```

Por exemplo:

```javascript
let nota = 85;

if (nota >= 90) {
    console.log("A nota é A");
} else if (nota >= 80) {
    console.log("A nota é B");
} else if (nota >= 70) {
    console.log("A nota é C");
} else {
    console.log("A nota é D");
}
```

Neste exemplo, dependendo da nota, uma mensagem diferente será exibida com base nas condições fornecidas.

Essas são as estruturas de seleção simples e compostas em JavaScript, que são cruciais para controlar o fluxo de execução do seu código com base nas condições especificadas.




```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <form action="">
        <label for="idIdade">Idade</label><br>
        <input type="number" name="nmIdade" id="idIdade">
        <br><br>
        <label for="idAltura">Altura</label><br>
        <input type="number" name="nmAltura" id="idAltura" step="0.01">
        <br><br>
        <input type="radio" name="nmGenero" id="idFem" checked>
        <label for="idFem">Feminino</label>
        <input type="radio" name="nmGenero" id="idMasc">
        <label for="idMasc">Maculino</label>
        <input type="radio" name="nmGenero" id="idNaoBinario">
        <label for="idNaoBinario">Nao Binario</label>


        <br><br>
        <output id="idOut">Peso Ideal: </output>
        <br><br>
        <input type="Button" value="Calcular Peso Ideal" onclick="calcularPesoIdeal()">
        <input type="Button" value="Testar Genero" onclick="testarGenero()">
        <input type="Button" value="Testar Alistamento" onclick="testaServicoMilitar()">

        <br><br>
        <input type="number" id="idMenu" name="nmMenu">
        <br>
        <br>
        <input type="button" value="Testar Estruturas Seleção" onclick="exemplosEstruturasSelecao()">

    </form>

    <script>

        function exemplosEstruturasSelecao() {
            //Estrutura de seleção simples
            var idade = 18
            if (idade > 18) {
                console.log("é maior de idade");
            }

            //Estrutura de Seleção composta  && -> AND  || -> OR   ! -> NOT
            var num = 25
            if (num < 10 || (num > 23 && num < 50)) {
                console.log("o numero é menor que 10 ou está no intervalo entre 23 e 50");
            }

            var temperatura = 40 
            var umidade = 22
            if (temperatura >= 38 && umidade < 25) {
                //entra aqui se resultado da expressão = Verdadeiro 
                console.log("Temperatura >= 38 e umidade < 25%");
            } else {
                //entra aqui se resultado da expressão = Falso
                console.log("Caiu aqui por que o resultado da expressão lógica deu falso");
            }

            //Estrutura de seleção encadeada 
            var menu = 3//document.getElementById("idMenu").value
            if (menu == 0) {
                console.log("Opcao 0 selecionada");
            } else {
                if (menu == 1) {
                    console.log("Opcao 1 selecionada");
                } else {
                    if (menu == 2) {
                        console.log("Opcao 2 selecionada");
                    } else {
                        if (menu == 3) {
                            console.log("Opcao 3 selecionada");
                        } else {
                            console.log("Opção Inválida")
                        }
                    }
                }
                
            }

            //Estrutura de seleção encadeada usando IF-ELSE-IF
            if (menu == 0) {
                console.log("Opcao 0 selecionada");
            } else if (menu == 1) {
                console.log("Opcao 1 selecionada");
            } else if (menu == 2) {
                console.log("Opcao 2 selecionada");
            } else if (menu == 3) {
                console.log("Opcao 3 selecionada");
            } else {
                console.log("Opção Inválida")
            }
    
            //switch-case {
            //ESCOLHA (menu)
            switch (menu) {
                //CASO 0: 
                case 0:
                    console.log(" - Opcao 0 selecionada");
                    break;
            
                case 1:
                    console.log(" - Opcao 1 selecionada");
                    break;

                case 2:
                    console.log(" - Opcao 2 selecionada");
                    break;

                case 3:
                    console.log(" - Opcao 3 selecionada");
                    break;

                default:
                    console.log(" - Opção Inválida");
                    break;
            }

            //Ternário 
            var opcao = (menu == 0)? "ternario falso" : "ternario falso"
            console.log(opcao);

    
        }




        function calcularXYZ() {
            console.log("Passou pela Function...");
        }

        function testarGenero() {
            let masculino = document.getElementById("idMasc").checked
            let feminino = document.getElementById("idFem").checked
            let lgbt = document.getElementById("idNaoBinario").checked

            if (masculino == true) {
                console.log("o genero masculino está selecionado");
            }

            if (feminino == true) {
                console.log("o genero feminino está selecionado");
            }

            if (lgbt == true) {
                console.log("o genero nao binário está selecionado");
            }


            if (masculino == true) {
                console.log("o genero masculino está selecionado");
            } else {
                if (feminino == true) {
                    console.log("o genero feminino está selecionado");
                } else {
                    console.log("o genero nao binário está selecionado");
                }
            }


            if (masculino == true) {
                console.log("o genero masculino está selecionado");
            } else if (feminino == true) {
                console.log("o genero feminino está selecionado");
            } else {
                console.log("o genero nao binário está selecionado");
            }

        }

        function calcularPesoIdeal() {
            let masculino = document.getElementById("idMasc").checked
            let feminino = document.getElementById("idFem").checked
            let altura = Number(document.getElementById("idAltura").value)

            let pesoIdeal

            if (masculino == true) {
                pesoIdeal = (72.7 * altura) - 58
            } else {
                pesoIdeal = (62.1 * altura) - 44.7
            }

            document.getElementById("idOut").value = "Peso Ideal: " + pesoIdeal.toFixed(2)
        }


    </script>

</body>

</html>
```
## Estruturas de Seleção em JS

As estruturas de seleção em JavaScript permitem que um programa execute diferentes blocos de código com base em condições específicas. As estruturas mais comuns são o if, else if e else. Abaixo, vou explicar cada uma delas em detalhes:

- if => A estrutura if é usada para executar um bloco de código se uma condição for verdadeira. Se a condição for falsa, o bloco de código dentro do if não será executado. A sintaxe é a seguinte:

```javascript
if (condicao) {
    // Código a ser executado se a condição for verdadeira
}
```
- else => A estrutura else é usada em conjunto com if para executar um bloco de código se a condição for falsa. Se a condição for verdadeira, o bloco de código dentro do else não será executado. A sintaxe é a seguinte:

```javascript
if (condicao) {
    // Código a ser executado se a condição for verdadeira
} else {
    // Código a ser executado se a condição for falsa
}
```

- else if => A estrutura else if permite verificar múltiplas condições em sequência. Se a primeira condição for falsa, ele verifica a próxima condição e assim por diante. O bloco de código dentro do primeiro if ou else if que tiver uma condição verdadeira será executado, e o restante será ignorado. A sintaxe é a seguinte:

```javascript
if (condicao1) {
    // Código a ser executado se a condição1 for verdadeira
} else if (condicao2) {
    // Código a ser executado se a condição2 for verdadeira
} else {
    // Código a ser executado se nenhuma das condições for verdadeira
}
```
#### Aqui está um exemplo que combina todas essas estruturas:

```javascript
var idade = 18;

if (idade < 18) {
    console.log("Menor de idade");
} else if (idade >= 18 && idade < 65) {
    console.log("Adulto");
} else {
    console.log("Idoso");
}
```
- Neste exemplo, o código verifica a idade e imprime uma mensagem dependendo da faixa etária.

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
    <form action="">
        <label for="idIdade">Idade</label><br>
        <input type="number" name="nmIdade" id="idIdade">
        <br><br>
        <label for="idAltura">Altura</label><br>
        <input type="number" name="nmAltura" id="idAltura" step="0.01">
        <br><br>
        <input type="radio" name="nmGenero" id="idFem" checked>
        <label for="idFem">Feminino</label>
        <input type="radio" name="nmGenero" id="idMasc">
        <label for="idMasc">Maculino</label>
        <input type="radio" name="nmGenero" id="idNaoBinario">
        <label for="idNaoBinario">Nao Binario</label>


        <br><br>
        <output id="idOut">Peso Ideal: </output>
        <br><br>
        <input type="Button" value="Calcular Peso Ideal" onclick="calcularPesoIdeal()">
        <input type="Button" value="Testar Genero" onclick="testarGenero()">
        <input type="Button" value="Testar Alistamento" onclick="testaServicoMilitar()">

        <br><br>
        <input type="number" id="idMenu" name="nmMenu">
        <br>
        <br>
        <input type="button" value="Testar Estruturas Seleção" onclick="exemplosEstruturasSelecao()">

    </form>
    <script>
        function exemplosEstruturasSelecao() {
            //Estrutura de seleção simples
            var idade = 18
            if (idade > 18) {
                console.log("é maior de idade");
            }

            //Estrutura de Seleção composta  && -> AND  || -> OR   ! -> NOT
            var num = 25
            if (num < 10 || (num > 23 && num < 50)) {
                console.log("o numero é menor que 10 ou está no intervalo entre 23 e 50");
            }

            var temperatura = 40 
            var umidade = 22
            if (temperatura >= 38 && umidade < 25) {
                //entra aqui se resultado da expressão = Verdadeiro 
                console.log("Temperatura >= 38 e umidade < 25%");
            } else {
                //entra aqui se resultado da expressão = Falso
                console.log("Caiu aqui por que o resultado da expressão lógica deu falso");
            }

            //Estrutura de seleção encadeada 
            var menu = 3//document.getElementById("idMenu").value
            if (menu == 0) {
                console.log("Opcao 0 selecionada");
            } else {
                if (menu == 1) {
                    console.log("Opcao 1 selecionada");
                } else {
                    if (menu == 2) {
                        console.log("Opcao 2 selecionada");
                    } else {
                        if (menu == 3) {
                            console.log("Opcao 3 selecionada");
                        } else {
                            console.log("Opção Inválida")
                        }
                    }
                }
                
            }

            //Estrutura de seleção encadeada usando IF-ELSE-IF
            if (menu == 0) {
                console.log("Opcao 0 selecionada");
            } else if (menu == 1) {
                console.log("Opcao 1 selecionada");
            } else if (menu == 2) {
                console.log("Opcao 2 selecionada");
            } else if (menu == 3) {
                console.log("Opcao 3 selecionada");
            } else {
                console.log("Opção Inválida")
            }
    
            //switch-case {
            //ESCOLHA (menu)
            switch (menu) {
                //CASO 0: 
                case 0:
                    console.log(" - Opcao 0 selecionada");
                    break;
            
                case 1:
                    console.log(" - Opcao 1 selecionada");
                    break;

                case 2:
                    console.log(" - Opcao 2 selecionada");
                    break;

                case 3:
                    console.log(" - Opcao 3 selecionada");
                    break;

                default:
                    console.log(" - Opção Inválida");
                    break;
            }

            //Ternário 
            var opcao = (menu == 0)? "ternario falso" : "ternario falso"
            console.log(opcao);

    
        }

        function calcularXYZ() {
            console.log("Passou pela Function...");
        }

        function testarGenero() {
            let masculino = document.getElementById("idMasc").checked
            let feminino = document.getElementById("idFem").checked
            let lgbt = document.getElementById("idNaoBinario").checked

            if (masculino == true) {
                console.log("o genero masculino está selecionado");
            }

            if (feminino == true) {
                console.log("o genero feminino está selecionado");
            }

            if (lgbt == true) {
                console.log("o genero nao binário está selecionado");
            }


            if (masculino == true) {
                console.log("o genero masculino está selecionado");
            } else {
                if (feminino == true) {
                    console.log("o genero feminino está selecionado");
                } else {
                    console.log("o genero nao binário está selecionado");
                }
            }


            if (masculino == true) {
                console.log("o genero masculino está selecionado");
            } else if (feminino == true) {
                console.log("o genero feminino está selecionado");
            } else {
                console.log("o genero nao binário está selecionado");
            }

        }

        function calcularPesoIdeal() {
            let masculino = document.getElementById("idMasc").checked
            let feminino = document.getElementById("idFem").checked
            let altura = Number(document.getElementById("idAltura").value)

            let pesoIdeal

            if (masculino == true) {
                pesoIdeal = (72.7 * altura) - 58
            } else {
                pesoIdeal = (62.1 * altura) - 44.7
            }

            document.getElementById("idOut").value = "Peso Ideal: " + pesoIdeal.toFixed(2)
        }


    </script>

</body>

</html>
```
## Estruturas de Repetição 

Em JavaScript, as estruturas de repetição são usadas para executar um bloco de código várias vezes, com base em uma condição específica. Existem várias formas de implementar loops em JavaScript, incluindo for, while, do-while e for...of. Vou explicar cada uma delas em detalhes:

- for = A estrutura for é uma maneira comum de executar um bloco de código um número específico de vezes. A sintaxe é a seguinte:

```javascript
for (inicialização; condição; incremento) {
    // Código a ser executado em cada iteração
}
```

### Exemplo:

```javascript
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

- while = A estrutura while é usada para executar um bloco de código enquanto uma condição é verdadeira. A sintaxe é a seguinte:

```javascript
while (condição) {
    // Código a ser executado enquanto a condição for verdadeira
}
```

### Exemplo:

```javascript
let contador = 0;
while (contador < 5) {
    console.log(contador);
    contador++;
}
```

- do-while = A estrutura do-while é semelhante ao while, mas garante que o bloco de código seja executado pelo menos uma vez, mesmo que a condição seja falsa. A sintaxe é a seguinte:

```javascript
do {
    // Código a ser executado
} while (condição);

```

### Exemplo:

```javascript
let contador = 0;
do {
    console.log(contador);
    contador++;
} while (contador < 5);
```

- for...of = A estrutura for...of é usada para iterar sobre elementos de uma coleção (por exemplo, arrays, strings, etc.). A sintaxe é a seguinte:

```javascript
for (variavel of colecao) {
    // Código a ser executado para cada elemento da coleção
}
```

### Exemplo:

```javascript
const nomes = ['Alice', 'Bob', 'Charlie'];
for (const nome of nomes) {
    console.log(nome);
}
```

- switch...case = A estrutura switch...case permite avaliar uma expressão e executar diferentes blocos de código com base no valor da expressão. A sintaxe é a seguinte:

```javascript
switch (expressao) {
    case valor1:
        // Código a ser executado se a expressao for igual a valor1
        break;
    case valor2:
        // Código a ser executado se a expressao for igual a valor2
        break;
    // ...
    default:
        // Código a ser executado se a expressao não corresponder a nenhum valor
}
```

### Exemplo:

```javascript
let diaSemana = 3;
let mensagem;

switch (diaSemana) {
    case 1:
        mensagem = "Domingo";
        break;
    case 2:
        mensagem = "Segunda-feira";
        break;
    case 3:
        mensagem = "Terça-feira";
        break;
    case 4:
        mensagem = "Quarta-feira";
        break;
    case 5:
        mensagem = "Quinta-feira";
        break;
    case 6:
        mensagem = "Sexta-feira";
        break;
    case 7:
        mensagem = "Sábado";
        break;
    default:
        mensagem = "Dia inválido";
}

console.log(mensagem);

```

- Este é um exemplo simples que exibe o nome do dia da semana com base no número fornecido.

Essas estruturas de repetição são fundamentais para criar iterações e automatizar tarefas que requerem processamento repetitivo de dados. A escolha da estrutura de repetição depende do problema específico que você está resolvendo e da lógica necessária para iterar sobre os dados.

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
        var contador = 10 
        //Enquanto  - usado quando não sabemos a qtd de vezes
        console.log("Antes do While");
        while (contador < 10) {
            contador++
            console.log("while " + contador);
        }
        console.log("Depois do While");



        //Faça Enquanto - se precisar executar pelo uma vez
        //contador = 0 
        console.log("Antes do do-While");
        do { //iteração = 1 passada dentro da estrura 
            contador++
            console.log("do-while " + contador);
        } while (contador < 10);
        console.log("Depois do do-While");


        //Para - usado quando sabemos exatamente quantas vezes
        console.log("Antes do For");
        for (let i = 0; i> 10; i++) {
            console.log("For: " + i);
        }

    </script>
    
</body>
</html>
```
## Estrutura de Dados Vetor 

Em JavaScript, o termo "vetor" é frequentemente utilizado para se referir a arrays. Um array é uma estrutura de dados que permite armazenar vários elementos sob um único nome, cada um identificado por um índice ou uma chave. Os arrays em JavaScript são dinâmicos, o que significa que podem crescer ou diminuir de tamanho durante a execução do programa.

Vamos discutir algumas características e operações relacionadas a arrays em JavaScript

### Declaração de um Array:
 Para declarar um array em JavaScript, você pode usar a seguinte sintaxe:

```javascript
const meuArray = [];  // Array vazio
const outroArray = [1, 2, 3, 4, 5];  // Array com elementos
```

### Acesso a Elementos:
Os elementos de um array podem ser acessados usando seus índices, que começam em 0 para o primeiro elemento. Por exemplo:

```javascript
const meuArray = ['a', 'b', 'c'];
console.log(meuArray[0]);  // Saída: 'a'
console.log(meuArray[2]);  // Saída: 'c'
```

### Tamanho do Array:
 Você pode obter o tamanho de um array (número de elementos) usando a propriedade length:

```javascript
const meuArray = [10, 20, 30];
console.log(meuArray.length);  // Saída: 3
```

### Adicionar e Remover Elementos:

Para adicionar elementos ao final de um array, você pode usar o método push:
```javascript
meuArray.push(40);  // Adiciona 40 ao final do array
```


- Para remover o último elemento de um array, você pode usar o método pop:

```javascript
meuArray.pop();  // Remove o último elemento do array
```

### Iteração sobre um Array:
Você pode usar estruturas de repetição, como for, for...of ou forEach, para iterar sobre os elementos de um array e realizar operações em cada elemento.

### Arrays Multidimensionais:
Em JavaScript, você pode criar arrays multidimensionais (arrays de arrays), permitindo a representação de estruturas de dados mais complexas, como matrizes. Por exemplo:

```javascript
const matriz = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
console.log(matriz[1][0]);  // Acessando o elemento 4
```

Essas são apenas algumas operações e conceitos básicos relacionados a arrays em JavaScript. Os arrays são uma parte essencial da programação e são usados para armazenar e manipular coleções de dados de maneira eficaz e flexível.

### Exemplo feito em Aula

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
        //Array vazio 
        var carro = []

        //Array pré inicializado (vetor, coleção, pilha, fila, lista)
        const fruta = ['laranja', 'morango', 'abacate']
        console.log(fruta);

        //Declarando um array usando o construtor da classe Array 
        let legumes = new Array('brócolis', 'cenoura', 'alface')


        //Acessando posições especificas do array
        var frutaCitrica = fruta[2]
        console.log("fruta Citrica: " + frutaCitrica);

        fruta[3] = "limao"
        fruta[4] = "fisalis"
        fruta[6] = "melancia"
        console.log(fruta);
        console.log(fruta[0]);
        console.log(fruta[1]);
        console.log(fruta[2]);
        console.log(fruta[3]);
        console.log(fruta[4]);

        //Tamanho do Array 
        console.log("Tamanho do Array: " + fruta.length);


        //Inserindo um novo elemento no final do array
        fruta[fruta.length] = "melão"
        fruta.push("Amora")


        //Inserindo um novo elemento no inicio do array
        fruta.unshift("Banana")
        
        //Tirar Elementos do começo do array 
        var fruta3 = fruta.shift()
        console.log("fruta 3 --> " + fruta3);


        //Tirar Elementos do Final do array 
        var fruta4 = fruta.pop()
        console.log("fruta 4 --> " + fruta4);

        console.log("---------------------------");
        console.log(fruta);

        //Construindo Fila vs Pilha  (pop, shift, unshift, push)
        //Fila - o primeiro elemento que entra é primeiro a sair 
        //Pilha - O último elemento a entrar é primeiro a sair 

        //Iterando um Array 
        for (let index = 0; index < fruta.length; index++) {
            let element = fruta[index];
            console.log(fruta[index]);
            console.log("Fruta[" + index + "] -> " + element);
        }

        //Exibindo o array inteiro no console 
        console.log(fruta);
        console.log(fruta.toString());
        console.table(fruta);



        //Passando a referencia de fruta para fruta2
        var fruta2 = fruta

        fruta[2] = "Limão"
        console.log(fruta);
        console.log(fruta2);

        var texto = "123"
        //Passando o valor de texto para texto2 
        var texto2 = texto


    </script>
</body>

</html>

```
## Funções em JavaScript
Em JavaScript, uma função é um bloco de código reutilizável que realiza uma tarefa específica. As funções são essenciais para organizar e modularizar o código.

### Sintaxe Básica
Aqui está a sintaxe básica para declarar uma função em JavaScript:

```javascript
function nomeDaFuncao(parametro1, parametro2) {
  // Corpo da função
  // Código para executar a tarefa
  // Pode retornar um valor usando a palavra-chave "return"
}
```

- nomeDaFuncao: Nome dado à função.
- parametro1, parametro2: Parâmetros que a função pode receber (opcionais).
#### Exemplo de Função Simples
Aqui está um exemplo de uma função simples que retorna a soma de dois números:
```javascript
function soma(a, b) {
  return a + b;
}

const resultado = soma(5, 3); // Chama a função e atribui o resultado a uma variável
console.log(resultado); // Saída: 8
```

#### Chamando uma Função
Para chamar (ou executar) uma função, você usa o nome da função seguido pelos parâmetros entre parênteses.

- Funções Anônimas e Expressões de Função
Além da sintaxe padrão, você pode definir funções de forma anônima e atribuí-las a variáveis (expressões de função). Aqui está um exemplo:

```javascript
const multiplicacao = function(a, b) {
  return a * b;
};

const resultadoMultiplicacao = multiplicacao(4, 2);
console.log(resultadoMultiplicacao); // Saída: 8
```

- Arrow Functions
Arrow functions são uma forma mais concisa de escrever funções em JavaScript. Aqui está um exemplo:
```javascript
const subtracao = (a, b) => a - b;

const resultadoSubtracao = subtracao(10, 5);
console.log(resultadoSubtracao); // Saída: 5
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
        //linha 1
        //linha 2
        //var genero = document.getElementById()

        var pesoIdealF = calcularPesoIdeal("f", 1.60)
        console.log(pesoIdealF);

        pesoIdealM = calcularPesoIdeal("m", 1.60)
        console.log(pesoIdealM);

        /*
                Funções são "Tarefas"/"Ações" executadas assim que são chamadas ou em 
                decorrencia de algum evento.
                Uma função pode receber parâmetros e retornar um resultado. Veja um exemplo 
                completo abaixo. 

                Paradigma: "Programação Estruturada"

        */

        //Escopo da Função... 
        var x1 = 2 //Assinatura da váriavel  nome=referencia, endereço, tipo, conteúdo
        var x2 = 3
        function teste(x1) {
            let x2 = 6
            return x1 + x2
        }

        console.log(teste(5));
        /*
        Toda função pode ter: 
        * Uma chamada (chamada para executar a função)
        * Parametros (opcional) - No Exemplo acima, genero e altura são os parâmetros
        * Ação (O processamento no interior da função) - No exemplo, o cálculo do peso ideal... 
        * Retorno (opcional) - (O valor resultante do Processamento) - No exemplo, o pesoIdeal está sendo retornado
        */

        //Função Nomeada
        function calcularPesoIdeal(genero, altura) {

            let pesoIdeal = 0
            if (genero == "f") {
                pesoIdeal = (62.1 * altura) - 44.7
            } else {
                pesoIdeal = (72.7 * altura) - 58
            }

            return pesoIdeal
        }




        /*
           Funções Anônimas ou Funções de expressão (Functions expression)
           ----------------
            Como o próprio nome diz, são funções sem nome. 
            O JavaScript é uma linguagem Funcional. Uma das caracteristicas do paradigma funcional 
            é poder atribuir funções a variáveis.   
        */



        var pesoIdeal2 = function (genero, altura) {

            let pesoIdeal = 0
            if (genero == "f") {
                pesoIdeal = (62.1 * altura) - 44.7
            } else {
                pesoIdeal = (72.7 * altura) - 58
            }

            return pesoIdeal
        }

        console.log("peso Ideal 2 : " + pesoIdeal2("f", 1.57));

        //------------------------------------------------------------------------------------------------------------
        /* 
           Funções Seta (Arrow Function) 
           ----------------
        */
        var pesoIdeal3 = (genero, altura) => { //arrow 

            let pesoIdeal = 0
            if (genero == "f") {
                pesoIdeal = (62.1 * altura) - 44.7
            } else {
                pesoIdeal = (72.7 * altura) - 58
            }

            return pesoIdeal
        }

        /*
            Arrow Function - Forma abreviada
            -------------------------------
            Se houver apenas um parâmetro, pode-se suprimir os parênteses
            Se houver apenas uma linha de instrução, pode-se suprimir as 
            chaves e o return será implícito
        */
        var dobro = num => num * 2
        console.log(dobro(5));


        /* Exemplo exagerado de más práticas...
        var num1 = 3
        var resultado = ((num1 % 2) == 0) ? num1 => num1 * 2 : (num1 < 0) ? num1 => num1 * -1 : num1 => num1 * 3
        console.log("aqui " + resultado(-3));
        */


        /*
        var vetor = [1,2,3]
        vetor.forEach(element => {
            
        });
        */
        //------------------------------------------------------------------------------------------------------------
        /* 
           Funções Auto-Executável/Auto-Invocável
           ----------------
        */

        (function(){
            console.log("Executou...");
        })()

        //teste()


    </script>
</body>

</html>
```

#### As arrow functions têm uma sintaxe mais compacta e, em muitos casos, substituem as expressões de função.

## Tratamento de Eventos em JavaScript
O tratamento de eventos é um aspecto fundamental no desenvolvimento web, permitindo que páginas da web interajam com os usuários. Em JavaScript, os eventos são ações que ocorrem no navegador, como clicar em um botão, enviar um formulário ou mover o mouse.

### Adicionando Event Listeners
Para tratar eventos em JavaScript, usamos Event Listeners (ou "ouvintes de eventos"). Eles são usados para "ouvir" um evento específico em um elemento HTML e executar uma ação quando esse evento ocorre.

-Aqui está a sintaxe básica para adicionar um Event Listener a um elemento:

```javascript
const meuElemento = document.getElementById('meuId');

meuElemento.addEventListener('nomeDoEvento', (event) => {
  // Código a ser executado quando o evento ocorrer
});
```

**meuId**: É o ID do elemento HTML ao qual você deseja adicionar o Event Listener.
**nomeDoEvento**: É o nome do evento que você deseja ouvir, como "click", "mouseover", "submit", etc.

#### Exemplo de Event Listener
Aqui está um exemplo de como adicionar um Event Listener para o evento de clique em um botão:

```javascript
const meuBotao = document.getElementById('meuBotao');

meuBotao.addEventListener('click', () => {
  alert('Botão clicado!');
});
```

- Neste exemplo, quando o botão com o ID "meuBotao" é clicado, exibirá um alerta com a mensagem "Botão clicado!".

#### Event Object (Objeto de Evento)
Dentro da função do Event Listener, você pode acessar um objeto de evento que contém informações sobre o evento, como o elemento alvo, coordenadas do mouse, teclas pressionadas, etc. Geralmente, esse objeto é chamado de event.

```javascript
meuElemento.addEventListener('nomeDoEvento', (event) => {
  console.log('Evento ocorreu no elemento:', event.target);
});
```

- No exemplo acima, estamos imprimindo o elemento alvo do evento no console.

#### Removendo Event Listeners
- Para remover um Event Listener, você usa o método removeEventListener.

```javascript
meuElemento.removeEventListener('nomeDoEvento', minhaFuncaoDeTratamentoDeEvento);
```

### Exemplos feito em aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="" method="get">
        <input type="email"  name="nmEmail" id="idEmail">
        <input type="button" id="idBotao" value="CLique Me" onclick="testarClique()">

        <input type="button" id="idBotao2" value="CLique Me 2">
        <input type="button" id="idBotao3" value="CLique Me 3">
        <input type="submit" id="idBotao4">

      
    </form>

    <script>

        //função chamada em Event Handler Inline (má Prática)
        function testarClique() {
            console.log("Clicou em clique me!!!");
        }

        //Event Handler Nível 1 
        var botao = document.getElementById("idBotao2")

        console.log(botao);

        botao.onclick = tratamentoBotao2

        function tratamentoBotao2() {
            console.log("Clicou Botão 2");  
        }

        //usando função anonima... 
        botao.ondblclick = function() {
            console.log("Clique duplo em Botao 2");
        }

        botao.onmouseover = function(){
            console.log("Passou o mause por cima do botão 2");
        }

        //Event Handler Nível 2
        var botao3 = document.getElementById("idBotao3")

        botao3.addEventListener("click", tratamentoBota3) //função de callback 

        function tratamentoBota3() {
            console.log("Clicou Botão 3");  
        }

        botao3.addEventListener("mouseover", function(){
            console.log("Clique duplo no botao 3");
        })

        const botao4 = document.getElementById("idBotao4")

        botao4.addEventListener("click", function(event){
            event.preventDefault() //previne o comportamento padrao do formulario 
            console.log(event);

            let email = document.getElementById("idEmail").value
            console.log("Email: " + email);
        })


    </script>
    
</body>
</html>
```

## Conclusão
O tratamento de eventos em JavaScript é crucial para criar interatividade em páginas da web. Event Listeners permitem que você responda a ações do usuário e execute ações apropriadas em resposta a essas ações.

## Strings em JavaScript
Em JavaScript, uma string é uma sequência de caracteres, como texto ou palavras. As strings são usadas para representar e manipular dados de texto em um programa.

### Criando Strings
Existem várias maneiras de criar strings em JavaScript:

#### Aspas Simples ou Duplas:

```javascript
const stringComAspasSimples = 'Esta é uma string com aspas simples.';
const stringComAspasDuplas = "Esta é uma string com aspas duplas.";
```

#### Template Strings:
As template strings permitem interpolação de variáveis e expressões usando ${}.

```javascript
const nome = 'João';
const saudacao = `Olá, meu nome é ${nome}.`;
```

#### Acessando Caracteres em uma String
Você pode acessar caracteres em uma string usando colchetes **[]** e um índice (começando em 0 para o primeiro caractere).

```javascript
const minhaString = 'Exemplo';
console.log(minhaString[0]);  // Saída: 'E'
```

#### Tamanho de uma String
Para obter o comprimento (número de caracteres) de uma string, você pode usar a propriedade **length**.

```javascript
const minhaString = 'Exemplo';
console.log(minhaString.length);  // Saída: 7
```

#### Métodos de String
JavaScript oferece diversos métodos para manipulação de strings. Aqui estão alguns exemplos:

- **toUpperCase()** e **toLowerCase()**:
Transformam os caracteres em maiúsculas ou minúsculas, respectivamente.

```javascript
const frase = 'Exemplo de String';
console.log(frase.toUpperCase());  // Saída: 'EXEMPLO DE STRING'
console.log(frase.toLowerCase());  // Saída: 'exemplo de string'
```

- **concat()**:
Concatena duas ou mais strings.

```javascript
const str1 = 'Olá, ';
const str2 = 'mundo!';
const mensagem = str1.concat(str2);
console.log(mensagem);  // Saída: 'Olá, mundo!'
```

**indexOf()** e **lastIndexOf()**:
Retornam a posição do primeiro ou último caractere correspondente em uma string.

```javascript
const texto = 'Aprendendo JavaScript';
console.log(texto.indexOf('JavaScript'));  // Saída: 11
```
### Exemplos feito em aula

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
    <input type="text" id="idTexto" placeholder="Digite sua Expressão">
    <input type="button" id="idbtTeste" value="executar Eval" onclick="testarEval()">

    <script>

        const string1 = "A string primitive"; //String literals 
        const string2 = 'Also a string primitive';
        const string3 = `Yet another string primitive`;

        const string4 = String(1); 
        const string5 = String(true);
        const string6 = String("Teste");

        const string7 = new String("A String object"); //String Object 

        console.log(typeof string1); // "string"
        console.log(typeof string2); // "string"
        console.log(typeof string3); // "string"
        console.log(typeof string4); // "string"
        console.log(typeof string5); // "string"
        console.log(typeof string6); // "string"
        console.log(typeof string7); // "object"

        console.log(string6.valueOf()); // "Teste"
        console.log(string7.valueOf()); // "A String object"

        //String vs. Array 
        var gato = "cat"
        console.log(gato[2]);
        console.log("cat"[1]);
        console.log("catwerr".length);
        console.log("cat".charAt(2));

        //Comparando Strings
        const a = "a";
        const b = "b";
 
        // A  B  c d
        // 65 66 
        if (a < b) {
            // true
            console.log(`${a} is less than ${b}`);
        } else if (a > b) {
            console.log(`${a} is greater than ${b}`);
        } else {
            console.log(`${a} and ${b} are equal.`);
        }


        const upperA = "A"
        console.log(a == upperA); //false
        console.log(a.toLowerCase() == upperA.toLowerCase()); //true
        console.log(a.toUpperCase() == upperA.toUpperCase()); //true
        console.log(areEqualCaseInsensitive(a, upperA));

        if (areEqualCaseInsensitive(a, upperA)) {
            console.log("a é igual A");
        } else {
            console.log("a é diferente A");
        }

        function areEqualCaseInsensitive(str1, str2) {
            return str1.toLowerCase() === str2.toLowerCase()
        }


        const numUm = 1
        const charUm = "1" 
        if (numUm == charUm){
            console.log("numUm é igual charUm");
        }else{
            console.log("numUm é diferente de charUm");
        }

        if (numUm === charUm){
            console.log("numUm é igual charUm");
        }else{
            console.log("numUm é diferente de charUm");
        }

        //Strig Template / Template literal
        const total = 12.4
        const totalComDesconto = 10.00
        //console.log("o total da conta é: " + total + ", com desconto fica: " + totalComDesconto)
        console.log(`o total da conta é: ${total} , com desconto fica: ${totalComDesconto}`);

        var nome = "Joao"
        //Métodos estáticos de String 
        console.log(String.fromCharCode(67, 65)); //Retorna o caractere correspondente ao valor ascii informado

        //
        const texto = "linha 1\nlinha 2"
        const filePath = String.raw`C:\Development\profile\aboutme.html`

        console.log(`The file was uploaded from: ${filePath}`);

        const filePath2 = "C:\\Development\\profile\\aboutme.html"

        console.log(filePath2);

        //Métodos de instância
        const texto1 = "texto"
        const text2 = " 123"
        console.log(texto1.charAt(2));
        console.log(texto1.charCodeAt(2));
        console.log(texto1.concat(text2, " ad", " 12"));

        const str1 = 'Cats are the best!';
        console.log(str1.endsWith('best!'));

        console.log(str1.endsWith('best', 17));

        const str2 = 'Is this a question?';

        console.log(str2.endsWith('question'));


        const sentence = 'The quick brown fox jumps over the lazy dog.';
        const word = 'fox';

        console.log(sentence.includes(word)); 

        console.log(`The word "${word}" ${sentence.includes(word) ? 'is' : 'is not'} in the sentence`);
    
        let text = "Apple, Banana, Kiwi";
        let part = text.slice(7, 13);
        console.log(part);

        console.log(text.substring(7, 13));
        console.log(text.substr(7, 6));
        
        let text3 = "Please visit Microsoft!";
        let newText = text3.replace("Microsoft", "W3Schools");

        console.log(newText);

        let text4 = "Please visit Microsoft!";
        let newText2 = text4.replace(/MICROSOFT/i, "W3Schools");

        console.log(newText2);

        let text5 = "Please visit Microsoft and Microsoft!";
        let newText5 = text5.replace(/Microsoft/g, "W3Schools");

        console.log(newText5);

        let text6 = "5";
        let padded = text6.padStart(4,"1");

        console.log(padded);

        let text7 = "Please, visit, Microsoft, and, Microsoft!";
        let array7 = text7.split(",")

        console.log(array7);

        //Eval ...
        let resultado = eval("2 + 2 * 3")
        console.log(resultado);


        function testarEval(){
            let texto = document.getElementById("idTexto").value
            let resultado = eval(texto)
            console.log(`Resul: ${resultado}`);
        }


    </script>
</body>
</html>
```
## Estes são apenas alguns exemplos de operações com strings em JavaScript. Strings são uma parte fundamental da linguagem e são amplamente utilizadas para manipulação de texto em programas.