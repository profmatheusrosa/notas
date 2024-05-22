# Sumário

1. [Fundamentos de Programação em Python](#fundamentos-de-programação-em-python)
   - [Sintaxe básica](#sintaxe-básica)
   - [Tipos de dados básicos (inteiros, floats, strings)](#tipos-de-dados-básicos-inteiros-floats-strings)
   - [Operadores (aritméticos, comparação, lógicos)](#operadores-aritméticos-comparação-lógicos)
2. [Estruturas de Controle](#estruturas-de-controle)
   - [Condicionais (if, elif, else)](#condicionais-if-elif-else)
   - [Estruturas de repetição (for, while)](#estruturas-de-repetição-for-while)
   - [Controle de fluxo (break, continue, pass)](#controle-de-fluxo-break-continue-pass)
3. [Coleções de Dados](#coleções-de-dados)
   - [Listas: criação, acesso, modificação, métodos](#listas-criação-acesso-modificação-métodos)
   - [Tuplas: criação, acesso, métodos](#tuplas-criação-acesso-métodos)
   - [Dicionários: criação, acesso, modificação, métodos](#dicionários-criação-acesso-modificação-métodos)
   - [Conjuntos: criação, operações, métodos](#conjuntos-criação-operações-métodos)
4. [Funções](#funções)
   - [Definição e chamada de funções](#definição-e-chamada-de-funções)
   - [Parâmetros e argumentos](#parâmetros-e-argumentos)
   - [Retorno de valores](#retorno-de-valores)
   - [Funções anônimas (lambda)](#funções-anônimas-lambda)
   - [Escopo de variáveis (global e local)](#escopo-de-variáveis-global-e-local)
5. [Manipulação de Strings](#manipulação-de-strings)
   - [Métodos de strings (fatiamento, substituição, busca, etc.)](#métodos-de-strings-fatiamento-substituição-busca-etc)
   - [Formatação de strings (f-strings, format(), %)](#formatação-de-strings-f-strings-format)
6. [Manipulação de Arquivos](#manipulação-de-arquivos)
   - [Leitura e escrita em arquivos](#leitura-e-escrita-em-arquivos)
   - [Manipulação de arquivos de texto e binários](#manipulação-de-arquivos-de-texto-e-binários)
   - [Uso de context managers (with)](#uso-de-context-managers-with)
7. [Estruturas de Dados Avançadas](#estruturas-de-dados-avançadas)
   - [Compreensão de listas](#compreensão-de-listas)
   - [Compreensão de dicionários](#compreensão-de-dicionários)
   - [Compreensão de conjuntos](#compreensão-de-conjuntos)
8. [Programação Orientada a Objetos (POO)](#programação-orientada-a-objetos-poo)
   - [Classes e objetos](#classes-e-objetos)
   - [Atributos e métodos](#atributos-e-métodos)
   - [Herança e polimorfismo](#herança-e-polimorfismo)
   - [Encapsulamento e abstração](#encapsulamento-e-abstração)
9. [Módulos e Pacotes](#módulos-e-pacotes)
   - [Importação de módulos (import, from ... import)](#importação-de-módulos-import-from--import)
   - [Criação de módulos e pacotes próprios](#criação-de-módulos-e-pacotes-próprios)
   - [Uso de bibliotecas padrão do Python (os, sys, math, datetime, etc.)](#uso-de-bibliotecas-padrão-do-python-os-sys-math-datetime-etc)
10. [Tratamento de Exceções](#tratamento-de-exceções)
    - [Captura e tratamento de exceções (try, except, finally)](#captura-e-tratamento-de-exceções-try-except-finally)
    - [Criação de exceções personalizadas](#criação-de-exceções-personalizadas)
11. [Programação Funcional](#programação-funcional)
    - [Funções de ordem superior (map, filter, reduce)](#funções-de-ordem-superior-map-filter-reduce)
    - [Expressões geradoras](#expressões-geradoras)
    - [Decoradores](#decoradores)




# Coleções de Dados

## Listas
As listas são coleções ordenadas e mutáveis de itens. Elas podem conter elementos de diferentes tipos (inteiros, strings, etc.) e permitem a modificação de seus elementos após a criação. 

Exemplo de criação de lista:
```python
lista = [1, 2, 3, "quatro", 5.0]
```

## Tuplas
As tuplas são coleções ordenadas e imutáveis de itens. Elas são semelhantes às listas, mas, uma vez criadas, seus elementos não podem ser modificados.

Exemplo de criação de tupla:
```python
Copiar código
tupla = (1, 2, 3, "quatro", 5.0)
```

## Dicionários
Os dicionários em Python são coleções de pares chave-valor, onde cada chave é única e mapeia para um valor específico. Eles são extremamente úteis para armazenar e acessar dados de forma eficiente, especialmente quando a associação entre diferentes tipos de dados é necessária.

### Características dos Dicionários
* Chaves Únicas: Cada chave em um dicionário deve ser única. Se uma chave for repetida, o valor associado a ela será sobrescrito.
* Acessos Rápidos: Os dicionários são implementados como tabelas de hash, permitindo acessos rápidos aos valores.
* Mutáveis: Os dicionários podem ser alterados após sua criação. É possível adicionar, modificar ou remover pares chave-valor.
* Tipos de Dados: As chaves devem ser de um tipo de dado imutável, como strings, números ou tuplas, enquanto os valores podem ser de qualquer tipo.

### Criando um Dicionário
Para criar um dicionário, utiliza-se a sintaxe de chaves {} ou a função dict().
```python
# Criando um dicionário vazio
meu_dicionario = {}

# Criando um dicionário com pares chave-valor
contatos = {
    "Alice": "alice@example.com",
    "Bob": "bob@example.com",
    "Carol": "carol@example.com"
}
```
### Acessando e Modificando Valores
Os valores podem ser acessados utilizando as chaves entre colchetes [].

```python
# Acessando um valor
email_alice = contatos["Alice"]
print(email_alice)  # Output: alice@example.com

# Modificando um valor
contatos["Alice"] = "novo_email_alice@example.com"
```
### Funções Principais
| Comando/ Método                     | Explicação                                                                                         | Exemplo                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| `d[key]`                            | Acessa o valor associado à `key`.                                                                  | `email_alice = contatos["Alice"]`                              |
| `d[key] = value`                    | Adiciona ou atualiza o par `key: value` no dicionário.                                             | `contatos["Alice"] = "novo_email@example.com"`                 |
| `del d[key]`                        | Remove o par `key: value` do dicionário.                                                           | `del contatos["Alice"]`                                        |
| `len(d)`                            | Retorna o número de pares chave-valor no dicionário.                                               | `num_contatos = len(contatos)`                                 |
| `d.keys()`                          | Retorna uma visão das chaves do dicionário.                                                        | `chaves = contatos.keys()`                                     |
| `d.values()`                        | Retorna uma visão dos valores do dicionário.                                                       | `valores = contatos.values()`                                  |
| `d.items()`                         | Retorna uma visão dos pares chave-valor do dicionário.                                             | `pares = contatos.items()`                                     |
| `d.get(key, default=None)`          | Retorna o valor para `key` se `key` estiver no dicionário, senão retorna `default`.                | `email = contatos.get("Alice", "email_nao_encontrado")`        |
| `d.pop(key, default=None)`          | Remove e retorna o valor para `key`. Se `key` não estiver presente, retorna `default` (opcional).  | `email = contatos.pop("Alice", "email_nao_encontrado")`        |
| `d.update(other_dict)`              | Atualiza o dicionário com pares chave-valor de `other_dict`.                                       | `contatos.update({"Eve": "eve@example.com"})`                  |
| `d.clear()`                         | Remove todos os itens do dicionário.                                                               | `contatos.clear()`                                             |
| `key in d`                          | Retorna `True` se `key` estiver no dicionário, senão retorna `False`.                              | `existe = "Alice" in contatos`                                 |
| `d.setdefault(key, default=None)`   | Retorna o valor para `key` se `key` estiver no dicionário. Senão, insere `key` com `default`.      | `contatos.setdefault("Eve", "eve@example.com")`                |
| `d.copy()`                          | Retorna uma cópia rasa do dicionário.                                                              | `contatos_copia = contatos.copy()`                             |
| `dict.fromkeys(seq, value=None)`    | Cria um novo dicionário com chaves de `seq` e valores iguais a `value`.                            | `novo_dict = dict.fromkeys(["Alice", "Bob"], "email_padrao")`  |


## Conjuntos
