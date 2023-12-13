# Sumário
- [Introdução](#introducao)
- [Comandos ANSI](#comandos-ansi)
- [Comandos DDL (Data Definition Language)](#Comandos-DDL-(Data-Definition-Language))

### Introdução

# Comandos 

| Banco de Dados | Comando  para Criar Tabela                                     |
| -------------- | -------------------------------------------------- |
| MySQL          | ` CREATE TABLE empregado (id INT AUTO_INCREMENT PRIMARY KEY, nome VARCHAR(255), departamento_id INT, FOREIGN KEY (departamento_id) REFERENCES departamento(id)); ` |
| Postgre     | ` CREATE TABLE empregado (id SERIAL PRIMARY KEY, nome VARCHAR(255), departamento_id INT REFERENCES departamento(id)); ` |
| SQL Server     | ` CREATE TABLE empregado (id INT IDENTITY(1,1) PRIMARY KEY, nome NVARCHAR(255), departamento_id INT REFERENCES departamento(id)); ` |
| Oracle         | ` CREATE TABLE empregado (id NUMBER GENERATED ALWAYS AS IDENTITY PRIMARY KEY, nome VARCHAR2(255), departamento_id NUMBER REFERENCES departamento(id)); ` |

| Banco de Dados | Comando  para Inserir Chave Primária                                      | Comando  para Remover Chave Primária                                  |
| -------------- | ----------------------------------------------- | ----------------------------------------------------------------------- |
| MySQL          | ` ALTER TABLE empregado ADD PRIMARY KEY (cpf); ` | ` ALTER TABLE nome_tabela DROP PRIMARY KEY; `                    |
| Postgre     | ` ALTER TABLE empregado ADD PRIMARY KEY (cpf); ` | ` ALTER TABLE nome_tabela DROP CONSTRAINT nome_chave_primaria; ` |
| SQL Server     | ` ALTER TABLE empregado ADD CONSTRAINT PK_empregado_cpf PRIMARY KEY (cpf); ` | ` ALTER TABLE nome_tabela DROP CONSTRAINT nome_chave_primaria; ` |
| Oracle         | ` ALTER TABLE empregado ADD CONSTRAINT PK_empregado_cpf PRIMARY KEY (cpf); ` | ` ALTER TABLE nome_tabela DROP PRIMARY KEY; `                    |


| Banco de Dados | Comando  para Inserir Coluna | Comando  para Excluir Coluna                                                       | Comando  para Modificar Coluna                       |
| -------------- | --------------------------------------------- | ----------------------------------------------------- | ------------------------------------------------------ |
| MySQL          | ` ALTER TABLE empregado ADD COLUMN salario DECIMAL(10,2); ` | ` ALTER TABLE nome_tabela DROP COLUMN nome_coluna; ` | ` ALTER TABLE nome_tabela MODIFY nome_coluna novo_tipo; ` |
| Postgre     | ` ALTER TABLE empregado ADD COLUMN salario DECIMAL(10,2); ` | ` ALTER TABLE nome_tabela DROP COLUMN nome_coluna; ` | ` ALTER TABLE nome_tabela ALTER COLUMN nome_coluna TYPE novo_tipo; ` |
| SQL Server     | ` ALTER TABLE empregado ADD salario DECIMAL(10,2); `      | ` ALTER TABLE nome_tabela DROP COLUMN nome_coluna; ` | ` ALTER TABLE nome_tabela ALTER COLUMN nome_coluna novo_tipo; ` |
| Oracle         | ` ALTER TABLE empregado ADD salario NUMBER(10,2); `       | ` ALTER TABLE nome_tabela DROP COLUMN nome_coluna; ` | ` ALTER TABLE nome_tabela MODIFY nome_coluna novo_tipo; ` |


| Banco de Dados | Comando  para Adicionar Restrição                             | Comando  para Remover Restrição                                      |
| -------------- | -------------------------------------------------------------- | ----------------------------------------------------------------------- |
| MySQL, Postgre, SQL Server, Oracle           | ` ALTER TABLE nome_tabela ADD CONSTRAINT nome_restrição CHECK (condição); ` | ` ALTER TABLE nome_tabela DROP CONSTRAINT nome_restrição; `      |

| Banco de Dados | Comando  para Criar Usuário                  | Comando  para Conceder Permissões                  |
| -------------- | --------------------------------------------- | ----------------------------------------------------- |
| MySQL          | ` CREATE USER 'nome_usuario'@'localhost' IDENTIFIED BY 'senha'; ` | ` GRANT permissao ON banco_de_dados.tabela TO 'nome_usuario'@'localhost'; ` |
| Postgre     | ` CREATE USER nome_usuario WITH PASSWORD 'senha'; ` | ` GRANT permissao ON tabela TO nome_usuario; ` |
| SQL Server     | ` CREATE LOGIN nome_usuario WITH PASSWORD = 'senha'; ` | ` USE banco_de_dados; GRANT permissao ON tabela TO nome_usuario; ` |
| Oracle         | ` CREATE USER nome_usuario IDENTIFIED BY senha; ` | ` GRANT permissao ON tabela TO nome_usuario; ` |

| Banco de Dados | Comando  para Criar Índices                                     |
| -------------- | ------------------------------------------------------------------ |
| MySQL, Postgre, SQL Server, Oracle        | ` CREATE INDEX nome_indice ON nome_tabela (nome_coluna); `   |

| Banco de Dados | Comando  para Excluir Todos os Registros         |
| -------------- | --------------------------------------- |
| MySQL, Postgre, SQL Server, Oracle         | `TRUNCATE TABLE nome_tabela; `   |

### Manipulação de Strings 
| Comando           | MySQL                                 | PostgreSQL                                      | SQL Server                                    |
| ----------------- | --------------------------------------| ----------------------------------------------- | --------------------------------------------- |
| **Concatenação**  | `CONCAT(string1, string2)`            | ```string1 \|\| string2```                           | `string1 + string2`                            |
| **Comprimento**   | `LENGTH(string)` ou `CHAR_LENGTH(string)`| `LENGTH(string)` ou `CHAR_LENGTH(string)`   | `LEN(string)` ou `DATALENGTH(string)`         |
| **Substring**     | `SUBSTRING(string FROM start FOR length)` | `SUBSTRING(string FROM start FOR length)`  | `SUBSTRING(string, start, length)`            |
| **Uppercase**     | `UPPER(string)`                       | `UPPER(string)`                                | `UPPER(string)`                               |
| **Lowercase**     | `LOWER(string)`                       | `LOWER(string)`                                | `LOWER(string)`                               |
| **Trim**          | `TRIM([leading\|trailing\|both] characters FROM string)` | `TRIM([leading\|trailing\|both] characters FROM string)` | `LTRIM(RTRIM(string))`                        |
| **Replace**       | `REPLACE(string, search, replacement)` | `REPLACE(string, search, replacement)`         | `REPLACE(string, search, replacement)`        |
| **Posição**       | `POSITION(substring IN string)`       | `POSITION(substring IN string)`                | `CHARINDEX(substring, string)`                |
| **Formatar Data** | `DATE_FORMAT(date, format)`            | `TO_CHAR(date, format)`                        | `FORMAT(date, format)`                        |


# Comandos  ANSI
## Comandos DML (Data Manipulation Language)
| Comando DML SQL ANSI  | Exemplo do Comando                                     |
| ---------------- | ------------------------------------------------------ |
| `SELECT`         | `SELECT coluna FROM tabela WHERE condição;`           |
| `INSERT`         | `INSERT INTO tabela (coluna1, coluna2) VALUES (valor1, valor2);` |
| `UPDATE`         | `UPDATE tabela SET coluna = novo_valor WHERE condição;` |
| `DELETE`         | `DELETE FROM tabela WHERE condição;`                   |
| `FROM`           | `SELECT coluna FROM tabela;`                           |
| `WHERE`          | `SELECT coluna FROM tabela WHERE condição;`           |
| `GROUP BY`       | `SELECT coluna, COUNT(*) FROM tabela GROUP BY coluna;` |
| `HAVING`         | `SELECT coluna, COUNT(*) FROM tabela GROUP BY coluna HAVING COUNT(*) > 1;` |
| `ORDER BY`       | `SELECT coluna FROM tabela ORDER BY coluna ASC;`       |
| `DISTINCT`       | `SELECT DISTINCT coluna FROM tabela;`                  |
| `JOIN`           | `SELECT tabela1.coluna, tabela2.coluna FROM tabela1 JOIN tabela2 ON tabela1.chave = tabela2.chave;` |
| `UNION`          | `SELECT coluna FROM tabela1 UNION SELECT coluna FROM tabela2;` |
| `INSERT INTO`    | `INSERT INTO tabela (coluna1, coluna2) VALUES (valor1, valor2);` |
| `VALUES`         | `INSERT INTO tabela (coluna1, coluna2) VALUES (valor1, valor2);` |
| `UPDATE SET`     | `UPDATE tabela SET coluna = novo_valor WHERE condição;` |
| `DELETE FROM`    | `DELETE FROM tabela WHERE condição;`                   |

## Comandos DDL (Data Definition Language)
| Comando DDL SQL ANSI | Exemplo do Comando                                     |
| ---------------- | ------------------------------------------------------ |
| `CREATE TABLE`   | `CREATE TABLE nome_tabela (coluna1 tipo1, coluna2 tipo2, PRIMARY KEY (coluna1));` |
| `ALTER TABLE`    | `ALTER TABLE nome_tabela ADD COLUMN nova_coluna tipo;` |
| `DROP TABLE`     | `DROP TABLE nome_tabela;`                              |
| `CREATE INDEX`   | `CREATE INDEX nome_indice ON nome_tabela (coluna);`    |
| `DROP INDEX`     | `DROP INDEX nome_indice;`                              |
| `CREATE VIEW`    | `CREATE VIEW nome_view AS SELECT coluna FROM nome_tabela WHERE condição;` |
| `DROP VIEW`      | `DROP VIEW nome_view;`                                |
| `CREATE DATABASE`| `CREATE DATABASE nome_banco;`                          |
| `ALTER DATABASE` | `ALTER DATABASE nome_banco MODIFY nome_coluna tipo;`   |
| `DROP DATABASE`  | `DROP DATABASE nome_banco;`                            |

## Comandos DTL (Data Transaction Language)
| Comando DTL SQL ANSI | Exemplo do Comando                                     |
| ---------------- | ------------------------------------------------------ |
| `COMMIT`         | `COMMIT;`                                              |
| `ROLLBACK`       | `ROLLBACK;`                                            |
| `SAVEPOINT`      | `SAVEPOINT nome_savepoint;`                            |
| `ROLLBACK TO`    | `ROLLBACK TO nome_savepoint;`                          |
| `RELEASE SAVEPOINT` | `RELEASE SAVEPOINT nome_savepoint;`                  |

## Comandos DCL (Data Control Language)
| Comando DCL SQL ANSI  | Exemplo do Comando                                       |
| ---------------- | -------------------------------------------------------- |
| `GRANT`          | `GRANT tipo_privilégio ON objeto TO usuário;`            |
| `REVOKE`         | `REVOKE tipo_privilégio ON objeto FROM usuário;`         |

