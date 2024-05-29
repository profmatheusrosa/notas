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
   - [Formatação de Strings](#formatação-de-strings)
   - [Métodos Comuns](#métodos-comuns)
6. [Manipulação de Arquivos](#manipulação-de-arquivos)
   - [Leitura e escrita em arquivos](#leitura-e-escrita-em-arquivos)
   - [Manipulação de arquivos de texto e binários](#manipulação-de-arquivos-de-texto-e-binários)
   - [Uso de context managers (with)](#uso-de-context-managers-with)
7. [Estruturas de Dados Avançadas](#estruturas-de-dados-avançadas)
   - [Compreensão de listas](#compreensão-de-listas)
   - [Compreensão de dicionários](#compreensão-de-dicionários)
   - [Compreensão de conjuntos](#compreensão-de-conjuntos)
8. [Programação Orientada a Objetos (POO)](#programação-orientada-a-objetos-poo)
   - [Princípios Fundamentais da POO](#principios-fundamentais-da-poo)
   - [Classes e objetos](#classes-e-objetos)
   - [Métodos e atributos](#atributos-e-métodos)
   - [Métodos Especiais](#métodos-especiais)
   - [Herança e polimorfismo](#herança-e-polimorfismo)
   - [Encapsulamento e abstração](#encapsulamento-e-abstração)
10. [Módulos e Pacotes](#módulos-e-pacotes)
   - [Importação de módulos (import, from ... import)](#importação-de-módulos-import-from--import)
   - [Criação de módulos e pacotes próprios](#criação-de-módulos-e-pacotes-próprios)
   - [Uso de bibliotecas padrão do Python (os, sys, math, datetime, etc.)](#uso-de-bibliotecas-padrão-do-python-os-sys-math-datetime-etc)
11. [Tratamento de Exceções](#tratamento-de-exceções)
    - [Captura e tratamento de exceções (try, except, finally)](#captura-e-tratamento-de-exceções-try-except-finally)
    - [Criação de exceções personalizadas](#criação-de-exceções-personalizadas)
12. [Programação Funcional](#programação-funcional)
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

Conjuntos (sets) são coleções não ordenadas de elementos únicos, o que significa que cada elemento aparece apenas uma vez em um conjunto. Eles são úteis para operações que envolvem matemática de conjuntos, como união, interseção e diferença. Conjuntos são definidos usando chaves {} ou a função set().

### Características dos conjuntos:

* Elementos Únicos: Não permitem elementos duplicados. Cada elemento aparece apenas uma vez.
* Não Ordenados: Não mantêm a ordem dos elementos. A ordem de iteração não é garantida.
* Mutáveis: Podem ser modificados após a criação. É possível adicionar e remover elementos.
* Imutabilidade dos Elementos: Os elementos de um conjunto devem ser imutáveis (por exemplo, inteiros, strings, tuplas). Não é possível usar listas ou outros conjuntos como elementos de um conjunto.
* Eficiência em Operações de Associação: Operações de verificação de associação (como in e not in) são rápidas devido à implementação baseada em tabelas de hash.
* Operações Matemáticas: Suportam operações matemáticas de conjuntos, como união, interseção, diferença e diferença simétrica.
* Métodos e Funções Ricos: Possuem um conjunto abrangente de métodos, como `add(), remove(), discard(), union(), intersection(), difference(), symmetric_difference(), issubset(), issuperset(), isdisjoint(), copy(), clear()`, entre outros.
* Versatilidade: Conjuntos são úteis em diversas aplicações, como eliminação de duplicatas, verificações rápidas de associação, operações matemáticas de conjuntos, etc.

### Criação de um conjunto
```python
# Criando conjuntos
conjunto1 = {1, 2, 3, 4}
conjunto2 = set([3, 4, 5, 6])

print(conjunto1)  # Saída: {1, 2, 3, 4}
print(conjunto2)  # Saída: {3, 4, 5, 6}
```

### Funções Principais
| Função/Método                | Descrição                                                                                      | Exemplo                                                                 |
|------------------------------|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| `.add(elem)`                  | Adiciona um elemento ao conjunto. Se o elemento já estiver presente, nada acontece.            | `conjunto.add(4)`                                                      |
| `.remove(elem)`               | Remove um elemento do conjunto. Levanta um erro `KeyError` se o elemento não estiver presente. | `conjunto.remove(2)`                                                   |
| `.discard(elem)`              | Remove um elemento do conjunto. Não levanta erro se o elemento não estiver presente.           | `conjunto.discard(3)`                                                  |
| `.union(other)`               | Retorna a união de dois conjuntos.                                                             | `conjunto1 | conjunto2` ou `conjunto1.union(conjunto2)`                  |
| `.intersection(other)`        | Retorna a interseção de dois conjuntos.                                                        | `conjunto1 & conjunto2` ou `conjunto1.intersection(conjunto2)`         |
| `.difference(other)`          | Retorna a diferença de dois conjuntos.                                                         | `conjunto1 - conjunto2` ou `conjunto1.difference(conjunto2)`           |
| `.symmetric_difference(other)`| Retorna a diferença simétrica de dois conjuntos.                                               | `conjunto1 ^ conjunto2` ou `conjunto1.symmetric_difference(conjunto2)` |
| `.issubset(other)`            | Verifica se o conjunto é um subconjunto de outro.                                              | `subconjunto.issubset(conjunto1)`                                      |
| `.issuperset(other)`          | Verifica se o conjunto é um superconjunto de outro.                                            | `conjunto1.issuperset(subconjunto)`                                    |
| `.isdisjoint(other)`          | Verifica se dois conjuntos são disjuntos (não têm elementos em comum).                        | `conjunto1.isdisjoint(conjunto2)`                                      |
| `.copy()`                     | Retorna uma cópia rasa do conjunto.                                                           | `conjunto.copy()`                                                      |
| `.clear()`                    | Remove todos os elementos do conjunto.                                                        | `conjunto.clear()`                                                     |
| `.len(set)`                   | Retorna o número de elementos no conjunto.                                                    | `len(conjunto)`                                                        |
| `.in`                         | Verifica se um elemento está no conjunto.                                                     | `3 in conjunto1`                                                       |
| `.not in`                     | Verifica se um elemento não está no conjunto.                                                 | `6 not in conjunto1`                                                   |
| `.update(other)`              | Adiciona elementos de outro conjunto ao conjunto.                                              | `conjunto1.update(conjunto2)`                                          |
| `.intersection_update(other)` | Atualiza o conjunto com a interseção entre ele e outro.                                         | `conjunto1.intersection_update(conjunto2)`                             |
| `.difference_update(other)`   | Atualiza o conjunto com a diferença entre ele e outro.                                          | `conjunto1.difference_update(conjunto2)`                               |
| `.symmetric_difference_update(other)` | Atualiza o conjunto com a diferença simétrica entre ele e outro.                       | `conjunto1.symmetric_difference_update(conjunto2)`                     |
| `.pop()`                      | Remove e retorna um elemento arbitrário do conjunto. Levanta um erro `KeyError` se o conjunto estiver vazio. | `conjunto.pop()`                                          |
| `.frozenset(iterable)`        | Retorna uma versão imutável de um conjunto.                                                    | `fconjunto = frozenset([1, 2, 3])`                                     |

# Funções

Funções são blocos de código reutilizáveis que executam uma tarefa específica. Elas permitem modularizar programas, tornando o código mais organizado, legível e fácil de manter. As funções podem receber entradas (argumentos), processá-las e retornar um resultado.

## Definindo Funções
Para definir uma função em Python, usamos a palavra-chave def, seguida pelo nome da função, parênteses que podem conter parâmetros e dois pontos. O corpo da função é indentado.

```python
def nome_da_funcao(parametros):
    # corpo da função
    return resultado
```

Exemplo Simples de Função
```python
def saudacao(nome):
    return f"Olá, {nome}!"

print(saudacao("João"))  # Saída: Olá, João!
```
## Funções com Parâmetros Padrão
Permitem definir valores padrão para parâmetros que podem ser omitidos ao chamar a função.

```python
def saudacao(nome, mensagem="Olá"):
    return f"{mensagem}, {nome}!"

print(saudacao("Maria"))          # Saída: Olá, Maria!
print(saudacao("Pedro", "Oi"))    # Saída: Oi, Pedro!
```

## Funções com Múltiplos Parâmetros
Aceitam múltiplos argumentos e podem realizar operações mais complexas.

```python
def soma(a, b):
    return a + b

print(soma(5, 7))  # Saída: 12
```

## Funções com Retorno Múltiplo
Podem retornar múltiplos valores usando tuplas.

```python
def operacoes(a, b):
    soma = a + b
    diferenca = a - b
    return soma, diferenca

resultado_soma, resultado_diferenca = operacoes(10, 5)
print(resultado_soma)       # Saída: 15
print(resultado_diferenca)  # Saída: 5
```

## Funções Anônimas (Lambda)
São funções pequenas e sem nome, definidas usando a palavra-chave lambda. São úteis para funções curtas e simples.

```python
dobro = lambda x: x * 2
print(dobro(4))  # Saída: 8
```

## Funções com Argumentos Variáveis
Aceitam um número variável de argumentos usando *args e **kwargs.

```python
def soma(*numeros):
    return sum(numeros)

print(soma(1, 2, 3, 4))  # Saída: 10

def imprimir_informacoes(**info):
    for chave, valor in info.items():
        print(f"{chave}: {valor}")

imprimir_informacoes(nome="Ana", idade=25)  
# Saída:
# nome: Ana
# idade: 25
```
# Manipulação de Strings
## Criação de Strings
Strings em Python podem ser criadas usando aspas simples (`'`), aspas duplas (`"`), aspas triplas simples (`'''`) ou aspas triplas duplas (`"""`).

```python
str1 = 'Olá, Mundo!'
str2 = "Olá, Mundo!"
str3 = '''Olá, 
Mundo!'''
str4 = """Olá, 
Mundo!"""
```
### Características das Strings
* Imutabilidade: Uma vez criada, uma string não pode ser alterada. Qualquer operação que modifique uma string cria uma nova string.
* Acesso: Pode-se acessar caracteres individuais em uma string usando índices. O índice em Python é baseado em zero.

### Fatiamento (Slicing)
O fatiamento permite acessar uma subseção de uma string usando a notação [início:fim:passo].
```python
s = "Python"
print(s[1:4])    # yth
print(s[:2])     # Py
print(s[3:])     # hon
print(s[::2])    # Pto
print(s[::-1])   # nohtyP (inverso da string)
````
### Operações com Strings
* Concatenar Strings:
```python
s1 = "Olá"
s2 = "Mundo"
s3 = s1 + ", " + s2 + "!"  # "Olá, Mundo!"
```
* Repetir Strings:
```python
s = "A" * 5  # "AAAAA"
```

## Formatação de Strings
### Método `format()`
Utiliza chaves {} como placeholders para valores.

```python
nome = "João"
idade = 30
mensagem = "Meu nome é {} e eu tenho {} anos.".format(nome, idade)
# "Meu nome é João e eu tenho 30 anos."
```

### f-strings (Python 3.6+)
Usa f antes da string e variáveis dentro de chaves {}.

```python
nome = "João"
idade = 30
mensagem = f"Meu nome é {nome} e eu tenho {idade} anos."
# "Meu nome é João e eu tenho 30 anos."
```
### Operador `%`:
```python
nome = "Maria"
idade = 25
print("Nome: %s, Idade: %d" % (nome, idade))  # Nome: Maria, Idade: 25
```

### Strings Multilinha
Strings multilinha são úteis para longos blocos de texto.

```python
multilinha = """Esta é uma string
multilinha, que pode conter
várias linhas de texto."""
```
## Métodos Comuns
| Função                         | Descrição                                             | Exemplo                                                         |
|--------------------------------|-------------------------------------------------------|-----------------------------------------------------------------|
| `str.lower()`                  | Converte todos os caracteres para minúsculas          | `"Python".lower() -> "python"`                                  |
| `str.upper()`                  | Converte todos os caracteres para maiúsculas          | `"Python".upper() -> "PYTHON"`                                  |
| `str.capitalize()`             | Converte o primeiro caractere para maiúscula e restante para minúsculas | `"python".capitalize() -> "Python"`                             |
| `str.title()`                  | Converte o primeiro caractere de cada palavra para maiúscula | `"python é incrível".title() -> "Python É Incrível"`             |
| `str.strip()`                  | Remove espaços em branco do início e do fim           | `"  Olá, Mundo!  ".strip() -> "Olá, Mundo!"`                    |
| `str.rstrip()`                 | Remove espaços em branco do fim                       | `"  Olá, Mundo!  ".rstrip() -> "  Olá, Mundo!"`                 |
| `str.lstrip()`                 | Remove espaços em branco do início                    | `"  Olá, Mundo!  ".lstrip() -> "Olá, Mundo!  "`                 |
| `str.replace(old, new)`        | Substitui todas as ocorrências de uma substring       | `"Olá, Mundo!".replace("Mundo", "Python") -> "Olá, Python!"`    |
| `str.split(sep=None)`          | Divide a string em uma lista de substrings            | `"Olá, Mundo!".split() -> ["Olá,", "Mundo!"]`                   |
| `str.join(iterable)`           | Junta elementos de um iterável em uma string          | `', '.join(['Olá', 'Python']) -> "Olá, Python"`                 |
| `str.startswith(prefix)`       | Verifica se a string começa com o prefixo especificado | `"Python".startswith("Py") -> True`                             |
| `str.endswith(suffix)`         | Verifica se a string termina com o sufixo especificado | `"Python".endswith("on") -> True`                               |
| `str.find(sub)`                | Retorna o índice da primeira ocorrência da substring  | `"Python é incrível".find("é") -> 7`                            |
| `str.count(sub)`               | Conta o número de ocorrências da substring            | `"Python é incrível".count("i") -> 2`                           |
| `str.format(*args, **kwargs)`  | Formata a string usando placeholders                  | `"Nome: {}, Idade: {}".format("Maria", 25) -> "Nome: Maria, Idade: 25"` |
| `f'string'`                    | Formata a string usando f-strings                     | `f"Nome: {'Maria'}, Idade: {25}" -> "Nome: Maria, Idade: 25"`   |
| `str + str`                    | Concatena duas strings                                | `"Olá" + ", " + "Mundo!" -> "Olá, Mundo!"`                      |
| `str * n`                      | Repete a string n vezes                                | `"A" * 5 -> "AAAAA"`                                            |
| `str[índice]`                  | Acessa o caractere na posição indicada                | `"Python"[0] -> "P"`                                            |
| `str[início:fim:passo]`        | Fatiamento: retorna a subseção da string              | `"Python"[1:4] -> "yth"`                                        |


# Manipulação de Arquivos

## Abertura de arquivos
Para manipular um arquivo, primeiro precisamos abri-lo. A função `open()` é utilizada para isso. 
### Sintaxe Básica 
```python
file = open('caminho_do_arquivo', 'modo')
```
### Modos de Abertura 
* `'r'`: Leitura (padrão). O arquivo deve existir.
* `'w'`: Escrita. Cria um novo arquivo ou sobrescreve o existente.
* `'a'`: Acrescentar. Adiciona ao final do arquivo.
* `'b'`: Binário. Utilizado com outros modos,

## Leitura de arquivos
Depois de abrir o arquivo, podemos ler seu conteúdo.

Considere o arquivo de texto chamado `exemplo.txt` com o seguinte conteúdo:
```
Linha 1
Linha 2
Linha 3
Linha 4
Linha 5
```
### Métodos de Leitura
* `read(size)`: Lê o arquivo inteiro ou até o tamanho especificado.
* `readline()`: Lê uma linha do arquivo.
* `readlines()`: Lê todas as linhas e retorna uma lista.

### Leitura Completa
```python
file = open('exemplo.txt', 'r')
conteudo = file.read()
print(conteudo)
file.close()
```
### Leitura Linha por Linha
```python
file = open('exemplo.txt', 'r')
for linha in file:
    print(linha, end='') # end='' é usado para evitar duplicação de novas linhas
file.close()
```
### Leitura com `readline()`
```python
file = open('exemplo.txt', 'r')
linha = file.readline()
while linha:
    print(linha, end='')
    linha = file.readline()
file.close()
```
### Leitura com `readlines()`
```python
file = open('exemplo.txt', 'r')
linhas = file.readlines()
for linha in linhas:
    print(linha, end='')
file.close()
```

## Escrita em arquivos
Para escrever em um arquivo, devemos abrir o arquivo em modo de escrita. Se o arquivo não existir, ele será criado.
### Métodos de Escrita 
* `write(string)`: Escreve uma string no arquivo.
* `writelines(lista)`: Escreve uma lista de strings no arquivo.

#### Escrita com `write()` 
```python
file = open('exemplo.txt', 'w')
file.write('Olá, Mundo!')
file.close()
```
#### Escrita com `writelines()` 
```python
file = open('exemplo.txt', 'w')
linhas = ['Primeira linha\n', 'Segunda linha\n', 'Terceira linha\n']
file.writelines(linhas)
file.close()
```
## Fechamento de arquivos
É importante sempre fechar o arquivo após concluir as operações. Isso garante que todos os recursos sejam liberados e que todas as alterações sejam salvas corretamente.

### Método `close()`
```python
file = open('exemplo.txt', 'r')
# Operações no arquivo
file.close()
```

### Gerenciamento de Contexto (with statement)
Usar `with` é uma prática recomendada, pois garante que o arquivo seja fechado corretamente, mesmo se ocorrer uma exceção.

```python
with open('exemplo.txt', 'r') as file:
    conteudo = file.read()
    print(conteudo)
# O arquivo é fechado automaticamente ao sair do bloco `with`
```
* Prefira usar o bloco `with` para abrir arquivos. Ele torna o código mais limpo e seguro.
* O método `close()` ainda pode ser utilizado, mas requer mais cuidado para garantir que o arquivo seja fechado em caso de erro.

## Manipulação de Arquivos de Texto
## Manipulação de Arquivos Binários
## Manipulação Avançada de Arquivos
### Leitura de CSV
Para manipular arquivos CSV, usamos o módulo csv. CSV é um formato comum para armazenamento de dados tabulares.

```python
import csv

# Criando um arquivo CSV de exemplo
with open('dados.csv', 'w', newline='') as file:
    escritor = csv.writer(file)
    escritor.writerow(['Nome', 'Idade'])
    escritor.writerow(['Alice', 30])
    escritor.writerow(['Bob', 25])

# Lendo o arquivo CSV
with open('dados.csv', 'r') as file:
    leitor = csv.reader(file)
    for linha in leitor:
        print(linha)
# Saída:
# ['Nome', 'Idade']
# ['Alice', 30]
# ['Bob', 25]
```

### Escrita em CSV
```python
import csv

dados = [
    ['Nome', 'Idade'],
    ['Alice', 30],
    ['Bob', 25]
]

with open('dados.csv', 'w', newline='') as file:
    escritor = csv.writer(file)
    escritor.writerows(dados)
```

### Leitura de JSON
Para manipular arquivos JSON, usamos o módulo json. JSON é um formato leve para intercâmbio de dados.
```python
import json

# Criando um arquivo JSON de exemplo
dados = {
    'nome': 'Alice',
    'idade': 30,
    'cidade': 'São Paulo'
}

with open('dados.json', 'w') as file:
    json.dump(dados, file, indent=4)

# Lendo o arquivo JSON
with open('dados.json', 'r') as file:
    dados = json.load(file)
    print(dados)
# Saída:
# {'nome': 'Alice', 'idade': 30, 'cidade': 'São Paulo'}
```
### Escrita em JSON
```python
import json

dados = {
    'nome': 'Alice',
    'idade': 30,
    'cidade': 'São Paulo'
}

with open('dados.json', 'w') as file:
    json.dump(dados, file, indent=4)
```    
## Erros Comuns e Tratamento de Exceções
Erros podem ocorrer durante a manipulação de arquivos. É importante tratar exceções para garantir que o programa lide adequadamente com esses erros. 

```python
try:
   with open('exemplo.txt', 'r') as file:
      conteudo = file.read()
except FileNotFoundError:
   print("O arquivo não foi encontrado.")
except IOError:
   print("Ocorreu um erro de entrada/saída.")
```
### Erros Comuns:
* FileNotFoundError: Ocorre quando se tenta abrir um arquivo que não existe.
* IOError: Erros gerais de leitura/escrita.
* ValueError: Uso incorreto de argumentos nos métodos de leitura/escrita.
* PermissionError: Ocorre quando se tenta abrir um arquivo sem as permissões adequadas para leitura ou gravação.
* UnicodeDecodeError: Erro ao tentar decodificar os dados de um arquivo de texto usando codificação inadequada.

### Boas Prãticas 
* Sempre use blocos `try` e `except` para capturar e tratar possíveis erros.
* Verifique se o arquivo existe antes de tentar abri-lo para leitura.
* Seja específico nos blocos `except` para tratar diferentes tipos de erros de forma apropriada.
* Use a codificação correta ao ler ou gravar arquivos de texto. Use o argumento encoding `open('exemplo.txt','r', encoding='utf-8')`.


