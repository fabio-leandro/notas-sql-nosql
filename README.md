<h1>Notas Bancos de Dados SQL e NOSQL</h1>

<h3>SQL</h3>

<br/>
```
function test() {
  console.log("notice the blank line before this function?");
}
```
<br/>

<p>Structured Query Language ou SQL é a linguagem mais conhecida do mundo e também a mais popular. É utilizada para executar comandos em Banco de Dados Relacionais, isto é, baseado em tabelas. É por meio dela que criamos databases, tabelas, colunas, indices, garantimos e revogamos privilégios a usuários e consultamos os dados armazenados no banco de dados.</p>

<p>SQL é uma linguagem declarativa dividida em conjuntos de comandos Data Definition Language (DDL), Data Manipulation Language (DML), Data Control Language (DCL), Transactional Control Language (TCL) e Data Query Language (DQL).</p>

<p>Comandos da linguagem SQL com PostgreSQL:</P>

<h4>DDL</h4>

<p>Linguagem de Definição de Dados ou DDL são comandos que permitem ao usuário definir as novas tabelas e os elementos que serão associados a elas. Ela é responsável pelos comandos de criação e alteração no banco de dados.</p>

<h4>CREATE</h4>

<p>Comando utilizado para criar a estrutura dos dados e tabelas.</p>
<br/>
  CREATE TABLE nome_tabela (
    id SERIAL NOT NULL,
    coluna_01 varchar(40),
    coluna_02 numeric (16,2),
    coluna_03 date
  );
<br/>

<h4>ALTER/h4>

  <p>Comando utilizado para adicionar, excluir ou modificar as colunas de uma tabela existente.</p>
  <p>ALTER TABLE nome_tabela ADD coluna_04 varchar(50);</p>

<h4>DROP</h4>

  <p>Comando utilizado para excluir estrutura de tabelas.</p>
  <p>DROP TABLE nome_tabela;</p>

  <h4>DML</h4>

<p>Linguagem de Manipulação de Dados ou DML são comandos utilizados para a recuperação, inclusão, remoção e modificação de informações em bancos de dados.​Os principais comandos DML são:</p>

  <h4>INSERT</h4>

<p>Comando utilizado para inserção de registros no banco de dados.</p>
<p>INSERT INTO nome_tabela VALUES ('valor_coluna_01','valor_coluna_02','valor_coluna_03','valor_coluna_04');</p>

<h4>UPDATE</h4>

  <p>Comando utilizado para alteração de registro no banco de dados.</p>
  <p>UPDATE  nome_tabela     SET coluna_04 = 'novo_valor_coluna_04'     WHERE id = 20;</p>

  <h4>DELETE</h4>
  
  <p>Comando utilizado para excluir registro no banco de dados.</p>
  <p>DELETE FROM nome_tabela WHERE id = 20;</p>

  <h4>DCL</h4>
  
<p>Linguagem de Controle de Dados ou DCL são comandos utilizados para controlar o acesso e gerenciar permissões de usuários no banco de dados.</P>
  <p>Os principais comandos DCL são:</P>

GRANT
​
Comando utilizado para atribuir privilégios de acesso do usuário a objetos do banco de dados.
CREATE USER nome_user WITH PASSWORD 'senha_user';
​
GRANT CONNECT ON DATABASE nome_database TO nome_user;
​
GRANT SELECT, INSERT, UPDATE, DELETE ON ALL TABLES IN SCHEMA public TO nome_user;
​

REVOKE
​
Comando utilizado para revogar privilégios de acesso do usuário a objetos do banco de dados.
REVOKE ALL
ON nome_tabela
FROM nome_user;
TCL
​
Linguagem de Controle de Transações ou TCL são comandos utilizados para gerenciar as mudanças feitas por instruções DML.
​Os principais comandos TCL são:

COMMIT
​
Comando utilizado para salvar uma transação.
INSERT INTO nome_tabela VALUES ('valor_coluna_01','valor_coluna_02','valor_coluna_03','valor_coluna_04');
COMMIT;
​

ROLLBACK
​
Comando utilizado para restaurar o banco de dados ao estado anterior desde o último COMMIT.
DELETE FROM nome_tabela WHERE id = 20;
COMMIT;
​

DQL
​
Linguagem de Consulta de Dados ou DQL utiliza-se do comando SELECT para consulta dos dados.

