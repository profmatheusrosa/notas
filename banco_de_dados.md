# Comandos SQL

| Banco de Dados | Comando SQL para Criar Tabela                                     |
| -------------- | -------------------------------------------------- |
| MySQL          | ```sql CREATE TABLE empregado (id INT AUTO_INCREMENT PRIMARY KEY, nome VARCHAR(255), departamento_id INT, FOREIGN KEY (departamento_id) REFERENCES departamento(id)); ``` |
| PostgreSQL     | ```sql CREATE TABLE empregado (id SERIAL PRIMARY KEY, nome VARCHAR(255), departamento_id INT REFERENCES departamento(id)); ``` |
| SQL Server     | ```sql CREATE TABLE empregado (id INT IDENTITY(1,1) PRIMARY KEY, nome NVARCHAR(255), departamento_id INT REFERENCES departamento(id)); ``` |
| Oracle         | ```sql CREATE TABLE empregado (id NUMBER PRIMARY KEY, nome VARCHAR2(255), departamento_id NUMBER REFERENCES departamento(id)); ``` |

| Banco de Dados | Comando SQL para Inserir Chave Primária                                      |
| -------------- | ----------------------------------------------- |
| MySQL          | ```sql ALTER TABLE empregado ADD PRIMARY KEY (cpf); ``` |
| PostgreSQL     | ```sql ALTER TABLE empregado ADD PRIMARY KEY (cpf); ``` |
| SQL Server     | ```sql ALTER TABLE empregado ADD CONSTRAINT PK_empregado_cpf PRIMARY KEY (cpf); ``` |
| Oracle         | ```sql ALTER TABLE empregado ADD CONSTRAINT PK_empregado_cpf PRIMARY KEY (cpf); ``` |

| Banco de Dados | Comando SQL para Inserir Coluna                                                      |
| -------------- | --------------------------------------------------------------- |
| MySQL          | ```sql ALTER TABLE empregado ADD COLUMN salario DECIMAL(10,2); ``` |
| PostgreSQL     | ```sql ALTER TABLE empregado ADD COLUMN salario DECIMAL(10,2); ``` |
| SQL Server     | ```sql ALTER TABLE empregado ADD salario DECIMAL(10,2); ```      |
| Oracle         | ```sql ALTER TABLE empregado ADD salario NUMBER(10,2); ```       |

| Banco de Dados | Comando SQL para Criar Usuário                  | Comando SQL para Conceder Permissões                  |
| -------------- | --------------------------------------------- | ----------------------------------------------------- |
| MySQL          | ```sql CREATE USER 'nome_usuario'@'localhost' IDENTIFIED BY 'senha'; ``` | ```sql GRANT permissao ON banco_de_dados.tabela TO 'nome_usuario'@'localhost'; ``` |
| PostgreSQL     | ```sql CREATE USER nome_usuario WITH PASSWORD 'senha'; ``` | ```sql GRANT permissao ON tabela TO nome_usuario; ``` |
| SQL Server     | ```sql CREATE LOGIN nome_usuario WITH PASSWORD = 'senha'; ``` | ```sql USE banco_de_dados; GRANT permissao ON tabela TO nome_usuario; ``` |
| Oracle         | ```sql CREATE USER nome_usuario IDENTIFIED BY senha; ``` | ```sql GRANT permissao ON tabela TO nome_usuario; ``` |
