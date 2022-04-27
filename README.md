# Desafio-de-Projeto-DIO
Tipos de Comandos SQL

## DQL: Linguagem de Consulta de Dados

### Definição:
As instruções SELECT permitem consultar o banco de dados para localizar informações em uma ou mais tabelas e retornar à consulta como um conjunto de resultados.

#### SELECT
É usado para recuperar dados do banco de dados.

##### Sintaxe:
SELECT * FROM table_name

Exemplo:
SELECT *

FROM Supplier

WHERE Country = "Italy"

## DML: Linguagem de Manipulação de Dados

### Definição:
Permitem aos usuários manipular dados em um banco de dados.

#### INSERT
É uma forma de inserir dados em uma tabela.

##### Sintaxe:
INSERT INTO TABLE_NAME

VALUES(value1,value2,value3,......,valueN);

Exemplo:
INSERT INTO javatpoint(Author,Subject) VALUES("Sonoo","DBMS");

#### UPTADE
Para atualizar um registro em uma tabela,se utiliza a instrução UPTADE.

##### Sintaxe:
UPDATE table_name SET [column_name1=value1,....column_nameN=valueN][WHERE CONDITION]

Exemplo:
UPTADE students

SET User_name = "Sonoo"

WHERE Student_Id= "3"

#### DELETE
Pode remover todas as linhas de uma tabela (usando *) ou pode ser usado como parte de uma cláusula Where para excluir linhas que atendam a uma condição específica.

##### Sintaxe:
DELETE FROM table_name [WHERE CONDITION];

Exemplo:
DELETE FROM javatpoint

WHERE Author="Sonoo";

## DDL: Linguagem de Definição de Dados

### Definição:
Permite aos usuários especificar um esquema de banco de dados através de um conjunto de definicões.

#### CREATE
Utilizado pra criar banco de dados, tabelas, store procedures, entre outros.

##### Sintaxe:
CREATE TABLE TABLE_NAME (COLUMN_NAME DATATYPES[,.....]);

Exemplo:
CREATE TABLE EMPLOYEE(Name VARCHAR2(20), Email VARCHAR(100), DOB DATE);

#### ALTER
Faz modificações em objetos criados com o create, como inserir ou remover uma nova coluna em uma tabela.

##### Sintaxe:
ALTER TABLE table_name ADD column_name COLUMN-definition;

Exemplo:
ALTER TABLE table_name MODIFY(column_definitions....);

#### DROP
Remove o que foi criado com o create.

##### Sintaxe:
DROP TABLE table_name;

Exemplo:
DROP TABLE EMPLOYEE;

## DCL: Linguagem de Controle de Dados

### Definição:
DCL inclui comandos como GRANT e REVOKE que lidam principalmente com os direitos, permissões e outros controles do sistema de banco de dados.

#### GRANT
Concede aos usuários privilégios de acesso ao banco de dados.

##### Sintaxe:
GRANT {lista_privilégios | ALL PRIVILEGES}

ON {relação | visão}

TO {lista_usuários | PUBLIC}

Exemplo:
GRANT SELECT, UPDTADE ON MY_TABLE TO SOME_USER, ANOTHER_USER;

#### REVOKE
Retira os privilégios de acesso do usuário dados usando o comando GRANT.

##### Sintaxe:
REVOKE {lista_privilégios | ALL PRIVILEGES}

ON {relação | visão}

FROM {lista_usuários | PUBLIC}

Exemplo:
REVOKE SELECT, UPDTADE ON MY_TABLE FROM USER1,USER2;

## DTL: Linguagem de Transação de Dados

### Definição:
Os comandos DTL são usados para gerenciar transações no banco de dados.

#### COMMIT
Confirma uma transação.

##### Sintaxe:
COMMIT;

Exemplo:
DELETE FROM CUSTOMERS

WHERE AGE = 25;

COMMIT;


#### ROLLBACK
Reverte uma transação no caso de ocorrer algum erro.

##### Sintaxe:
ROLLBACK;

Exemplo:
DELETE FROM CUSTOMERS;

WHERE AGE = 25;

ROLLBACK;

#### BEGIN
Marca o ponto inicial de uma transação local explícita.

##### Sintaxe:
BEGIN { TRAN | TRANSACTION }

Exemplo:
BEGIN TRANSACTION;

DELETE FROM HumanResources.JobCandidate

  WHERE JobCandidateID = 13;
COMMIT;
