# Introdução à Lógica de Programação

A lógica de programação é o alicerce essencial para qualquer pessoa que deseje se aventurar no mundo da programação. Ela serve como a base fundamental para a criação de algoritmos e solução de problemas de maneira eficaz e estruturada.

## O Que é Lógica de Programação?

A lógica de programação é a arte de pensar de forma lógica e estruturada para resolver problemas de maneira algorítmica. Ela envolve a habilidade de decompor problemas complexos em partes menores e mais gerenciáveis, identificar padrões, tomar decisões lógicas e criar algoritmos claros e eficientes para alcançar um objetivo específico.

## Por que a Lógica de Programação é Importante?

A lógica de programação é importante por várias razões:

- **Resolução de Problemas:** Ela ensina a abordar problemas complexos de maneira organizada e lógica, tornando a solução mais acessível.

- **Eficiência:** Algoritmos bem projetados economizam tempo e recursos, resultando em software mais eficiente.

- **Compreensão de Código:** Entender a lógica por trás do código facilita a leitura e a manutenção de programas.

- **Versatilidade:** As habilidades de lógica de programação são transferíveis para várias linguagens de programação.

## Conceitos Fundamentais

Alguns conceitos fundamentais na lógica de programação incluem:

- **Variáveis:** Armazenam dados que podem ser manipulados pelo programa.
- **Estruturas de Controle:** Incluem decisões condicionais (if, else) e loops (for, while) para controlar o fluxo do programa.
- **Funções e Procedimentos:** Permitem organizar o código em unidades reutilizáveis.
- **Estruturas de Dados:** Permitem armazenar e organizar informações de maneira eficiente.

Aprender lógica de programação é um passo crucial para se tornar um programador eficiente. À medida que você ganha experiência, esses conceitos se tornarão a base para a criação de aplicativos complexos e poderosos.

Nesta série de tutoriais, exploraremos esses conceitos em detalhes, fornecendo exemplos práticos e exercícios para ajudá-lo a aprimorar suas habilidades de lógica de programação.

[Lógica de Programação passado na aula - clique que levará para o PDF](/biblioteca/001%20-%20Lógica%20de%20Programação.pdf)


## Proposições

As proposições na lógica de programação, também conhecidas como proposições lógicas ou simplesmente proposições, são afirmações ou sentenças que podem ser classificadas como verdadeiras ou falsas. Elas são a base da lógica formal e são amplamente usadas na programação para tomar decisões, controlar o fluxo de execução de um programa e avaliar condições.

#### Aqui estão alguns conceitos importantes relacionados às proposições na lógica de programação:

- Proposições Simples: São proposições que não podem ser divididas em partes menores com significado independente. Exemplos de proposições simples incluem "A temperatura é maior que 30 graus Celsius" ou "O usuário está logado no sistema".

- Operadores Lógicos: São usados para combinar ou manipular proposições. Os operadores lógicos mais comuns são:

- E (AND): Retorna verdadeiro apenas se ambas as proposições forem verdadeiras.
- OU (OR): Retorna verdadeiro se pelo menos uma das proposições for verdadeira.
- NÃO (NOT): Inverte o valor de uma proposição, tornando verdadeiro em falso e vice-versa.

- Proposições Compostas: São construídas combinando proposições simples com operadores lógicos. Por exemplo, "A temperatura é maior que 30 graus Celsius E o sol está brilhando" é uma proposição composta que usa o operador "E" para combinar duas proposições simples.

- Valores Verdadeiros e Falsos: Na lógica de programação, costumamos usar os valores "verdadeiro" (true) e "falso" (false) para representar o resultado da avaliação de proposições. "Verdadeiro" indica que a proposição é verdadeira, enquanto "falso" indica que a proposição é falsa.

- Avaliação de Condições: As proposições são frequentemente usadas para avaliar condições em programas. Por exemplo, em uma estrutura de seleção (como o if em linguagens de programação), uma proposição é avaliada, e com base em seu resultado, um bloco de código específico é executado.

[Lógica de Programação  - clique que levará para o PDF](/biblioteca/002%20-%20Proposições%20e%20Estruturas%20de%20seleção.pdf)

#### Exemplo de proposições e expressões lógicas em pseudocódigo:

```
Proposição A: A temperatura é maior que 30 graus Celsius.
Proposição B: O sol está brilhando.

Proposição Composta: A E B (A temperatura é maior que 30 graus Celsius E o sol está brilhando).
Proposição Composta: A OU B (A temperatura é maior que 30 graus Celsius OU o sol está brilhando).
Proposição Composta: NÃO A (A temperatura não é maior que 30 graus Celsius).

```
Na programação, a avaliação de proposições e expressões lógicas desempenha um papel crucial na tomada de decisões e no controle de fluxo, permitindo que os programas ajam de maneira condicional com base em condições específicas.

## Tabela Verdade

Uma tabela verdade é uma representação tabular de todas as possíveis combinações de valores lógicos para um conjunto de proposições ou variáveis lógicas. Ela é usada na lógica proposicional e na teoria dos circuitos lógicos para avaliar o resultado de expressões lógicas sob diferentes condições.

Em uma tabela verdade, cada linha representa uma combinação única de valores lógicos para as variáveis envolvidas, e as colunas mostram o resultado da expressão lógica para essas combinações.

Exemplo de Tabela Verdade para a Operação "E" (AND)
A operação "E" (AND) é verdadeira apenas quando ambas as proposições são verdadeiras.

```
| A | B | A AND B |
|---|---|--------|
| F | F |    F   |
| F | V |    F   |
| V | F |    F   |
| V | V |    V   |
```

