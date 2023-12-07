# API REST (Representational State Transfer)
O REST (Representational State Transfer) é um modelo de arquitetura para sistemas distribuídos que foi concebido por Roy Fielding, um dos principais autores do protocolo HTTP, em 2000. Ele listou diversos modelos arquiteturais, e o REST se destacou como uma abordagem eficaz para o desenvolvimento de sistemas distribuídos, servindo como base para o próprio protocolo HTTP.

# Conceitos: RESTful
Recursos
No contexto REST, um recurso pode ser entendido como uma entidade ou modelo de dados. Alguns exemplos de recursos podem incluir Aluno, Tópico, Curso e Disciplina.

# Identificador de Recursos (URI)
Cada recurso é identificado por uma URI (Uniform Resource Identifier). Por exemplo:

- Recursos:
    -  Aluno  --> Entidade/Modelo 
    -  Topico 
    -  Curso 
    -  Disciplinas
  - Identificador de Recursos (URI): 
    -  Aluno(/aluno) 
    -  Topico(/topico) 
    -  Curso(/curso) 
    -  Disciplina(/disciplina)  
  
- Manipulação de Recursos (Verbos HTTP)
- O REST segue o padrão CRUD (Create, Read, Update, Delete) para manipulação de recursos, utilizando os seguintes verbos HTTP:

~~~
       CRUD - Create, Read, Update, Delete
       ====== 
       Consultas   GET/aluno     
                   GET/aluno/{id}
       Criar Novo  POST/aluno 
       Alterar     PUT/aluno
                   PUT/aluno/{id}
       Apagar      DELETE/aluno 
                   DELETE/aluno/{id}        
~~~ 
## Representação de Recursos (Media Type)
Os recursos podem ser representados em diferentes formatos, como JSON, XML, TXT, HTML, Binário, etc. Exemplos de representações em JSON e XML para um recurso Aluno seriam:

JSON:

```json
{
    "aluno": {
        "userId": "XPTO123",
        "nome": "John Von Neumann",
        "tipo": "adm"
    }
}

```

XML:

```xml
<aluno>
    <userId>XPTO123</userId>
    <nome>John Von Neumann</nome>
    <tipo>adm</tipo>
</aluno>
```

# Comunicação Stateless
O REST opera de forma stateless, o que significa que cada solicitação do cliente para o servidor deve conter todas as informações necessárias para entender e processar a solicitação. O servidor não mantém estado da sessão do cliente entre as solicitações.

- Comunicação Stateless (não mantém sessão aberta) 

- HTTP Status Codes
O protocolo HTTP utiliza códigos de status para indicar o resultado da solicitação. Alguns códigos comuns podem ser encontrados aqui. Esses códigos incluem informações sobre o sucesso, redirecionamento, erro do cliente, erro do servidor, entre outros.



### HTTP status codes

- https://developer.mozilla.org/en-US/docs/Web/HTTP/Status 
