<div style="background-color: gray;">
        <div style="margin-left: 20px; margin-right: 20px; margin-bottom: 20px;">
        <h1>Notas Bancos de Dados SQL e NOSQL</h1>
    
        <h2 style="color: black;"><u>O que é um Banco SQL?</u></h2>
    
        <p>A SQL — Structured Query Language, ou linguagem estruturada de consultas — é a linguagem padrão dos Bancos de Dados Relacionais. Eles são estruturados em tabelas em formas de colunas e linhas, também chamadas de tuplas. Banco de dados relacionais são orientados a conjuntos e é a base para manipulação dos dados relacionais.
        </p>
        <p>A linguagem SQL é classificada em 4 categorias, a saber:</p>
        
        <h4 style="color: blue;">1. DML: Data Manipulation Language</h4>
        <p>Comandos DML tratam dos dados. Eles alteram as informações em um banco de dados SQL. Os comandos mais usados, são:</p> 
        <ul>
            <li>SELECT;</li>
            <li>INSERT;</li>
            <li>DELETE;</li>
            <li>UPDATE.</li>
        </ul>
    
        <h4 style="color: blue;">2. DDL: Data Definition Language</h4>
        <p>Esses comandos criam ou alteram as estruturas das tabelas. Os comandos mais comuns são:</p>
        <ul>
            <li>CREATE;</li>
            <li>ALTER;</li>
            <li>DROP.</li>
        </ul>
    
        <h4 style="color: blue;">3. DCL: Data Control Language</h4> 
        <p>Os comandos DCL são usados pelo administrador do banco de dados para dar as permissões de acesso, conforme determinado no processo de modelagem do sistema e pelos seus gestores.</p> 
    
        <p>Seus comandos mais conhecidos que atribuem ou revogam os privilégios são: <span style="font-weight: 700">GRANT</span>  e <span style="font-weight: 700">REVOKE</span> . Esses comandos geralmente ficam sob a atribuição do DBA, como responsável pela segurança do ambiente de banco de dados SQL.</p> 
    
        <h4 style="color: blue;">4. DTL: Data Transaction Language</h4>
        <p>Esses são comandos que controlam as transações no banco de dados. A forma como um banco de dados relacional implementa a consistência de seus dados se dá por meio dessas transações.</p>
    
        <p>O isolamento das transações é baseado no seguinte princípio: ou uma alteração nos dados é concluída totalmente ou os dados devem retornar à situação original antes da mudança.</p>

        <h2 style="color: black;"><u>O que é um Banco NOSQL?</u></h2> 
        <p>Bancos de dados NoSQL são criados para modelos de dados específicos e têm esquemas flexíveis para a criação de aplicativos modernos. Os bancos de dados NoSQL são amplamente reconhecidos por sua facilidade de desenvolvimento, funcionalidade e performance em escala.</p>
        
        <h4 style="color: blue;">Como funciona um banco de dados NoSQL?</h4>
        <p>Os bancos de dados NoSQL usam uma variedade de modelos de dados para acessar e gerenciar os dados. Esses tipos de banco de dados são otimizados especificamente para aplicativos que exigem modelos de grande volume de dados, baixa latência e flexibilidade. Esses requisitos são atendidos mediante o relaxamento de algumas restrições de consistência de dados nos bancos relacionais.</p>

        <h4 style="color: blue;">Por que usar um banco de dados NoSQL?</h4>

        <p>Os bancos de dados NoSQL são ideais para muitos aplicativos modernos, como dispositivos móveis, Web e jogos. Principais vantagens dos Bancos NOSQL:</p>

        <ul >
            <li style="padding-bottom: 10px;"><span style="font-weight: 700;">Flexibilidade:</span> os bancos de dados NoSQL geralmente fornecem esquemas flexíveis que permitem um desenvolvimento mais rápido e iterativo. O modelo de dados flexível torna os bancos de dados NoSQL ideais para dados semiestruturados e não estruturados.</li>
            <li style="padding-bottom: 10px;"><span style="font-weight: 700;">Escalabilidade:</span> os bancos de dados NoSQL geralmente são projetados para serem escalados horizontalmente usando clusters distribuídos de hardware, em vez de escalá-los verticalmente adicionando servidores caros e robustos. Alguns provedores de nuvem lidam com essas operações nos bastidores como um serviço totalmente gerenciado.</li>
            <li style="padding-bottom: 10px;"><span style="font-weight: 700;">Alta performance:</span> o banco de dados NoSQL é otimizado para modelos de dados específicos e padrões de acesso que permitem maior performance do que quando se tenta realizar uma funcionalidade semelhante com bancos de dados relacionais.</li>
            <li style="padding-bottom: 10px;"><span style="font-weight: 700;">Altamente funcional:</span> os bancos de dados NoSQL fornecem APIs e tipos de dados altamente funcionais criados especificamente para cada um de seus respectivos modelos de dados.</li>
        </ul>

        <h4 style="color: blue;">Tipos de bancos de dados NoSQL</h4>

        <ul>
            <li style="padding-bottom: 10px;"><span style="font-weight: 700;">Valor principal:</span> 
                Este é o tipo mais flexível de banco de dados NoSQL porque o aplicativo tem controle total sobre o que é armazenado no campo de valor sem quaisquer restrições.</li>
            <li style="padding-bottom: 10px;"><span style="font-weight: 700;">Documento:</span> 
                Também conhecidos como armazenamento de documentos ou bancos de dados orientados a documentos, esses bancos de dados são usados para armazenar, recuperar e gerenciar dados semiestruturados. Não há necessidade de especificar quais campos um documento conterá.</li>
            <li style="padding-bottom: 10px;"><span style="font-weight: 700;">Gráfico:</span> 
                Este banco de dados organiza os dados como nós e relacionamentos, que mostram as conexões entre os nós. Isso oferece suporte a uma representação de dados mais rica e completa. Bancos de dados gráficos são aplicados em redes sociais, sistemas de reserva e detecção de fraudes.</li>
            <li style="padding-bottom: 10px;"><span style="font-weight: 700;">Coluna larga:</span>
                Esses bancos de dados armazenam e gerenciam dados na forma de tabelas, linhas e colunas. Eles são amplamente implantados em aplicativos que requerem um formato de coluna para capturar dados sem esquema.</li>
        </ul>

        <h2 style="color: black;"><u>SQL (relacional) vs. NoSQL (não relacional)</u></h2>

        <table border="1">
            <tr style="font-weight: 700; text-align: center;">
                <td>ITEM</td>
                <td>SQL</td>
                <td>NOSQL</td>
            </tr>
            <tr>
                <td>Cargas de trabalho ideais</td>
                <td>Bancos de dados relacionais são projetados para aplicativos transacionais e fortemente consistentes de processamento de transações online (OLTP) e são bons para processamento analítico online (OLAP).</td>
                <td>Os bancos de dados do NoSQL são projetados para vários padrões de acesso aos dados que incluem aplicativos de baixa latência. Os bancos de dados de pesquisa NoSQL são projetados para análise de dados semiestruturados. </td>
            </tr>

            <tr>
                <td>Modelo de dados</td>
                <td>O modelo relacional normaliza dados em tabelas, compostas por linhas e colunas. Um esquema define estritamente tabelas, colunas, índices, relações entre tabelas e outros elementos do banco de dados. O banco de dados impõe a integridade referencial nos relacionamentos entre as tabelas.</td>
                <td>Os bancos de dados NoSQL fornecem uma variedade de modelos de dados, como chave-valor, documento e gráfico, que são otimizados para performance e escala.</td>
            </tr>

            <tr>
                <td>Propriedades ACID</td>
                <td>Bancos de dados relacionais fornecem propriedades de atomicidade, consistência, isolamento e durabilidade (ACID):

                    A atomicidade exige uma transação para executar completamente ou não é executada de forma alguma.
                    A consistência exige que, quando uma transação é confirmada, os dados devem estar em conformidade com o esquema do banco de dados.
                    O isolamento exige que as transações simultâneas sejam executadas separadamente umas das outras.
                    A resiliência exige a capacidade de se recuperar de uma falha do sistema ou falta de energia inesperada para o último estado conhecido.</td>
                <td>Os bancos de dados NoSQL geralmente fazem compensações relaxando algumas das propriedades ACID dos bancos de dados relacionais para um modelo de dados mais flexível que pode ser escalado horizontalmente. Isso torna os bancos de dados NoSQL uma excelente opção para casos de uso de baixa latência e alta taxa de transferência que precisam ser escalados horizontalmente além das limitações de uma única instância.</td>
            </tr>

            <tr>
                <td>Performance</td>
                <td>A performance normalmente depende do subsistema do disco. A otimização de consultas, índices e estrutura de tabela é necessária para alcançar máxima performance.</td>
                <td>A performance geralmente é uma função do tamanho do cluster do hardware subjacente, da latência de rede e do aplicativo que faz a chamada.</td>
            </tr>

            <tr>
                <td>Escala</td>
                <td>Os bancos de dados relacionais geralmente escalam verticalmente o tamanho ao aumentar os recursos de computação do hardware, ou escalam horizontalmente o tamanho ao adicionar réplicas para cargas de trabalho somente leitura.</td>
                <td>Os bancos de dados NoSQL normalmente são particionáveis porque os padrões de acesso podem escalar horizontalmente o tamanho usando arquitetura distribuída para aumentar a taxa de transferência que fornece performance consistente em escala quase ilimitada.</td>
            </tr>

            <tr>
                <td>APIs</td>
                <td>As solicitações para armazenar e recuperar dados são comunicadas usando consultas compatíveis com uma Structured Query Language (SQL – Linguagem de consultas estruturadas). Essas consultas são analisadas e executadas pelo banco de dados relacional.</td>
                <td>APIs baseadas em objetos permitem que desenvolvedores de aplicativos armazenem e restaurem facilmente estruturas de dados. As chaves de partição permitem que os aplicativos procurem pares de chave-valor, conjuntos de colunas ou documentos semiestruturados que contenham objetos e atributos de aplicativos serializados.</td>
            </tr>
        </table>
        <cite><a href="https://aws.amazon.com/pt/nosql/#:~:text=Os%20bancos%20de%20dados%20de%20pesquisa%20NoSQL,para%20an%C3%A1lise%20de%20dados%20semiestruturados.&text=O%20modelo%20relacional%20normaliza%20dados,elementos%20do%20banco%20de%20dados.">Fonte: Amazon AWS</a></cite>

        <h2 style="color: black;"><u>Terminologia do SQL vs. do NoSQL</u></h2>
        <p>A tabela a seguir compara a terminologia usada pelos bancos de dados NoSQL selecionados com a terminologia usada pelos bancos de dados SQL.</p>

        <table border="1">
            <tr style="font-weight: 700;">
                <td>SQL</td>
                <td>MongoDB</td>
                <td>DynamoDB</td>
                <td>Cassandra </td>
            </tr>

            <tr>
                <td>Tabela</td>
                <td>Coleta</td>
                <td>Tabela</td>
                <td>Tabela</td>
            </tr>

            <tr>
                <td>Linha</td>
                <td>Documento</td>
                <td>Item</td>
                <td>Linha</td>
            </tr>

            <tr>
                <td>Coluna</td>
                <td>Campo</td>
                <td>Atributo</td>
                <td>Coluna</td>
            </tr>

            <tr>
                <td>Chave primária</td>
                <td>ObjectId</td>
                <td>Chave primária</td>
                <td>Chave primária</td>
            </tr>

            <tr>
                <td>Índice</td>
                <td>Índice</td>
                <td>Índice secundário</td>
                <td>Índice</td>
            </tr>

            <tr>
                <td>Visualização</td>
                <td>Visualização</td>
                <td>Índice secundário global</td>
                <td>Visualização materializada</td>
            </tr>

            <tr>
                <td>Tabela ou objeto aninhado</td>
                <td>Documento incorporado</td>
                <td>Mapa</td>
                <td>Mapa</td>
            </tr>

            <tr>
                <td>Matriz</td>
                <td>Matriz</td>
                <td>Lista</td>
                <td>Lista</td>
            </tr>
        </table>
        <cite><a href="https://aws.amazon.com/pt/nosql/#:~:text=Os%20bancos%20de%20dados%20de%20pesquisa%20NoSQL,para%20an%C3%A1lise%20de%20dados%20semiestruturados.&text=O%20modelo%20relacional%20normaliza%20dados,elementos%20do%20banco%20de%20dados.">Fonte: Amazon AWS</a></cite>


    </div>
</div>
