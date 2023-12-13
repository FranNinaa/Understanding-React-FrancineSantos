# Bancos de Dados Relacionais

Um banco de dados relacional é um tipo de banco de dados que organiza os dados em tabelas relacionadas. Essas tabelas são compostas por linhas e colunas, onde cada linha representa um registro e cada coluna representa um atributo.

Os bancos de dados relacionais são baseados no modelo relacional, que utiliza chaves primárias e chaves estrangeiras para estabelecer relações entre as tabelas. Essas relações permitem que os dados sejam consultados e manipulados de forma eficiente.

Uma das principais vantagens dos bancos de dados relacionais é a capacidade de garantir a integridade dos dados. Isso é feito através de restrições, como chaves primárias, chaves estrangeiras e regras de integridade referencial.

Além disso, os bancos de dados relacionais oferecem recursos avançados de consulta, como a linguagem SQL (Structured Query Language), que permite realizar operações complexas de busca, inserção, atualização e exclusão de dados.

No entanto, os bancos de dados relacionais também possuem algumas limitações. Por exemplo, eles podem ter dificuldades em lidar com grandes volumes de dados ou em escalar horizontalmente. Além disso, a estrutura rígida das tabelas pode dificultar a modelagem de dados complexos.

Apesar dessas limitações, os bancos de dados relacionais continuam sendo amplamente utilizados em diversas aplicações, devido à sua confiabilidade, segurança e capacidade de garantir a consistência dos dados.

## Funcionalidades do Banco de Dados Relacional

### Organização em tabelas relacionadas
Um banco de dados relacional organiza os dados em tabelas relacionadas. Cada tabela é composta por linhas (registros) e colunas (atributos), permitindo uma estrutura organizada e eficiente para armazenar e manipular os dados.

### Chaves primárias e chaves estrangeiras
O modelo relacional utiliza chaves primárias e chaves estrangeiras para estabelecer relações entre as tabelas. As chaves primárias são atributos únicos que identificam de forma exclusiva cada registro em uma tabela. As chaves estrangeiras são atributos que estabelecem relações entre tabelas, referenciando as chaves primárias de outras tabelas.

### Restrições e integridade dos dados
Os bancos de dados relacionais garantem a integridade dos dados através de restrições, como chaves primárias, chaves estrangeiras e regras de integridade referencial. Essas restrições ajudam a manter a consistência e a validade dos dados armazenados.

### Linguagem SQL (Structured Query Language)
A linguagem SQL é amplamente utilizada em bancos de dados relacionais para realizar operações de busca, inserção, atualização e exclusão de dados. Com o SQL, é possível realizar consultas complexas, criar e modificar tabelas, definir restrições e realizar outras operações relacionadas ao banco de dados.

### Recursos avançados de consulta
Os bancos de dados relacionais oferecem recursos avançados de consulta através da linguagem SQL. É possível realizar operações como junção de tabelas, filtragem de dados, ordenação, agregação e outras operações complexas para obter informações específicas dos dados armazenados.

### Confiabilidade, segurança e consistência dos dados
Uma das principais vantagens dos bancos de dados relacionais é a confiabilidade e segurança dos dados. Com as restrições e regras de integridade, é possível garantir a consistência dos dados armazenados. Além disso, os bancos de dados relacionais possuem mecanismos de backup e recuperação para proteger os dados contra falhas e perdas.

### Limitações dos bancos de dados relacionais
Apesar das vantagens, os bancos de dados relacionais também possuem algumas limitações. Eles podem ter dificuldades em lidar com grandes volumes de dados ou em escalar horizontalmente. Além disso, a estrutura rígida das tabelas pode dificultar a modelagem de dados complexos.


## Exemplo 1: Tabela Usuários

| ID | Nome  | Email              |
|----|-------|--------------------|
| 1  | João  | joao@example.com   |
| 2  | Maria | maria@example.com  |
| 3  | Pedro | pedro@example.com  |

## Exemplo 2: Tabela Produos

| ID | Nome        | Preço  |
|----|-------------|--------|
| 1  | Camiseta    | 29.99  |
| 2  | Calça Jeans | 59.99  |
| 3  | Sapato      | 79.99  |

## Exemplo 3: Tabela Pedidos

