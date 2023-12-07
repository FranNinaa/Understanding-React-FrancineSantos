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

1. Abra um navegador e acesse **http://localhost:3000/**.

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

# Devolver Paginas HTML


Devolver páginas HTML é uma prática essencial em desenvolvimento web, onde os servidores web respondem às solicitações dos clientes, geralmente navegadores, enviando conteúdo HTML para ser renderizado e exibido aos usuários. A entrega de páginas HTML é fundamental para a experiência do usuário na web, uma vez que o HTML (Hypertext Markup Language) é a linguagem de marcação padrão para a estruturação e apresentação de conteúdo em páginas web.

Ao solicitar uma página web, o navegador envia uma requisição para o servidor correspondente. O servidor, por sua vez, processa a requisição e devolve uma resposta, muitas vezes contendo um documento HTML, juntamente com outros recursos como folhas de estilo (CSS), scripts (JavaScript), imagens e muito mais. A combinação desses recursos forma a página web completa que os usuários visualizam em seus navegadores.

A resposta do servidor, geralmente entregue usando protocolos como HTTP, pode conter códigos de status indicando o sucesso ou falha da requisição. Para devolver páginas HTML, os desenvolvedores utilizam frameworks e bibliotecas, como o Express.js para Node.js, Django para Python, ou Ruby on Rails para Ruby, que facilitam a criação de rotas, manipulação de requisições e respostas, e a renderização de arquivos HTML.

Além disso, a evolução das práticas de desenvolvimento web trouxe à tona abordagens mais modernas, como a criação de SPAs (Single Page Applications) usando frameworks como React, Angular e Vue.js. Nesses casos, a entrega inicial de uma página HTML é seguida por interações dinâmicas do lado do cliente, onde o conteúdo da página é atualizado sem a necessidade de carregamentos completos.

Em resumo, devolver páginas HTML é um aspecto fundamental do desenvolvimento web, formando a base para a construção de interfaces de usuário e proporcionando uma experiência coesa e interativa aos usuários da web. A compreensão eficiente dessa prática é crucial para desenvolvedores que buscam criar aplicações web robustas e amigáveis.


## Exemplo em aula

```js
const express = require("express")
const path = require("path")


const app = express()

const porta = 3001
app.listen(porta, function() {
    console.log(`Servidor Rodando na porta ${porta}`);
})


app.get("/", function(req, resp){

    console.log("__dirname: " + __dirname);
    console.log("basename: " + path.basename(__dirname));
    console.log("dirname: " + path.dirname(__dirname));
    console.log("extname: " + path.extname("index.html"));

    resp.sendFile(path.join(__dirname + "/paginas/index.html"))
})
```

### Explicação do código do exemplo da aula

## Importação de Módulos:

```javascript
const express = require("express"): // Importa o módulo Express para criar o servidor.
const path = require("path"): // Importa o módulo path para manipulação de caminhos de arquivos e diretórios.
```

- Configuração do Servidor:

```javascript
const app = express(): // Cria uma instância do aplicativo Express.
const porta = 3001: // Define a porta na qual o servidor irá escutar.

```

- Iniciando o Servidor:

```javascript
app.listen(porta, function() {...}: // Inicia o servidor e exibe uma mensagem no console indicando que o servidor está rodando na porta especificada.
```

- Rota para a Página Inicial ("/"):

```javascript
app.get("/", function(req, resp) {...}: // Define uma rota para a raiz do servidor (página inicial).
resp.sendFile(path.join(__dirname + "/paginas/index.html")): // Devolve a página HTML localizada no diretório "paginas".
```

- Log de Informações sobre Diretórios:
```javascript
console.log("__dirname: " + __dirname): // Exibe o caminho do diretório atual.
console.log("basename: " + path.basename(__dirname)): // Exibe o nome do diretório.
console.log("dirname: " + path.dirname(__dirname)): // Exibe o caminho do diretório pai.
console.log("extname: " + path.extname("index.html")): // Exibe a extensão do arquivo especificado.

```
O código em geral serve para criar um servidor Express simples que escuta na porta 3001 e retorna a página HTML localizada no diretório "paginas" quando a rota raiz ("/") é acessada.

