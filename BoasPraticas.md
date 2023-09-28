# Boas Práticas na Programação
O emprego de boas práticas melhora a qualidade do código, ajuda a condicionar o raciocínio lógico e aumenta a produtividade!

## 1. Indentação é obrigatória
Indentar corretamente o código é fundamental. A indentação não deve ser vista como uma "muleta", mas sim como uma prática que auxilia nosso cérebro a pensar de forma estruturada. É importante realizar a indentação enquanto o código está sendo construído, o que facilita a leitura e compreensão da lógica do programa.

Exemplo em JavaScript:

```javascript
// Ruim
function myFunction() {
if(condition) {
doSomething();
}
}

// Bom
function myFunction() {
  if (condition) {
    doSomething();
  }
}
```

## 2. Nomes de variáveis, funções, procedimentos e parâmetros
Os nomes devem ser precisos e expressivos, transmitindo claramente a ideia central. Nomes extensos são aceitáveis se refletirem com precisão a função ou o parâmetro em questão.

Exemplo em JavaScript:

```javascript
// Ruim
let x = 10;

// Bom
let numeroDeEstudantes = 10;
```

## 3. Comentários
Comentários são essenciais para explicar o que um trecho de código faz. Recomenda-se criar os comentários antes do código, descrevendo o passo a passo que o código deverá seguir para alcançar o resultado, e depois preencher esse passo a passo com o código.

Exemplo em JavaScript:

```javascript
// Ruim
// Função para calcular
function calcular(x, y) {
  return x + y;
}

// Bom
// Função para calcular a soma de dois números
function calcularSoma(x, y) {
  return x + y;
}
```

### 4. Prefira um código legível (de fácil leitura) a um código "menos verboso"
O código fonte é escrito para seres humanos, portanto, priorize a clareza e legibilidade. Evite códigos excessivamente compactos que dificultem a compreensão.

Exemplo em JavaScript:

```javascript
// Ruim
const result = a+b*c;

// Bom
const resultado = a + (b * c);
```

### 5. Use e Abuse do Ctrl+C, Ctrl+V e do auto-complete da IDE
Aproveite as ferramentas disponíveis, como o uso do atalho de copiar e colar (Ctrl+C, Ctrl+V) e o auto-complete da IDE. Essas ferramentas ajudam a evitar erros de digitação e aumentam a produtividade durante o desenvolvimento.

## 6. Não deixe para testar apenas no final
É fundamental testar o programa à medida que cada pequena funcionalidade é criada. Realize testes frequentes, mesmo entre pequenas alterações, para identificar e corrigir eventuais problemas de forma proativa.

## 7. Padronização de código
Adote um estilo de codificação consistente em todo o projeto. Isso inclui a formatação, indentação, uso de espaços, e outros aspectos que tornam o código visualmente coeso.

Exemplo em JavaScript:

```javascript
// Ruim (inconsistente)
function funcaoA() {
    return 42;
}

function funcaoB() {
    return 42;
}

// Bom (consistente)
function funcaoA() {
    return 42;
}

function funcaoB() {
    return 42;
}
```

### 8. Divisão modular do código
Separe o código em funções, classes ou módulos pequenos e coesos, cada um responsável por uma tarefa específica. Isso facilita a leitura, manutenção e reutilização do código.

Exemplo em JavaScript:

```javascript
// Ruim (função com muitas responsabilidades)
function processarDados(dados) {
    // Código extenso...
}

// Bom (funções com responsabilidades separadas)
function validarDados(dados) {
    // Código de validação...
}

function processarDadosValidos(dados) {
    // Processamento de dados válidos...
}

function processarDadosInvalidos(dados) {
    // Tratamento de dados inválidos...
}
```

## 9. Gestão de exceções adequada
Manuseie exceções de forma apropriada, fornecendo mensagens de erro úteis e capturando apenas as exceções necessárias para o contexto. Evite capturar exceções genéricas.

Exemplo em JavaScript:

```javascript
// Ruim (captura de exceção genérica)
try {
    resultado = operacaoArriscada();
} catch (e) {
    console.error("Ocorreu um erro:", e);
}

// Bom (captura de exceção específica)
try {
    resultado = operacaoArriscada();
} catch (error) {
    console.error("Ocorreu um erro:", error);
}
```

## Conclusão
Adotar boas práticas na programação é fundamental para garantir a qualidade e a manutenibilidade do código. Ao seguir essas diretrizes, você estará no caminho certo para produzir código limpo, legível e de alta qualidade em JavaScript.
A aplicação dessas boas práticas na programação contribui para o desenvolvimento de código mais robusto, legível e fácil de manter. Além disso, ao seguir essas diretrizes, os programadores podem melhorar a eficiência e a produtividade durante o processo de desenvolvimento de software.