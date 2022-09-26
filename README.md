<dNotas Bancos de Dados SQL e NOSQL
=================================

O que é um Banco SQL?
---------------------

A SQL — Structured Query Language, ou linguagem estruturada de consultas — é a linguagem padrão dos Bancos de Dados Relacionais. Eles são estruturados em tabelas em formas de colunas e linhas, também chamadas de tuplas. Banco de dados relacionais são orientados a conjuntos e é a base para manipulação dos dados relacionais.

A linguagem SQL é classificada em 4 categorias, a saber:

#### 1\. DML: Data Manipulation Language

Comandos DML tratam dos dados. Eles alteram as informações em um banco de dados SQL. Os comandos mais usados, são:

*   SELECT;
*   INSERT;
*   DELETE;
*   UPDATE.

#### 2\. DDL: Data Definition Language

Esses comandos criam ou alteram as estruturas das tabelas. Os comandos mais comuns são:

*   CREATE;
*   ALTER;
*   DROP.

#### 3\. DCL: Data Control Language

Os comandos DCL são usados pelo administrador do banco de dados para dar as permissões de acesso, conforme determinado no processo de modelagem do sistema e pelos seus gestores.

Seus comandos mais conhecidos que atribuem ou revogam os privilégios são: GRANT e REVOKE . Esses comandos geralmente ficam sob a atribuição do DBA, como responsável pela segurança do ambiente de banco de dados SQL.

#### 4\. DTL: Data Transaction Language

Esses são comandos que controlam as transações no banco de dados. A forma como um banco de dados relacional implementa a consistência de seus dados se dá por meio dessas transações.

O isolamento das transações é baseado no seguinte princípio: ou uma alteração nos dados é concluída totalmente ou os dados devem retornar à situação original antes da mudança.

O que é um Banco NOSQL?
-----------------------

Bancos de dados NoSQL são criados para modelos de dados específicos e têm esquemas flexíveis para a criação de aplicativos modernos. Os bancos de dados NoSQL são amplamente reconhecidos por sua facilidade de desenvolvimento, funcionalidade e performance em escala.

#### Como funciona um banco de dados NoSQL?

Os bancos de dados NoSQL usam uma variedade de modelos de dados para acessar e gerenciar os dados. Esses tipos de banco de dados são otimizados especificamente para aplicativos que exigem modelos de grande volume de dados, baixa latência e flexibilidade. Esses requisitos são atendidos mediante o relaxamento de algumas restrições de consistência de dados nos bancos relacionais.

#### Por que usar um banco de dados NoSQL?

Os bancos de dados NoSQL são ideais para muitos aplicativos modernos, como dispositivos móveis, Web e jogos. Principais vantagens dos Bancos NOSQL:

*   Flexibilidade: os bancos de dados NoSQL geralmente fornecem esquemas flexíveis que permitem um desenvolvimento mais rápido e iterativo. O modelo de dados flexível torna os bancos de dados NoSQL ideais para dados semiestruturados e não estruturados.
*   Escalabilidade: os bancos de dados NoSQL geralmente são projetados para serem escalados horizontalmente usando clusters distribuídos de hardware, em vez de escalá-los verticalmente adicionando servidores caros e robustos. Alguns provedores de nuvem lidam com essas operações nos bastidores como um serviço totalmente gerenciado.
*   Alta performance: o banco de dados NoSQL é otimizado para modelos de dados específicos e padrões de acesso que permitem maior performance do que quando se tenta realizar uma funcionalidade semelhante com bancos de dados relacionais.
*   Altamente funcional: os bancos de dados NoSQL fornecem APIs e tipos de dados altamente funcionais criados especificamente para cada um de seus respectivos modelos de dados.

#### Tipos de bancos de dados NoSQL

*   Valor principal: Este é o tipo mais flexível de banco de dados NoSQL porque o aplicativo tem controle total sobre o que é armazenado no campo de valor sem quaisquer restrições.
*   Documento: Também conhecidos como armazenamento de documentos ou bancos de dados orientados a documentos, esses bancos de dados são usados para armazenar, recuperar e gerenciar dados semiestruturados. Não há necessidade de especificar quais campos um documento conterá.
*   Gráfico: Este banco de dados organiza os dados como nós e relacionamentos, que mostram as conexões entre os nós. Isso oferece suporte a uma representação de dados mais rica e completa. Bancos de dados gráficos são aplicados em redes sociais, sistemas de reserva e detecção de fraudes.
*   Coluna larga: Esses bancos de dados armazenam e gerenciam dados na forma de tabelas, linhas e colunas. Eles são amplamente implantados em aplicativos que requerem um formato de coluna para capturar dados sem esquema.