Certifique-se de que o arquivo index.html está presente no diretório paginas e que a estrutura do seu projeto esteja organizada adequadamente para que o caminho para o arquivo seja construído corretamente. Se a estrutura do seu projeto não incluir o diretório paginas no mesmo nível que o arquivo JavaScript, você precisará ajustar o caminho em path.join(__dirname + "/paginas/index.html").

# Consistencia em arquivos CSV

Consistência ao lidar com arquivos CSV é crucial para garantir a integridade e a interpretabilidade dos dados. Abaixo estão algumas práticas importantes para manter a consistência ao trabalhar com arquivos CSV no código fornecido:

- Delimitadores Consistentes:

Garanta que o delimitador usado no arquivo CSV seja consistente em todo o processo de leitura e escrita. No código fornecido, você está utilizando a vírgula (,) como delimitador. Certifique-se de que esta escolha seja mantida em todo o seu código.

- Tratamento de Linhas Vazias:

Considere como lidar com linhas vazias no arquivo CSV. No código fornecido, você está dividindo as linhas usando users.split("\r\n"). Certifique-se de que este método seja robusto o suficiente para lidar com diferentes formatos de quebras de linha e para não quebrar se uma linha estiver vazia.

- Gestão de Cabeçalhos:

Se o arquivo CSV incluir um cabeçalho (uma linha que descreve o conteúdo de cada coluna), certifique-se de tratar essa linha de maneira consistente. No exemplo, você está criando objetos com propriedades específicas baseadas em índices. Se houver um cabeçalho no CSV, considere usar esses nomes como chaves de propriedade.

- Validação dos Dados:

Implemente validação adequada para os dados do CSV. Certifique-se de que os valores estejam nos formatos esperados e, se possível, implemente tratamentos para valores ausentes ou inválidos.

- Formato de Data e Hora:

Se o CSV incluir datas ou horas, certifique-se de que você está interpretando e formatando esses valores de maneira consistente. O JavaScript oferece várias maneiras de lidar com datas, e a escolha depende das necessidades específicas do seu aplicativo.

- Manipulação de Aspas:

Considere como você deseja lidar com aspas em torno dos valores no CSV. Alguns arquivos CSV usam aspas para encapsular valores que podem conter o delimitador. Certifique-se de tratar esses casos de maneira consistente.

- Tratamento de Erros no CSV:

Implemente tratamentos adequados para erros que possam ocorrer durante a leitura ou processamento do arquivo CSV. Isso inclui tratamento de erros ao dividir as linhas e ao acessar índices no array resultante.

- Documentação:

Documente claramente o formato esperado do CSV, especialmente se estiver compartilhando arquivos ou trabalhando em equipe. Isso ajuda a garantir que todos estejam cientes das expectativas em relação à estrutura do arquivo.
Ao seguir essas práticas, você contribuirá para a consistência e confiabilidade no manuseio de arquivos CSV em seu código.

# Exemplo feito em aula

```js
const fs = require("fs/promises")

const config = {
    param1: "Parametro1",
    param2: 1234,
    param3: "Direita"
}

//salvar(JSON.stringify(config))
//adicionarDado(JSON.stringify(config))
//lerArquivo()
lerUsers()

async function salvar(dado) {
    await fs.writeFile("config.txt", dado)
}

async function adicionarDado(dado) {
    await fs.appendFile("config.txt", dado + "\n")
}

async function lerArquivo() {
    try {
        const dado = await fs.readFile("config.txt", "utf-8")

    } catch (error) {
        console.log(error.name);
        console.log(error.message);
        console.log(error.stack);
    }



    console.log(dado);
    console.log(JSON.parse(dado).param1);
}

//Trabalhando com um arquivo csv
async function lerUsers() {

    var  users
    try {
        users = await fs.readFile("users1.csv", "utf-8")
        const user = users.split("\r\n")
        const userDetails = []
    
        user.forEach(element => {
            //userDetails.push(element.split(","))
            let userArray = element.split(",")
    
            let user = {
                userId: userArray[0],
                nome: userArray[1],
                linguagem: userArray[2],
                ano: userArray[3]
            }
    
            userDetails.push(user)
    
            console.log(user);
        })
    
        console.log(userDetails);
    
    } catch (error) {
        console.log(error.name);
        console.log(error.message);
        console.log(error.stack);
        console.log(error);
    }
}
```

