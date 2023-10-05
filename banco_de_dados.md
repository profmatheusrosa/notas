# Comandos SQL

| Banco de Dados | Comando SQL                                         |
| -------------- | -------------------------------------------------- |
| MySQL          | ```sql CREATE TABLE empregado (id INT AUTO_INCREMENT PRIMARY KEY, nome VARCHAR(255), departamento_id INT, FOREIGN KEY (departamento_id) REFERENCES departamento(id)); ``` |
| PostgreSQL     | ```sql CREATE TABLE empregado (id SERIAL PRIMARY KEY, nome VARCHAR(255), departamento_id INT REFERENCES departamento(id)); ``` |
| SQL Server     | ```sql CREATE TABLE empregado (id INT IDENTITY(1,1) PRIMARY KEY, nome NVARCHAR(255), departamento_id INT REFERENCES departamento(id)); ``` |
| Oracle         | ```sql CREATE TABLE empregado (id NUMBER PRIMARY KEY, nome VARCHAR2(255), departamento_id NUMBER REFERENCES departamento(id)); ``` |
