## **Sumário**
1. [Módulo 1: Introdução a Estruturas de Dados e Análise de Complexidade](#módulo-1-introdução-a-estruturas-de-dados-e-análise-de-complexidade)
   - 1.1 O que são Estruturas de Dados?
   - 1.2 Eficiência de Algoritmos
   - 1.3 Notação Big-O
   - 1.4 Exemplos de Código Comentados
2. [Módulo 2: Estruturas Lineares](#módulo-2-estruturas-lineares)
   - 2.1 Arrays e Listas
   - 2.2 Pilhas (LIFO)
   - 2.3 Filas (FIFO)
   - 2.4 Aplicações Práticas
3. [Módulo 3: HashMaps e Dicionários](#módulo-3-hashmaps-e-dicionários)
   - 3.1 Conceito de Hashing
   - 3.2 Tratamento de Colisões
   - 3.3 Implementação
   - 3.4 Aplicações Práticas
4. [Módulo 4: Árvores e Heaps](#módulo-4-árvores-e-heaps)
5. [Módulo 5: Grafos e Algoritmos de Busca](#módulo-5-grafos-e-algoritmos-de-busca)
6. [Módulo 6: Grafos Ponderados e Algoritmos de Otimização](#módulo-6-grafos-ponderados-e-algoritmos-de-otimização)
7. [Módulo 7: Programação Dinâmica e Resolução de Problemas](#módulo-7-programação-dinâmica-e-resolução-de-problemas)

---

### **Plano de Curso – Algoritmos e Estruturas de Dados**

| **Tópico Principal**                              | **Subtópico 1**                  | **Subtópico 2**                  | **Subtópico 3**                  | **Subtópico 4**            |
|---------------------------------------------------|-----------------------------------|-----------------------------------|-----------------------------------|----------------------------|
| **Módulo 1 – Introdução a Estruturas de Dados e Análise de Complexidade** | O que são Estruturas de Dados?   | Eficiência de Algoritmos          | Notação Big-O               | Medindo Complexidade       |
| **Módulo 2 – Estruturas Lineares**                | Arrays e Listas                  | Pilhas (LIFO)                    | Filas (FIFO)                    | Aplicações Práticas        |
| **Módulo 3 – HashMaps e Dicionários**             | Conceito de Hashing              | Tratamento de Colisões           | Implementação                  | Aplicações                 |
| **Módulo 4 – Árvores e Heaps**                    | Árvores Binárias (BST)           | Travessias (pré, in, pós-ordem)  | Heaps (mínimo/máximo)          | Union-Find                 |
| **Módulo 5 – Grafos e Algoritmos de Busca**       | Conceitos e Representação        | Busca em Largura (BFS)           | Busca em Profundidade (DFS)    | Aplicações                 |
| **Módulo 6 – Grafos Ponderados e Algoritmos de Otimização** | Algoritmo de Dijkstra            | Árvores Geradoras Mínimas (Prim/Kruskal) | Aplicações           | Implementações             |
| **Módulo 7 – Programação Dinâmica e Resolução de Problemas** | Conceito de PD                   | Problema da Mochila              | Fibonacci Otimizado           | Estratégias de Otimização  |

---

# Módulo 1: Introdução a Estruturas de Dados e Análise de Complexidade 

## **1.1 O que são Estruturas de Dados?**  
Estruturas de dados são formas organizadas de armazenar e gerenciar informações na memória do computador. Elas permitem a realização eficiente de operações como inserção, remoção, busca e ordenação.  

As principais estruturas de dados incluem:
- **Listas e Arrays** – Armazenam elementos de forma sequencial.
- **Pilhas e Filas** – Estruturas lineares com regras específicas de acesso.
- **Dicionários (HashMaps)** – Permitem acesso rápido a dados por meio de chaves.
- **Árvores e Grafos** – Estruturas hierárquicas e de relacionamentos.

A escolha da estrutura correta pode impactar diretamente o desempenho de um algoritmo.

---

## **1.2 Eficiência de Algoritmos**  

### **1.2.1 Por que a eficiência é importante?**  
Ao escrever um programa, muitas vezes há diversas maneiras de resolver um problema. No entanto, algumas soluções são significativamente mais rápidas e eficientes do que outras.  

A eficiência é crucial para:
- **Reduzir o tempo de execução** de um programa.
- **Otimizar o uso de memória** e recursos do sistema.
- **Garantir escalabilidade** quando lidamos com grandes volumes de dados.

Exemplo prático:
Se tivermos uma lista de um milhão de números e quisermos encontrar um número específico, um método de busca linear pode demorar muito, enquanto uma busca binária pode ser muito mais rápida.

---

## **1.3 Notação Big-O**  

### **1.3.1 O que é a Notação Big-O?**  
A notação Big-O é usada para medir a eficiência de um algoritmo, especialmente em relação ao crescimento do tempo de execução conforme a entrada aumenta.  

### **Tabela comparativa de complexidade**  

| **Complexidade** | **Descrição** | **Exemplo** |
|----------------|-------------|-------------|
| **O(1) – Constante** | O tempo de execução não muda com o tamanho da entrada. | Acesso direto a um elemento em um array. |
| **O(log n) – Logarítmica** | O tempo de execução cresce lentamente à medida que a entrada aumenta. | Busca binária em uma lista ordenada. |
| **O(n) – Linear** | O tempo de execução cresce proporcionalmente ao tamanho da entrada. | Percorrer uma lista para encontrar um elemento. |
| **O(n²) – Quadrática** | O tempo de execução cresce rapidamente com o tamanho da entrada. | Algoritmos de ordenação como Bubble Sort. |
| **O(2ⁿ) – Exponencial** | O tempo de execução dobra a cada novo elemento na entrada. | Algoritmos de força bruta, como Fibonacci recursivo sem otimização. |

---

## **1.4 Exemplos de Código Comentados**  

### **1.4.1 Exemplo de O(1) – Tempo Constante**  
```python
 def acessar_elemento(lista, index):
     """
     Retorna o elemento de uma lista no índice especificado.
     Essa operação ocorre em tempo constante O(1).
     """
     return lista[index]

# Teste do código
numeros = [10, 20, 30, 40, 50]
print(acessar_elemento(numeros, 2))  # Saída: 30
```

### **1.4.2 Exemplo de O(n) – Tempo Linear**  
```python
 def buscar_elemento(lista, elemento):
     """
     Percorre a lista para encontrar um elemento.
     No pior caso, a complexidade é O(n), pois pode ser necessário percorrer toda a lista.
     """
     for item in lista:
         if item == elemento:
             return True
     return False

# Teste do código
numeros = [10, 20, 30, 40, 50]
print(buscar_elemento(numeros, 30))  # Saída: True
```

---

# Módulo 2 – Estruturas Lineares

## Listas
As listas são uma das estruturas de dados mais utilizadas. Elas permitem armazenar múltiplos elementos em uma única variável e podem ser manipuladas de diversas formas.

### Características:
- Estrutura sequencial
- Permite armazenar diferentes tipos de dados
- Indexação por posição
- Pode ser modificada (mutável)

### Exemplo em Python:
```python
# Criando uma lista
numeros = [1, 2, 3, 4, 5]
print(numeros)

# Adicionando um elemento
numeros.append(6)
print(numeros)

# Removendo um elemento
numeros.remove(3)
print(numeros)
```

## Filas
A fila (queue) segue a regra **FIFO** (First In, First Out), onde o primeiro elemento a entrar é o primeiro a sair.

### Características:
- Inserção no final (enqueue)
- Remoção no início (dequeue)
- Útil em sistemas de processamento de tarefas

### Exemplo em Python:
```python
from collections import deque

fila = deque([1, 2, 3])
print(fila)

# Inserindo no final
fila.append(4)
print(fila)

# Removendo do início
fila.popleft()
print(fila)
```

## Pilhas
A pilha (stack) segue a regra **LIFO** (Last In, First Out), onde o último elemento a entrar é o primeiro a sair.

### Características:
- Inserção e remoção no topo
- Utilizada em chamadas recursivas, histórico de navegação, etc.

### Exemplo em Python:
```python
pilha = []

# Inserindo elementos
pilha.append(1)
pilha.append(2)
pilha.append(3)
print(pilha)

# Removendo do topo
pilha.pop()
print(pilha)
```

## Dicionários (Hashmaps)
Os dicionários armazenam dados em pares **chave-valor**, permitindo buscas eficientes.

### Características:
- Acesso rápido por chave
- Permite armazenar diferentes tipos de valores
- Não mantém ordem (antes do Python 3.7)

### Exemplo em Python:
```python
# Criando um dicionário
dados = {"nome": "Alice", "idade": 25, "cidade": "Brasília"}
print(dados)

# Acessando valores
print(dados["nome"])

# Adicionando novos pares
dados["profissão"] = "Engenheira"
print(dados)
```

Essas estruturas são fundamentais na programação e otimizam a manipulação de dados em diversas aplicações!

---

# Módulo 3: HashMaps e Dicionários

## **3.1 Conceito de Hashing**  
Hashing é uma técnica usada para mapear dados de tamanho arbitrário para valores fixos, chamados de "hashes". Essa técnica é amplamente utilizada em estruturas de dados como HashMaps e Dicionários para permitir acesso rápido aos dados.

### **Características do Hashing:**
- Usa uma função de hash para calcular o índice de armazenamento.
- Permite acesso eficiente em tempo constante O(1) na maioria dos casos.
- É amplamente utilizado em bancos de dados, caches e sistemas de busca.

---

## **3.2 Tratamento de Colisões**  
Colisões ocorrem quando dois elementos diferentes geram o mesmo valor de hash. Para lidar com isso, existem várias técnicas:

### **3.2.1 Encadeamento (Chaining):**
- Cada posição da tabela de hash armazena uma lista de elementos.
- Em caso de colisão, os elementos são adicionados à lista correspondente.

### **3.2.2 Endereçamento Aberto (Open Addressing):**
- Em vez de usar listas, os elementos são armazenados diretamente na tabela.
- Técnicas comuns:
  - **Linear Probing:** Procura a próxima posição disponível.
  - **Quadratic Probing:** Usa uma função quadrática para encontrar a próxima posição.
  - **Double Hashing:** Usa uma segunda função de hash para calcular o próximo índice.

---

## **3.3 Implementação**  
A implementação de HashMaps varia dependendo da linguagem de programação. Abaixo está um exemplo em Python usando dicionários:

```python
# Criando um dicionário
hashmap = {}

# Adicionando elementos
hashmap["chave1"] = "valor1"
hashmap["chave2"] = "valor2"

# Acessando elementos
print(hashmap["chave1"])  # Saída: valor1

# Verificando se uma chave existe
if "chave3" in hashmap:
    print("Chave encontrada!")
else:
    print("Chave não encontrada.")

# Removendo elementos
del hashmap["chave1"]
print(hashmap)
```

---

## **3.4 Aplicações Práticas**  
HashMaps e Dicionários são amplamente utilizados em diversas áreas da computação:

- **Armazenamento de Dados:** Para armazenar e acessar dados rapidamente.
- **Contagem de Frequências:** Contar a frequência de elementos em uma lista.
- **Caches:** Implementação de caches para melhorar o desempenho.
- **Sistemas de Busca:** Indexação de dados para buscas rápidas.

### **Exemplo: Contagem de Frequências**
```python
def contar_frequencias(lista):
    """
    Conta a frequência de cada elemento em uma lista.
    """
    frequencias = {}
    for item in lista:
        if item in frequencias:
            frequencias[item] += 1
        else:
            frequencias[item] = 1
    return frequencias

# Teste do código
dados = ["a", "b", "a", "c", "b", "a"]
print(contar_frequencias(dados))  # Saída: {'a': 3, 'b': 2, 'c': 1}
```

HashMaps e Dicionários são ferramentas poderosas que otimizam o desempenho de algoritmos e são essenciais para resolver problemas complexos de forma eficiente.

---

# Módulo 4: Árvores e Heaps
<!-- Conteúdo do módulo 4 -->

# Módulo 5: Grafos e Algoritmos de Busca
<!-- Conteúdo do módulo 5 -->

# Módulo 6: Grafos Ponderados e Algoritmos de Otimização
<!-- Conteúdo do módulo 6 -->

# Módulo 7: Programação Dinâmica e Resolução de Problemas
<!-- Conteúdo do módulo 7 -->