O código fornecido acima lida com operações de leitura e escrita de arquivos usando o módulo fs/promises do Node.js. Para manter a consistência nos arquivos, você pode considerar as seguintes práticas:

- Padrões de Nomenclatura:

Certifique-se de seguir padrões consistentes ao nomear seus arquivos. Por exemplo, usar letras minúsculas, separar palavras com underscores ou camelCase, e escolher nomes descritivos para facilitar a compreensão do conteúdo.

- Manipulação de Erros:

Implemente consistência ao lidar com erros. No código fornecido, você já tem blocos try-catch que capturam erros. Considere padronizar as mensagens de erro e ações a serem tomadas em caso de falhas.

- Formatação e Estilo:

Mantenha uma formatação e estilo consistentes em seu código para facilitar a leitura. Use espaçamento e indentação de maneira uniforme em todo o código.

- Comentários e Documentação:

Inclua comentários que expliquem partes importantes do código, especialmente se outras pessoas ou você mesmo precisarem entender o propósito de determinadas funções ou trechos. Documentar a estrutura dos arquivos e o formato dos dados pode ser crucial.

- Manipulação de Strings e Arquivos CSV:

Quando estiver manipulando strings ou lendo arquivos CSV, certifique-se de que a estrutura dos dados seja consistente. No exemplo do arquivo CSV, parece que você está esperando que cada linha seja dividida em elementos usando vírgulas. Garanta que todos os arquivos CSV sigam esse padrão.

- Caminhos Relativos ou Absolutos:

Considere usar caminhos relativos de maneira consistente ao acessar arquivos. Isso facilita a portabilidade do código entre diferentes ambientes.

- Tratamento de Buffer ou Strings:

Ao trabalhar com readFile, esteja ciente de que o retorno pode ser um buffer ou uma string, dependendo das opções fornecidas. Certifique-se de tratar a resposta de acordo para manter consistência

arquivo **users.csv**
```js
cbl1,Grace Hopper,Cobol,1950
js1,Brendan Eich,JavaScript,1993
jv1,Patrick Naughton,Java,1991
```

O arquivo users.csv contém um formato CSV (Comma-Separated Values), que é um formato de armazenamento de dados onde os valores são separados por vírgulas. Cada linha no arquivo representa um conjunto de dados associado a um usuário específico. A estrutura do arquivo parece seguir um padrão específico:

- Formato CSV:

O arquivo utiliza a vírgula **(,)** como delimitador entre os valores. Cada linha é composta por campos que representam atributos associados a um usuário.

- Estrutura das Linhas:

- Cada linha no arquivo representa um usuário e contém quatro campos separados por vírgulas.
- O primeiro campo **(cbl1, js1, jv1)** parece ser um identificador ou código único para cada usuário.
- O segundo campo **(Grace Hopper, Brendan Eich, Patrick Naughton)** contém o nome do usuário.
- O terceiro campo **(Cobol, JavaScript, Java)** representa a linguagem associada ao usuário.
- O quarto campo **(1950, 1993, 1991)** indica o ano associado ao usuário.
Exemplos de Linhas:

As três linhas presentes no exemplo do arquivo users.csv fornecem informações sobre três usuários distintos:

 - Linha 1: Identificador cbl1, nome Grace Hopper, linguagem Cobol, ano 1950.