SELECT * FROM nome_tabela;
​
Limitar o número de linhas extraídas na consulta dos dados:

SELECT * FROM nome_tabela
LIMIT 2;
​
Filtrar as colunas na consulta dos dados:

SELECT coluna_01, coluna_02 FROM nome_tabela;
​
Renomear as colunas na consulta dos dados:

SELECT coluna_01 AS Coluna01,
       coluna_02 AS Coluna02
FROM nome_tabela;
​
Ordenar o retorno dos dados na consulta:

SELECT coluna_01
FROM nome_tabela
ORDER BY coluna_01 DESC;
​
Retornar os dados distintos de uma tabela:

SELECT DISTINCT coluna_01
FROM nome_tabela;
​
Listar todos os dados que se enquadrem em uma determinada condição:

SELECT * FROM nome_tabela
WHERE coluna_01 = 'qualquer_valor_coluna_01';
​
Listar todos os dados que se enquadrem em duas condições:

SELECT *
FROM tb_cidades
WHERE coluna_01 = 'valor_coluna_01' 
AND coluna_02 = 'valor_coluna_02'; 
​

NoSQL
​
Os bancos de dados NoSQL (ou não-relacionais) utilizam um padrão diferente de armazenamento em relação ao SQL. O grande diferencial dessa tecnologia é a capacidade de escalabilidade para as operações das empresas de uma forma mais simples e econômica do que no banco relacional.
​
O NoSQL também proporciona uma performance melhor para o gerenciamento de dados das organizações, pois não há necessidade de agrupar os dados em um esquema de tabelas para usar as informações.
​
No MongoDB, conjuntos de documentos são chamados de “Coleções” (collections). Seriam os análogos das tabelas no Postgres, com a diferença fundamental de que seus documentos não precisam respeitar um schema rígido de tabela, como nos bancos relacionais.
​
Assim como no caso dos bancos relacionais, essas coleções ficam salvas dentro de “databases” no mesmo banco.
​

Criando uma collection
Para criar uma collection, fazemos no shell:

db.createCollection('customers')
​
Para deletar uma:

db.collection.drop('customers')
​

Inserindo documentos
​
Para inserir um documento na nossa collection, fazemos:

    db.customers.insertOne(
        {
            nome: "Carlos Alberto",
            idade: 27   
        }
    )
​
Ao fazer isto, um id randômico automaticamente é criado:

    "insertedId" : ObjectId("602471311f028450f0839cdd")
​
Nada nos impede de inserir um documentos com outro formato na mesma collection:

    db.customers.insertOne(
        {
            nome: "Maria", 
            idade: 30,
            empresas: ['Facebook', 'Google']
        }
    )
​
Podemos inserir múltiplos itens simultaneamente:

    db.customers.insertMany([
        {nome: "Maria Clara"},
        {nome: "Pedro", idade: 21},
        {nome: "Joao", empresas: ['Apple', 'Samsung']}
    ])
​

Atualizando documentos
​
Para atualizar um documento (o primeiro apenas!):

    db.customers.updateOne(
        {nome: "Maria"},
        {$set: {"idade": 31}}
    )
​
O código acima atualiza a idade da primeira "Maria" que encontra para 31. Se quisermos um comportamento que estamos mais acostumados no Postgres, onde atualizamos todos os itens que se encaixam na busca, fazemos:

    db.customers.updateMany(
        {nome: "Maria"},
        {$set: {"idade": 31}}
    )
Deletando documentos
​
Como nos outros casos, há o “One” e o “Many”. Abaixo, deletamos o primeiro registro cujo nome é "Maria Clara".

    db.customers.deleteOne({nome: "Maria Clara"})
​
Para deletar todos os registros cujos nomes são “Maria Clara”, fazemos:

    db.customers.deleteMany({nome: "Maria Clara"})
​
O famoso “delete sem WHERE” é:

    db.customers.deleteMany({})
Consultas básicas
​
Para contar todos os elementos numa tabela:

    db.customers.count()
​
Para filtrar:

    db.customers.count({nome: 'Pedro'})
​
Para consultar uma coleção, no equivalente ao SQL para SELECT * FROM customers, basta fazer:

    db.customers.find()
​
As condições para a consulta vão como argumento do find(), da mesma forma que com o count():

    db.customers.find( { <condições> } )

Ex:

    db.customers.find(
        {
            $or: [{nome: 'Pedro'}, {idade: 31}]
        }
    )

