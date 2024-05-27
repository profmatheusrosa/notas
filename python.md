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
   - [Princípios Fundamentais da POO](#principios-fundamentais-da-poo)
   - [Classes e objetos](#classes-e-objetos)
   - [Métodos e atributos](#atributos-e-métodos)
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




# 3. Coleções de Dados

## - Listas
As listas são coleções ordenadas e mutáveis de itens. Elas podem conter elementos de diferentes tipos (inteiros, strings, etc.) e permitem a modificação de seus elementos após a criação. 

Exemplo de criação de lista:
```python
lista = [1, 2, 3, "quatro", 5.0]
```

## - Tuplas
As tuplas são coleções ordenadas e imutáveis de itens. Elas são semelhantes às listas, mas, uma vez criadas, seus elementos não podem ser modificados.

Exemplo de criação de tupla:
```python
Copiar código
tupla = (1, 2, 3, "quatro", 5.0)
```

## - Dicionários
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


## - Conjuntos

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

# 4. Funções

Funções são blocos de código reutilizáveis que executam uma tarefa específica. Elas permitem modularizar programas, tornando o código mais organizado, legível e fácil de manter. As funções podem receber entradas (argumentos), processá-las e retornar um resultado.

## - Definindo Funções
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
## - Funções com Parâmetros Padrão
Permitem definir valores padrão para parâmetros que podem ser omitidos ao chamar a função.

```python
def saudacao(nome, mensagem="Olá"):
    return f"{mensagem}, {nome}!"

print(saudacao("Maria"))          # Saída: Olá, Maria!
print(saudacao("Pedro", "Oi"))    # Saída: Oi, Pedro!
```

## - Funções com Múltiplos Parâmetros
Aceitam múltiplos argumentos e podem realizar operações mais complexas.

```python
def soma(a, b):
    return a + b

print(soma(5, 7))  # Saída: 12
```

## - Funções com Retorno Múltiplo
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

## - Funções Anônimas (Lambda)
São funções pequenas e sem nome, definidas usando a palavra-chave lambda. São úteis para funções curtas e simples.

```python
dobro = lambda x: x * 2
print(dobro(4))  # Saída: 8
```

## - Funções com Argumentos Variáveis
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
# 6. Manipulação de Arquivos

## 6.1. Abertura de arquivos
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

## 6.2. Leitura de arquivos
Depois de abrir o arquivo, podemos ler seu conteúdo.

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
    print(linha, end='')
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
## 6.3. Escrita em arquivos
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
## 6.4. Fechamento de arquivos
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

## 6.5. Manipulação de Arquivos de Texto
## 6.6. Manipulação de Arquivos Binários
## 6.7. Manipulação Avançada de Arquivos
## 6.8. Erros Comuns e Tratamento de Exceções
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

# 8. Programação Orientada a Objetos (POO)
A Programação Orientada a Objetos (POO) é um paradigma de programação que organiza o software em "objetos", que são instâncias de "classes". Uma classe pode ser vista como um molde ou template que define os atributos (dados) e métodos (funções) que os objetos criados a partir dela terão.

## 8.1. Princípios Fundamentais da POO
### Abstração:
Abstração é o processo de simplificar a complexidade do software, focando nos aspectos essenciais de uma entidade, ocultando detalhes desnecessários.
Exemplo: Ao modelar um carro, a abstração poderia focar nos atributos "marca", "modelo" e "ano", sem se preocupar com detalhes como o tipo de material usado nos bancos.

### Encapsulamento:
Encapsulamento é o princípio de esconder os detalhes internos de um objeto e expor apenas o que é necessário para a interação com outros objetos.
Exemplo: Um objeto ContaBancaria pode esconder seu saldo com um atributo privado e fornecer métodos públicos depositar e sacar para manipular esse saldo.

### Herança:
Herança permite que uma classe (classe filha) herde atributos e métodos de outra classe (classe pai), promovendo a reutilização de código.
Exemplo: Uma classe Veiculo pode ser a classe pai de Carro e Moto, onde ambos herdam atributos como marca e modelo.

### Polimorfismo:
Polimorfismo permite que diferentes classes sejam tratadas através da mesma interface. Métodos com o mesmo nome podem ter diferentes implementações.
Exemplo: Um método fazer_som pode ser implementado de formas diferentes em classes Cachorro e Gato.

A POO é um paradigma poderoso e amplamente utilizado que facilita a criação de software modular, reutilizável e fácil de manter. Comparado a outros paradigmas, como a programação procedural e funcional, a POO oferece uma maneira intuitiva de modelar e interagir com entidades complexas, refletindo melhor a maneira como pensamos sobre o mundo real. No entanto, a escolha do paradigma deve ser baseada nas necessidades específicas do projeto e nas preferências da equipe de desenvolvimento.

## 8.2. Classes e objetos
### Classe
Uma classe é um modelo ou um molde que define a estrutura e o comportamento (atributos e métodos) que os objetos criados a partir dessa classe terão. Ela encapsula dados e funcionalidades que operam sobre esses dados, permitindo a criação de novos tipos de dados definidos pelo usuário.

Definição de uma Classe
Uma classe é definida usando a palavra-chave class, seguida pelo nome da classe.

```python
class Carro:
    # Construtor da classe
    def __init__(self, marca, modelo, ano):
        self.marca = marca  # Atributo de instância
        self.modelo = modelo  # Atributo de instância
        self.ano = ano  # Atributo de instância
```

### Objeto
Um objeto é uma instância de uma classe. Quando uma classe é definida, nenhum espaço na memória é alocado até que um objeto dessa classe seja instanciado. Um objeto é uma entidade que contém um estado (valores de atributos) e um comportamento (métodos).

Criação de um Objeto
Para criar um objeto de uma classe, utilizamos a seguinte sintaxe:

```python
meu_carro = Carro('Toyota', 'Corolla', 2020)
Aqui, meu_carro é um objeto da classe Carro com atributos marca, modelo e ano.
```
## 8.3. Métodos e atributos
## 8.4. Herança e polimorfismo
A herança e o polimorfismo são conceitos poderosos na POO, permitindo a criação de sistemas flexíveis, reutilizáveis e facilmente mantidos. Utilizá-los corretamente é fundamental para o desenvolvimento de software robusto e eficiente.

### Herança
Herança é o mecanismo pelo qual uma classe (chamada de classe derivada ou subclasse) pode herdar atributos e métodos de outra classe (chamada de classe base ou superclasse). Isso permite a criação de uma hierarquia de classes e a reutilização de código.

Vantagens:

Reutilização de Código: Ao herdar de uma classe base, uma subclasse pode reutilizar os métodos e atributos da classe base sem precisar reescrever o código.
Facilidade de Manutenção: Alterações no comportamento comum podem ser feitas na classe base e refletidas em todas as subclasses.
Organização: Facilita a organização do código ao agrupar funcionalidades comuns em uma classe base.
Implementação em Python:
Para implementar herança em Python, utilizamos a sintaxe class Subclasse(Superclasse):. A subclasse pode sobrescrever métodos da superclasse para alterar seu comportamento.

Exemplo:

```python
# Classe base
class Animal:
    def __init__(self, nome):
        self.nome = nome

    def fazer_som(self):
        raise NotImplementedError("Subclasses devem implementar este método")

# Classe derivada
class Cachorro(Animal):
    def fazer_som(self):
        return "Au Au"

# Outra classe derivada
class Gato(Animal):
    def fazer_som(self):
        return "Miau"

# Uso das classes
meu_cachorro = Cachorro("Rex")
meu_gato = Gato("Mimi")
print(meu_cachorro.nome)  # Rex
print(meu_cachorro.fazer_som())  # Au Au
print(meu_gato.nome)  # Mimi
print(meu_gato.fazer_som())  # Miau
```

Neste exemplo, Cachorro e Gato herdam de Animal. Cada subclasse implementa o método fazer_som de maneira específica, proporcionando comportamentos diferentes para cada tipo de animal.

### Polimorfismo
É a capacidade de diferentes classes de serem tratadas como instâncias de uma mesma classe base. Ele permite que métodos com o mesmo nome em diferentes classes tenham comportamentos distintos.

### Tipos de Polimorfismo:

### Polimorfismo em tempo de compilação (ou sobrecarga): Python não suporta sobrecarga de métodos de forma nativa como em outras linguagens (por exemplo, C++). Em Python, métodos não podem ter o mesmo nome e diferentes assinaturas.

### Polimorfismo em tempo de execução: Python suporta polimorfismo em tempo de execução, permitindo que métodos sejam sobrescritos nas subclasses.

Implementação em Python:
Polimorfismo é frequentemente implementado utilizando herança e a sobrescrita de métodos. Classes derivadas podem ser tratadas como instâncias da classe base, e métodos específicos da classe derivada serão chamados.

Exemplo:

```python
class Animal:
    def fazer_som(self):
        raise NotImplementedError("Subclasses devem implementar este método")

class Cachorro(Animal):
    def fazer_som(self):
        return "Au Au"

class Gato(Animal):
    def fazer_som(self):
        return "Miau"

def emitir_som(animal):
    print(animal.fazer_som())

# Lista de diferentes objetos do tipo Animal
animais = [Cachorro(), Gato()]

for animal in animais:
    emitir_som(animal)
```
### Boas Práticas:
Evitar Herança Múltipla: Pode complicar a hierarquia de classes e introduzir problemas difíceis de depurar.
Preferir Composição a Herança: Use composição para combinar comportamentos em vez de criar hierarquias complexas.
Interface Clara: Defina métodos abstratos claros na classe base para garantir que subclasses implementem a funcionalidade necessária.

## 8.5. Encapsulamento e Abstração
Encapsulamento e abstração são técnicas complementares na POO que ajudam a gerir a complexidade, melhorar a modularidade e proteger a integridade dos dados. O encapsulamento foca em esconder os detalhes internos de implementação e proteger os dados, enquanto a abstração se concentra em simplificar e generalizar conceitos para facilitar a interação com os objetos. Em conjunto, essas práticas promovem a criação de sistemas robustos, flexíveis e de fácil manutenção.

## Encapsulamento
Refere-se à prática de restringir o acesso direto aos dados de um objeto e permitir que esses dados sejam manipulados apenas por métodos definidos. Em Python, isso é conseguido usando convenções de nomenclatura e mecanismos de controle de acesso, como atributos e métodos privados.

### Objetivo:
Proteger o estado interno do objeto contra modificações não controladas.
Fornecer uma interface pública clara e estável para a interação com o objeto.
Aumentar a modularidade e facilitar a manutenção do código.
Atributos Privados:
Em Python, atributos privados são indicados por um prefixo de sublinhado duplo __. Essa convenção sugere que esses atributos não devem ser acessados diretamente fora da classe.

Exemplo:
```python
class ContaBancaria:
    def __init__(self, saldo_inicial):
        self.__saldo = saldo_inicial  # atributo privado

    def depositar(self, quantia):
        if quantia > 0:
            self.__saldo += quantia
        else:
            raise ValueError("A quantia de depósito deve ser positiva")

    def sacar(self, quantia):
        if 0 < quantia <= self.__saldo:
            self.__saldo -= quantia
        else:
            raise ValueError("Saldo insuficiente ou quantia inválida")

    def obter_saldo(self):
        return self.__saldo

# Utilização
conta = ContaBancaria(1000)
conta.depositar(200)
print(conta.obter_saldo())  # Saída: 1200
```

Métodos Públicos:
Os métodos públicos, como depositar, sacar e obter_saldo, permitem interagir com os dados encapsulados de maneira controlada.

Encapsulamento com Propriedades:
Python também oferece o decorador @property, que permite definir métodos que podem ser acessados como atributos, proporcionando uma maneira mais Pythonica de encapsular dados.

Exemplo:
```python
class ContaBancaria:
    def __init__(self, saldo_inicial):
        self.__saldo = saldo_inicial

    @property
    def saldo(self):
        return self.__saldo

    @saldo.setter
    def saldo(self, valor):
        if valor < 0:
            raise ValueError("O saldo não pode ser negativo")
        self.__saldo = valor

conta = ContaBancaria(1000)
print(conta.saldo)  # Saída: 1000
conta.saldo = 1200
print(conta.saldo)  # Saída: 1200
```

## Abstração 
É o processo de simplificação de sistemas complexos através da ocultação de detalhes desnecessários e exposição apenas das partes essenciais. Em POO, abstração permite que os desenvolvedores definam classes e objetos que representam conceitos gerais, enquanto ocultam os detalhes de implementação.

### Objetivo:
Simplificar a complexidade.
Fornecer uma interface clara e intuitiva.
Facilitar a reutilização de código.
Implementação de Abstração:
Abstração é frequentemente implementada através de classes abstratas e interfaces. Em Python, a classe ABC (Abstract Base Class) do módulo abc é utilizada para definir métodos abstratos.

Exemplo:
```python
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def emitir_som(self):
        pass

class Cachorro(Animal):
    def emitir_som(self):
        return "Au Au"

class Gato(Animal):
    def emitir_som(self):
        return "Miau"

# Utilização
def fazer_animal_emitir_som(animal):
    print(animal.emitir_som())

cachorro = Cachorro()
gato = Gato()

fazer_animal_emitir_som(cachorro)  # Saída: Au Au
fazer_animal_emitir_som(gato)      # Saída: Miau
```

### Interfaces:
Embora Python não tenha uma sintaxe de interface como Java, as classes abstratas e métodos abstratos funcionam de maneira semelhante, definindo um contrato que as subclasses devem implementar.