- Linha 2: Identificador js1, nome Brendan Eich, linguagem JavaScript, ano 1993.
- Linha 3: Identificador jv1, nome Patrick Naughton, linguagem Java, ano 1991.
- 
Essas informações são organizadas de maneira tabular e são frequentemente utilizadas para representar conjuntos de dados em aplicativos, bancos de dados, ou em situações onde a organização em colunas e linhas é conveniente.

Ao ler esse arquivo em seu código, você está processando esses dados para criar objetos representando usuários, onde cada objeto tem propriedades como userId, nome, linguagem, e ano. A manipulação desses dados pode incluir operações como exibição, filtragem, ou qualquer outra ação específica que você deseje realizar com as informações sobre os usuários contidas no arquivo CSV.

# Autenticação JWT

A autenticação JWT (JSON Web Token) é um método popular para autenticar usuários em aplicativos web e serviços. É um padrão aberto (RFC 7519) que define uma maneira compacta e autocontida de representar informações entre duas partes de maneira segura. Os JWTs são frequentemente usados como tokens de acesso em sistemas de autenticação e autorização.

Aqui estão alguns conceitos chave relacionados à autenticação JWT:

- Estrutura do JWT:

Um JWT consiste em três partes: o cabeçalho (header), a carga útil (payload), e a assinatura (signature). Cada parte é base64url-encoded, separada por pontos. O resultado final é algo como "xxxxx.yyyyy.zzzzz".
Cabeçalho (Header):

O cabeçalho geralmente consiste em duas partes: o tipo do token, que é JWT, e o algoritmo de hash utilizado para assinar o token, como HMAC SHA256 ou RSA.

- Carga Útil (Payload):

A carga útil contém as chamadas "afirmações". As afirmações são declarações sobre uma entidade (normalmente o usuário) e metadados adicionais. Existem três tipos de afirmações: registradas, públicas e privadas. As afirmações registradas são um conjunto de afirmações predefinidas (como expiração e emissão), as afirmações públicas podem ser definidas por quem quiser usar o JWT, e as afirmações privadas são acordadas entre as partes.

- Assinatura (Signature):

A assinatura é gerada a partir do cabeçalho, da carga útil e de uma chave secreta (ou chave pública, no caso de JWTs assinados por RSA ou ECDSA). A assinatura é usada para verificar que a mensagem não foi alterada ao longo do caminho e, no caso de tokens de acesso, para verificar se o remetente é quem diz ser.

- Processo de Autenticação JWT:

O processo típico de autenticação com JWT envolve o seguinte:
- O cliente fornece suas credenciais (geralmente nome de usuário e senha) para o servidor.
- O servidor verifica as credenciais e, se válidas, gera um JWT, que é assinado usando uma chave secreta conhecida apenas pelo servidor.
- O JWT é retornado para o cliente.
- O cliente armazena o JWT (geralmente em cookies ou local storage) e o inclui nas solicitações para recursos protegidos.
- O servidor verifica a assinatura do JWT para garantir que o token seja válido e não tenha sido adulterado.
  
- Se o JWT for válido, o servidor permite o acesso aos recursos protegidos.
Vantagens:

Os JWTs são autossuficientes e não exigem que o servidor armazene informações adicionais sobre a sessão do usuário, tornando-os escaláveis e fáceis de implementar.
São frequentemente utilizados em arquiteturas stateless, onde o estado da sessão é mantido no lado do cliente.

- Desafios:

