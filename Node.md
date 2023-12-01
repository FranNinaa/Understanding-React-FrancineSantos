# Introdução ao Node.js
## O que é o Node.js?
O Node.js é uma plataforma de execução de código JavaScript do lado do servidor, construída sobre o motor V8 do Google Chrome. Ele permite que os desenvolvedores usem JavaScript para escrever scripts do lado do servidor, o que tradicionalmente era feito usando linguagens como PHP, Python ou Ruby. O Node.js é conhecido por sua eficiência e escalabilidade, sendo amplamente utilizado para construir aplicativos web em tempo real e APIs.

## Como o Node.js Funciona?
O Node.js utiliza um modelo de I/O não bloqueante e assíncrono, o que o torna eficiente para manipular um grande número de conexões simultâneas. Ele é baseado em eventos, permitindo que os desenvolvedores criem aplicativos escaláveis e de alto desempenho.

O V8 engine, utilizado pelo Node.js, compila código JavaScript para código de máquina diretamente, o que resulta em execução rápida. A biblioteca principal do Node.js fornece funcionalidades para manipulação de arquivos, rede, HTTP e muito mais.

## Exemplo de Código
Hello World em Node.js
Crie um arquivo chamado hello.js com o seguinte conteúdo:

```js
// Importa o módulo http
const http = require('http');

// Cria um servidor HTTP que responde com "Hello, World!" para todas as solicitações
const server = http.createServer((req, res) => {
  res.writeHead(200, { 'Content-Type': 'text/plain' });
  res.end('Hello, World!\n');
});

// Ouve na porta 3000
const port = 3000;
server.listen(port, () => {
  console.log(`Servidor rodando em http://localhost:${port}/`);
});

```
## Executando o Código
1. Abra o terminal na pasta onde o arquivo hello.js está localizado.

2. Execute o seguinte comando para iniciar o servidor:
   

- node hello.js

3. Abra um navegador e acesse **http://localhost:3000/**.

Você verá a mensagem "Hello, World!" sendo exibida. Este é um exemplo simples para começar a entender como o Node.js funciona.

# Personalizando o Servidor
Você pode personalizar o servidor conforme suas necessidades, manipulando diferentes tipos de solicitações, processando parâmetros da URL, servindo arquivos estáticos e muito mais. O exemplo acima é apenas o ponto de partida.

# Recursos Adicionais
**Express.js:** Para construir aplicativos web mais complexos e estruturados, considere o uso do framework Express.js. Ele simplifica o roteamento, manipulação de middleware e muito mais.

**npm:** Use o npm (Node Package Manager) para instalar pacotes e módulos de terceiros que podem ser úteis para o desenvolvimento do seu servidor.

# Conclusão
O Node.js é uma ferramenta poderosa para o desenvolvimento de aplicativos web eficientes e escaláveis. Este README oferece uma introdução básica, e há muito mais recursos e módulos disponíveis para explorar conforme você avança em sua jornada com o Node.js. Consulte a documentação oficial em **nodejs.org** para aprender mais sobre suas capacidades e funcionalidades. 

# Introdução a Módulos em Node.js
O que são Módulos em Node.js?
Em Node.js, os módulos são unidades de código encapsuladas, projetadas para tornar o código mais organizado, reutilizável e fácil de manter. Cada arquivo JavaScript em Node.js é considerado um módulo, e você pode criar módulos personalizados para dividir seu código em partes mais gerenciáveis.

# Como Funcionam os Módulos em Node.js?
Os módulos em Node.js seguem o padrão CommonJS, que define uma maneira simples e eficaz de criar, importar e exportar módulos.

# Exemplo Básico de Módulo
Considere dois arquivos: moduloA.js e moduloB.js.

moduloA.js:

```js

// Exporta uma função
exports.saudacao = function() {
    return "Olá do Módulo A!";
};
```

**moduloB.js:**

```js
// Importa o móduloA
const moduloA = require('./moduloA');