Neste exemplo, A e B são variáveis lógicas. A coluna "A AND B" mostra o resultado da operação "E" (AND) entre A e B para cada combinação de valores. A operação "E" é verdadeira (V) somente quando ambas A e B são verdadeiras (V).

Exemplo de Tabela Verdade para a Operação "OU" (OR)
A operação "OU" (OR) é verdadeira quando pelo menos uma das proposições é verdadeira.

```
| A | B | A OR B |
|---|---|--------|
| F | F |    F   |
| F | V |    V   |
| V | F |    V   |
| V | V |    V   |

```
Neste exemplo, A e B são variáveis lógicas, e a coluna "A OR B" mostra o resultado da operação "OU" (OR) entre A e B para cada combinação de valores. A operação "OU" é verdadeira (V) se pelo menos uma das proposições for verdadeira (V).

Exemplo de Tabela Verdade para a Operação "NÃO" (NOT)
A operação "NÃO" (NOT) inverte o valor de uma proposição.

```
| A | NOT A |
|---|-------|
| F |   V   |    
| V |   F   |   
```

Neste exemplo, A é uma variável lógica, e a coluna "NOT A" mostra o resultado da operação "NÃO" (NOT) para cada valor de A. A operação "NÃO" inverte o valor lógico, tornando 0 em 1 e 1 em 0.

Você pode usar tabelas verdade para avaliar expressões lógicas complexas, projetar circuitos lógicos e tomar decisões com base em condições lógicas. Elas são uma ferramenta fundamental na lógica e na programação.

## Estrutura de Seleção

A lógica de programação é fundamental para a construção de programas de computador eficientes e corretos. Uma das estruturas mais importantes da lógica de programação é a estrutura de seleção, que permite que um programa tome decisões com base em condições específicas. As estruturas de seleção permitem que o programa execute diferentes blocos de código com base nas condições que estão sendo avaliadas.

Existem duas formas principais de estruturas de seleção:

Estrutura de Seleção Simples (ou Condicional):
A estrutura de seleção simples permite que um programa escolha entre duas alternativas. O código dentro do bloco é executado se a condição especificada for verdadeira, caso contrário, o programa continua sua execução normalmente. A sintaxe geral em várias linguagens de programação é:

```
if (condição) {
    // Código a ser executado se a condição for verdadeira
}
```
#### Exemplo em pseudo-código:

```
Se (idade >= 18) {
    Escreva("Você é maior de idade")
}
```
### Estrutura de Seleção Composta (ou Condicional Composta):
A estrutura de seleção composta permite que um programa escolha entre duas ou mais alternativas. Ela usa a cláusula else para especificar o que deve ser feito se a condição não for verdadeira. A sintaxe geral em várias linguagens de programação é:
```
var idade = 20;

if (idade >= 18) {
    console.log("Você é maior de idade");
}
```
#### Exemplo em pseudo-código:

```
Se (idade >= 18) {
    Escreva("Você é maior de idade")
} Senão {
    Escreva("Você é menor de idade")
}
```
### Estrutura de Seleção Múltipla (ou Condicional Múltipla ou Switch/Case):
A estrutura de seleção múltipla permite que um programa escolha entre várias alternativas com base em valores discretos. Ela é frequentemente usada quando há uma lista de opções a serem consideradas. A sintaxe geral em várias linguagens de programação é:

```
var opcao = 2;

switch (opcao) {
    case 1:
        console.log("Você escolheu a opção 1");
        break;
    case 2:
        console.log("Você escolheu a opção 2");
        break;
    default:
        console.log("Opção inválida");
}

```
#### Exemplo em pseudo-código:

```
Escolha (opcao) {
    Caso 1:
        Escreva("Você escolheu a opção 1")
        Pare
    Caso 2:
        Escreva("Você escolheu a opção 2")
        Pare
    Caso Contrário:
        Escreva("Opção inválida")
}
```
As estruturas de seleção são fundamentais para controlar o fluxo de execução de um programa, permitindo que ele tome decisões com base nas condições definidas. Elas são amplamente utilizadas em programação para criar lógica complexa e tomar decisões dinâmicas com base nos dados e nas entradas do usuário.


## Exemplo feito na aula

#### Hello Word !
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

    </form>

    <script>
        var nome = 'João'; //String = texto //linguagem fracamente tipada 
        var dor = true; //false 
        var temperatura = 38; 
        
        if (nome == "Ivan" 
        || nome == "João") {
            console.log('Hellow World! ' + nome);
        } else {
            console.log('Ops Não te conheço...!!!');
        }

    

    </script>
</body>
</html>
```
#### Estrutura de Seleção com JavaScript

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
        <input type="text" id="idTosse" placeholder="Tosse? V ou F"> <br><br>
        <input type="text" id="idDorGranganta" placeholder="Dor de Garganta? V ou F"><br><br>
        <input type="number" id="idFebre" placeholder="Febre? Graus"><br><br>
        <input type="text" id="idFaltaAr" placeholder="Falta de Ar? V ou F"><br><br>
        <input type="button" value="Testar" onclick="testar()">
    </form>

    <script>
        
        function testar() {
            var tosse = document.getElementById("idTosse").value;
            var dorDeGarganta = document.getElementById("idDorGranganta").value;
            var febre = document.getElementById("idFebre").value;
            var faltaDeAr = document.getElementById("idFaltaAr").value; 
            
            if ((tosse == "V" && dorDeGarganta == "V") 
            ||  (febre >= 38 && faltaDeAr == "V")) {
                console.log("Procurar Médico");
            } else {
                console.log("Fique em Casa"); 
            }
        }


    </script>
</body>
</html>
```



![logo entra 21](https://cdn.sonicadigital.com.br/entra21/storage/header/257/original-61f8610472d4f.png)

