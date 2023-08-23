

# O que é Repositório Local e Repositório Remoto


<p><img alt="Git GitHub" title="" src="https://terminalroot.com.br/assets/img/cursos/git.jpg" /></p>

## Repositório Local

Um repositório local é um diretório em sua máquina onde você mantém e gerencia seus arquivos de projeto, histórico de versões e informações de controle de código usando o sistema de controle de versão Git. O Git permite que você controle as mudanças feitas nos arquivos ao longo do tempo, criando commits que representam snapshots do estado dos arquivos em um determinado momento.

Principais características de um repositório local:

- **Histórico de Versões:** O Git mantém um histórico completo de todas as alterações feitas nos arquivos ao longo do tempo, permitindo que você acompanhe o progresso do projeto e reverta para versões anteriores se necessário.

- **Trabalho Offline:** Você pode fazer commits e alterações em seu repositório local sem precisar de conexão com a internet. Isso é útil quando você está trabalhando em um ambiente desconectado.

## Repositório Remoto

Um repositório remoto é um repositório hospedado em um servidor online, como o GitHub. Ele serve como um local centralizado onde você pode compartilhar seu código com outros colaboradores, permitindo que eles vejam, revisem e contribuam para o projeto. O GitHub fornece uma plataforma para armazenar, gerenciar e colaborar em projetos usando o Git.

Principais características de um repositório remoto:

- **Colaboração:** Múltiplos desenvolvedores podem colaborar em um projeto compartilhando suas alterações no repositório remoto. Isso permite que eles trabalhem simultaneamente sem conflitos.

- **Backup:** O repositório remoto serve como um backup seguro para o código-fonte do projeto. Se ocorrerem problemas no repositório local, você ainda terá uma cópia segura no repositório remoto.

- **Acesso Universal:** Como o repositório remoto é acessível pela internet, ele permite que colaboradores de diferentes locais e equipes acessem e contribuam para o projeto.

#### Os repositórios locais e remotos são elementos fundamentais no desenvolvimento de software usando o Git e GitHub. Eles permitem que você gerencie e compartilhe seu código de forma eficaz, tornando a colaboração e o controle de versão mais eficientes e organizados.

# Tutorial de Uso do Git e GitHub

Este tutorial fornece um guia passo a passo sobre como usar o Git para controle de versão e o GitHub para hospedar seus projetos.
Com apoio em aprendizado com o professor Ivan-J-Borchardt no curso Entra21.

## Passo 1: Instalação

- Faça o download e instale o Git em sua máquina a partir do site oficial: [https://git-scm.com/downloads](https://git-scm.com/downloads).

## Passo 2: Configuração Inicial

- Configure seu nome de usuário e endereço de e-mail no Git:
```
   git config --global user.name "Seu Nome"
   git config --global user.email "seu@email.com"
```
## Passo 3: Iniciando um Repositório Local
- Crie uma pasta para o seu projeto e navegue até ela no terminal.
- Inicie um novo repositório Git:
```
git init
```
## Passo 4: Adicionando e Comitando Mudanças
- Crie ou copie os arquivos do seu projeto para a pasta do repositório.
- Adicione os arquivos ao controle de versão:
```
git add nome-do-arquivo
```
- Realize um commit das mudanças:
```
git commit -m "Mensagem descritiva das mudanças"
```
## Passo 5: Criando um Repositório no GitHub
- Acesse o GitHub em https://github.com e faça login na sua conta.
- Clique no sinal '+' no canto superior direito e escolha "New Repository".
- Preencha o nome do repositório, descrição e configurações desejadas. Clique em "Create Repository".

## Passo 6: Conectando Repositório Local ao GitHub
- Copie a URL do repositório criado no GitHub.
- No terminal, adicione o link remoto ao repositório local:
 ```
 git remote add origin URL-do-Repositório
```
- Envie suas mudanças locais para o GitHub:
 ```
git push -u origin master
```
- O origin master é padrão podendo sempre usando o mesmo
- Para verifica se esta mesmo na master pode digitar o comando:

```
git status
```
- Se esteja em outro repositório como por exemplo a main
- Caso precise mudar para a Main digite os seguintes códigos:
```
git branch -M main
```
- Fazendo esses passos logo após digite status para a verificação
  
## Passo 7: Clonando Repositório do GitHub

- Acesse a página do repositório que deseja clonar. O endereço normalmente é composto pelo site do github + nome do usuáiro + nome do repositório + '.git'.
- Você pode conseguir esse endereço acessando a página do repositório no GitHub e clicando em 'Clonar' ou 'Clone', conforme imagem a seguir:


    <img  align="center" alt="Git GitHub" src="https://www.alura.com.br/artigos/assets/clonando-repositorio-git-github/imagen18_1.gif" />


- No terminal, acesse a pasta onde deseja clonar o repositório. Normalmente, ao abrirmos o terminal, ele abre dentro do usuário padrão. 
- Considerando isso, rodamos o comando para acessar a pasta onde salvaremos o repositório.
- Com isso digite o comando a seguir:
```
git clone (http do seu projeto que foi copiado conforme a imagem anterior)
```
- Esse comando irá criar uma pasta (no local onde rodou o comando) com o nome do repositório (e todas suas pastas e arquivos).

## Passo 8: Baixar as atualizações do repositório original
- Depois que já temos nosso repositório em ambiente local, é necessário sempre mantê-lo atualizado.
- Para isso, sempre que formos iniciar uma tarefa, rodamos o comando:
```
git pull
```
- Esse comando baixa as novidades do repositório para nossa máquina.
- Definindo que queremos puxar as atualizações da branch master do repositório remoto de origem:
```
git pull origin master
```  
- E está feito! Seu repositório está atualizado!

- Autor Francine dos Santos


 