// Usa a função exportada
console.log(moduloA.saudacao()); // Saída: Olá do Módulo A!
```
# Executando o Exemplo
Crie os arquivos moduloA.js e moduloB.js na mesma pasta.

No terminal, execute o seguinte comando no diretório dos arquivos:

**node moduloB.js**
- A saída será: Olá do Módulo A!

Este é um exemplo simples de como os módulos podem ser criados e utilizados em Node.js.

# Importante Saber
- Caminho Relativo ou Absoluto: Ao importar módulos, você pode usar caminhos relativos **(como ./moduloA)** ou caminhos absolutos para especificar a localização do módulo.

- Módulos Internos: **Node.js** possui uma série de módulos internos **(core modules)** que oferecem funcionalidades essenciais, como **fs** para operações de sistema de arquivos e http para criar servidores web.

- npm e Módulos de Terceiros: Node.js usa o sistema de gerenciamento de pacotes npm para instalar e gerenciar módulos de terceiros. Você pode instalar módulos adicionais usando o comando npm install.


Entender como trabalhar com módulos é fundamental para o desenvolvimento em **Node.js**. A modularidade não apenas facilita a organização do código, mas também promove a reutilização de código, tornando o desenvolvimento mais eficiente e sustentável. Consulte a documentação oficial do Node.js para obter mais informações sobre módulos e suas capacidades.


# Comando Guide NPM

# npm - Node Package Manager


Verificando se o npm está instalado
==============================================
retorna a versão no npm instalado, se instalado...

>npm -v 


Configurar o Projeto para ser um Projeto Node
===============================================
Cria o arquivo package.json, o sistema perguntará qual valor de cada variavel. 

>npm init   

O parametro "-y" inicializa as variáveis do package.json com valores default. 

>npm init -y 


Instalando o pacote Express:
=============================================== 
>npm install express@4.16.3 --save-exact


//(versão = @4.16.3)

>npm i nodemon -g 

Baixar todas as dependencias do projeto
===============================================
Para compartilhar o projeto, apagar a pasta nome_modules do projeto,
dessa forma, ao instalar o projeto em outro SO, basta baixar as 
dependencias novamente para manter a compatibilidade de SO

>npm install 

Opcionalmente pode-se abreviar o parâmetro install: 

>npm i

Instalando o nodemon
===============================================

>npm install nodemon -g 

//o -g significa que a instalação será global e não apenas 
//no projeto 

retorna o caminho do npm 
>npm  config get prefix 

# Publicando no NPM
1. Crie sua conta no NPM 
~~~
    https://www.npmjs.com/
~~~

2. Crie um repositório no GitHub e clone-o para sua máquina 

3. Crie um projeto Node 
~~~
    npm init
~~~
4. Crie seu módulo no index.js

5. Estando na pasta do projeto, faça login no NPM 
~~~
    npm login
~~~

6. Teste se vc está realmente logado 
~~~
    npm whoami
~~~

7. Publique o Módulo 
~~~
    npm publish
~~~

# Middleware em Node.js
# Introdução
O Middleware é uma peça fundamental na construção de aplicativos web usando Node.js, ajudando a facilitar o processamento de requisições HTTP de forma modular.

# O que é Middleware?
Middleware é um software situado entre o sistema operacional e as aplicações, agindo como um intermediário para gerenciar e facilitar comunicações. Em Node.js, middleware refere-se a funções que têm acesso aos objetos de solicitação (req), resposta (res), e à próxima função de middleware no ciclo de solicitação-resposta.

# Como Funcionam os Middlewares em Node.js?
Os middlewares são usados para executar ações durante o processamento de uma requisição HTTP. Eles podem realizar tarefas como:

- Modificar objetos de requisição ou resposta.
- Executar operações antes que a manipulação principal da requisição seja realizada.
- Finalizar a resposta antes que ela seja enviada de volta ao cliente.
- Executar operações em determinadas condições ou rotas.
- Exemplo Básico de Middleware
- Considere o seguinte exemplo de um middleware que loga informações sobre cada requisição:

```js
// Middleware de log
function logMiddleware(req, res, next) {
  console.log(`[${new Date().toISOString()}] ${req.method} ${req.url}`);
  next(); // Chama a próxima função de middleware no ciclo
}

// Aplicativo usando o middleware
const express = require('express');
const app = express();

// Usa o middleware globalmente para todas as rotas
app.use(logMiddleware);

// Rota principal
app.get('/', (req, res) => {
  res.send('Bem-vindo à minha aplicação!');
});

// Inicia o servidor na porta 3000
const port = 3000;
app.listen(port, () => {
  console.log(`Servidor rodando em http://localhost:${port}`);
});
```

# Personalizando e Utilizando Middleware
Você pode criar e utilizar middleware personalizado de acordo com as necessidades do seu aplicativo. O Express.js, um popular framework para Node.js, facilita a criação e utilização de middleware de maneira mais estruturada.

Explore bibliotecas de middleware existentes, como body-parser para analisar dados do corpo da requisição, morgan para logging avançado, entre outros.

Middleware é uma ferramenta poderosa em Node.js para modularizar e personalizar o processamento de requisições HTTP. Ao entender e utilizar efetivamente os middlewares, você pode melhorar a modularidade, a manutenção e a extensibilidade dos seus aplicativos web. Consulte a documentação do Express.js e outras bibliotecas relevantes para explorar opções avançadas e práticas recomendadas.