SQL (relacional) vs. NoSQL (não relacional)
-------------------------------------------

ITEM

SQL

NOSQL

Cargas de trabalho ideais

Bancos de dados relacionais são projetados para aplicativos transacionais e fortemente consistentes de processamento de transações online (OLTP) e são bons para processamento analítico online (OLAP).

Os bancos de dados do NoSQL são projetados para vários padrões de acesso aos dados que incluem aplicativos de baixa latência. Os bancos de dados de pesquisa NoSQL são projetados para análise de dados semiestruturados.

Modelo de dados

O modelo relacional normaliza dados em tabelas, compostas por linhas e colunas. Um esquema define estritamente tabelas, colunas, índices, relações entre tabelas e outros elementos do banco de dados. O banco de dados impõe a integridade referencial nos relacionamentos entre as tabelas.

Os bancos de dados NoSQL fornecem uma variedade de modelos de dados, como chave-valor, documento e gráfico, que são otimizados para performance e escala.

Propriedades ACID

Bancos de dados relacionais fornecem propriedades de atomicidade, consistência, isolamento e durabilidade (ACID): A atomicidade exige uma transação para executar completamente ou não é executada de forma alguma. A consistência exige que, quando uma transação é confirmada, os dados devem estar em conformidade com o esquema do banco de dados. O isolamento exige que as transações simultâneas sejam executadas separadamente umas das outras. A resiliência exige a capacidade de se recuperar de uma falha do sistema ou falta de energia inesperada para o último estado conhecido.

Os bancos de dados NoSQL geralmente fazem compensações relaxando algumas das propriedades ACID dos bancos de dados relacionais para um modelo de dados mais flexível que pode ser escalado horizontalmente. Isso torna os bancos de dados NoSQL uma excelente opção para casos de uso de baixa latência e alta taxa de transferência que precisam ser escalados horizontalmente além das limitações de uma única instância.

Performance

A performance normalmente depende do subsistema do disco. A otimização de consultas, índices e estrutura de tabela é necessária para alcançar máxima performance.

A performance geralmente é uma função do tamanho do cluster do hardware subjacente, da latência de rede e do aplicativo que faz a chamada.

Escala

Os bancos de dados relacionais geralmente escalam verticalmente o tamanho ao aumentar os recursos de computação do hardware, ou escalam horizontalmente o tamanho ao adicionar réplicas para cargas de trabalho somente leitura.

Os bancos de dados NoSQL normalmente são particionáveis porque os padrões de acesso podem escalar horizontalmente o tamanho usando arquitetura distribuída para aumentar a taxa de transferência que fornece performance consistente em escala quase ilimitada.

APIs

As solicitações para armazenar e recuperar dados são comunicadas usando consultas compatíveis com uma Structured Query Language (SQL – Linguagem de consultas estruturadas). Essas consultas são analisadas e executadas pelo banco de dados relacional.

APIs baseadas em objetos permitem que desenvolvedores de aplicativos armazenem e restaurem facilmente estruturas de dados. As chaves de partição permitem que os aplicativos procurem pares de chave-valor, conjuntos de colunas ou documentos semiestruturados que contenham objetos e atributos de aplicativos serializados.

[Fonte: Amazon AWS](https://aws.amazon.com/pt/nosql/#:~:text=Os%20bancos%20de%20dados%20de%20pesquisa%20NoSQL,para%20an%C3%A1lise%20de%20dados%20semiestruturados.&text=O%20modelo%20relacional%20normaliza%20dados,elementos%20do%20banco%20de%20dados.)

Terminologia do SQL vs. do NoSQL
--------------------------------

A tabela a seguir compara a terminologia usada pelos bancos de dados NoSQL selecionados com a terminologia usada pelos bancos de dados SQL.

SQL

MongoDB

DynamoDB

Cassandra

Tabela

Coleta

Tabela

Tabela

Linha

Documento

Item

Linha

Coluna

Campo

Atributo

Coluna

Chave primária

ObjectId

Chave primária

Chave primária

Índice

Índice

Índice secundário

Índice

Visualização

Visualização

Índice secundário global

Visualização materializada

Tabela ou objeto aninhado

Documento incorporado

Mapa

Mapa

Matriz

Matriz

Lista

Lista

[Fonte: Amazon AWS](https://aws.amazon.com/pt/nosql/#:~:text=Os%20bancos%20de%20dados%20de%20pesquisa%20NoSQL,para%20an%C3%A1lise%20de%20dados%20semiestruturados.&text=O%20modelo%20relacional%20normaliza%20dados,elementos%20do%20banco%20de%20dados.)