Os JWTs devem ser manuseados com cuidado, especialmente ao armazenar informações sensíveis no payload, pois podem ser decodificados facilmente pelo cliente.
A revogação de tokens pode ser desafiadora, já que os JWTs geralmente têm vida útil limitada.
A autenticação JWT é amplamente adotada e oferece uma solução eficaz para a autenticação em sistemas distribuídos e APIs. No entanto, é importante entender suas características e considerar fatores de segurança ao implementá-la.

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
    <!-- Campos de entrada para usuário e senha -->
    <input type="text" id="idUser" placeholder="userId"><br>
    <input type="text" id="idPass" placeholder="password"><br><br>

    <!-- Botões para realizar ações de login, logout e um teste -->
    <input type="button" value="login" onclick="login()">
    <input type="button" value="logout" onclick="logout()">
    <input type="button" value="teste" onclick="user()">

    <script>
        async function login() {
            // Obtenção dos valores dos campos de entrada
            let user = document.getElementById("idUser").value
            let senha = document.getElementById("idPass").value

            // Configuração das opções para a requisição POST de login
            const options = {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({
                    "user": user,
                    "password": senha
                })
            };

            // Realização da requisição de login
            let res = await fetch('http://localhost:3000/login', options)
            
            // Obtenção do token de autenticação da resposta
            let autenticacao = await res.json()

            // Armazenamento do token na sessão do navegador
            sessionStorage.setItem("auth", autenticacao.token)

            console.log(autenticacao);
        }

        async function logout() {
            // Configuração das opções para a requisição POST de logout
            const options = {
                method: 'POST',
                headers: {
                    'x-access-token': sessionStorage.getItem("auth")
                }
            };

            // Remoção do token da sessão do navegador
            sessionStorage.removeItem("auth")
            
            // Realização da requisição de logout
            let res = await fetch('http://localhost:3000/logout', options)
            
            console.log(res.status);
        }

        async function user() {
            // Configuração das opções para a requisição GET de informações do usuário
            const options = {
                method: 'GET',
                headers: {
                    'x-access-token': sessionStorage.getItem("auth")
                }
            };

            // Realização da requisição para obter informações do usuário
            let res = await fetch('http://localhost:3000/user', options)
            
            console.log(res.status);
        }
    </script>

</body>

</html>

```

### Arquivo server.js

```js
import express from "express"
import jwt from "jsonwebtoken"
import path from "path"
import { fileURLToPath } from 'url';

// Obtém o caminho do diretório atual
const __filename = fileURLToPath(import.meta.url);
const __dirname = path.dirname(__filename);

// Chave secreta para assinar tokens JWT
const SECRET = process.env.SECRET || "dfghj&%$GHH5/hbj54"
const app = express()

// Middleware para permitir o uso de JSON nas requisições
app.use(express.json())

// Middleware para verificar a autenticação usando JWT
function verificarJWT(req, res, next) {
    // Obtém o token do cabeçalho da requisição
    const token = req.header("x-access-token")

    // Verifica se o token está na lista negra
    const indexTokenBlack = blacklist.findIndex(tokenLista => tokenLista == token)

    // Se o token estiver na lista negra, nega o acesso
    if (indexTokenBlack > -1) {
        res.status(401).end()
    }

    // Verifica se o token é válido usando a chave secreta
    jwt.verify(token, SECRET, function(error, decoded) {
        if (error) {
            res.status(401).end()
        }

        // Se o token for válido, permite a próxima etapa da requisição
        next()
    })
}

// Rota para servir o arquivo front.html
app.get("/", (req, res)=>{
    res.sendFile(__dirname + "/front.html")
})

// Rota protegida por autenticação JWT
app.get("/user", verificarJWT,  (req, res)=>{
    res.status(200).send("Lista de usuários")
})

// Rota para realizar o login e gerar um token JWT
app.post("/login", (req, res)=>{
    if (req.body.user == "FT012" && req.body.password == "SohEuSei") {
        // Se as credenciais são válidas, gera um token com o userId e o expira em 60 segundos
        const token = jwt.sign({userId: 123}, SECRET, {expiresIn: 60})

        res.status(200).json({auth: true, token})
    } 

    // Se as credenciais são inválidas, retorna status 403 (Forbidden)
    res.status(403).end()
})

// Lista negra para tokens JWT inválidos
const blacklist = []

// Rota para realizar o logout adicionando o token à lista negra
app.post("/logout", (req, res)=>{
    blacklist.push(req.header("x-access-token"))
    res.status(200).end()
})

// Configuração do número da porta para o servidor
const PORT = process.env.PORT || 3000

// Inicia o servidor na porta especificada
app.listen(PORT, ()=> {
    console.log(`Servidor rodando na porta ${PORT}`); 
})

```