| ID | Usuário ID | Produto ID | Quantidade | Data       |
|----|------------|------------|------------|------------|
| 1  | 1          | 2          | 2          | 2021-08-01 |
| 2  | 2          | 1          | 1          | 2021-08-02 |
| 3  | 3          | 3          | 3          | 2021-08-03 |

# Exemplos de LInhas de comando em SQL

### Criar Tabela

 ```sql
CREATE TABLE NomeDaTabela (
    ID INT PRIMARY KEY,
    Nome VARCHAR(255),
    Email VARCHAR(255)
);

CREATE TABLE Produtos (
    ID INT PRIMARY KEY,
    Nome VARCHAR(255),
    Preco DECIMAL(10, 2)
);

 ```

### Inserir Dados

```sql
INSERT INTO NomeDaTabela (ID, Nome, Email)
VALUES
(1, 'João', 'joao@example.com'),
(2, 'Maria', 'maria@example.com'),
(3, 'Pedro', 'pedro@example.com');

INSERT INTO Produtos (ID, Nome, Preco)
VALUES
(1, 'Camiseta', 29.99),
(2, 'Calça Jeans', 59.99),
(3, 'Sapato', 79.99);

```

### Consultar Dados

```sql 
SELECT * FROM NomeDaTabela;

SELECT * FROM Produtos;

```

### Atualizar Dados

```sql
UPDATE NomeDaTabela
SET Email = 'novoemail@example.com'
WHERE ID = 1;

UPDATE Produtos
SET Preco = 39.99
WHERE ID = 1;


```

### Excluir Dados

```sql
DELETE FROM NomeDaTabela
WHERE ID = 3;

```

### Criar Tabela de Pedidos:

```sql
CREATE TABLE Pedidos (
    ID INT PRIMARY KEY,
    UsuarioID INT,
    ProdutoID INT,
    Quantidade INT,
    Data DATE,
    FOREIGN KEY (UsuarioID) REFERENCES Usuarios(ID),
    FOREIGN KEY (ProdutoID) REFERENCES Produtos(ID)
);

```
#  Conclusão sobre Banco de Dados Relacional
O modelo de banco de dados relacional continua a desempenhar um papel crucial no armazenamento e gerenciamento eficiente de dados estruturados. Neste contexto, observamos a criação de três tabelas essenciais: Usuários, Produtos e Pedidos, e a aplicação de operações fundamentais por meio da linguagem SQL.

O uso de tabelas relacionadas permite estabelecer conexões entre entidades, refletindo as relações do mundo real de maneira coesa e organizada. As chaves primárias e estrangeiras são empregadas para garantir integridade referencial, assegurando que as relações entre os dados sejam mantidas consistentes.

A manipulação de dados, incluindo a inserção, consulta, atualização e exclusão, é facilitada por comandos SQL. Essa linguagem fornece uma abordagem declarativa e poderosa para interagir com o banco de dados, tornando possível extrair informações específicas, realizar atualizações ou realizar análises complexas.

A flexibilidade do modelo relacional, aliada à sua capacidade de escalabilidade e integridade, faz com que seja uma escolha robusta para muitas aplicações. No entanto, é importante considerar as necessidades específicas do projeto ao escolher o tipo de banco de dados, ponderando as vantagens e desvantagens de diferentes modelos em relação aos requisitos do sistema em questão.

# Exemplos feito em aula

```sql
drop table aluno;

create table aluno (
  id integer PRIMARY KEY,
  nome VARCHAR(50), 
  cpf char(14),   
  id_End INTEGER REFERENCES endereco(id) not null
  ); 

create TABLE endereco (
  id INTEGER PRIMARY key, 
  rua VARCHAR(35), 
  cidade varchar(35), 
  estado varchar (35)
);

insert into endereco values (1, 'rua das palmeiras', 'Blumenau', 'SC')
insert into endereco values (2, 'Av. Beirra mar Norte', 'Florianópolis', 'SC');


INSERT into aluno values (1, 'Joao', '009.000.567-12', 1);
INSERT into aluno values (3, 'Joana', '009.000.567-12', 2);


select * from endereco; 
select * from aluno; 

SELECT aluno.id, 
       aluno.nome, 
       aluno.cpf, 
       endereco.id,
       endereco.rua, 
       endereco.cidade,
       endereco.estado
  from aluno, endereco
where aluno.id_end = endereco.id; 

-- DQL 
select * 
  from demo
 where id >= 2 
   and id <= 4; 
  
  
 where id BETWEEN 2 and 4;
```