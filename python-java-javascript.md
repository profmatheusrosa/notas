# Sumário

1. [Principais características](#principais-características)
2. [Principais comandos](#principais-comandos)
3. [Tipos de dados](#tipos-de-dados)
4. [Manipulação de Strings](#manipulação-de-strings)
5. [Manipulação de Listas](#manipulação-de-listas)
6. [Manipulação de Dicionários](#manipulação-de-dicionários)
7. [Específicos Python](#especificos-python)
---


# Principais Características
| Critério                        | Java                                   | JavaScript                            | Python                                 |
|---------------------------------|----------------------------------------|----------------------------------------|----------------------------------------|
| **Paradigma de Programação**    | Orientado a Objetos                    | Multi-paradigma (Orientado a Objetos, Procedural) | Multi-paradigma (Orientado a Objetos, Procedural, Funcional) |
| **Propósito/Domínio de Aplicação** | Geral (desktop, web, mobile)          | Web (front-end, back-end com Node.js) | Geral (web, automação, ciência de dados) |
| **Tipagem de Dados**            | Estática e Forte                      | Dinâmica e Fraca                       | Dinâmica e Forte                      |
| **Forma de Execução**           | Compilada e Interpretada              | Interpretada                           | Interpretada                          |
| **Ambiente de Execução**        | Máquina Virtual Java (JVM)            | Navegador e Node.js                   | Local e Servidor                      |
| **Gerenciamento de Memória**    | Gerenciamento automático com Garbage Collection | Automático (Garbage Collection)        | Automático (Garbage Collection)       |
| **Comunidade e Ecossistema**    | Grande e Estabelecida                 | Grande e Ativa                         | Grande e Ativa                        |
| **Sintaxe e Leitura de Código** | Sintaxe rigorosa e verbosa            | Sintaxe flexível e concisa             | Sintaxe limpa e legível               |
| **Uso em Desenvolvimento Web**  | Sim, com frameworks como Spring e Hibernate | Sim, com frameworks como React e Node.js | Sim, com frameworks como Django e Flask |
| **Uso em IA e Ciência de Dados** | Utilizado (principalmente com bibliotecas Java para machine learning) | Utilizado (com bibliotecas como TensorFlow.js e Node.js para server-side) | Muito utilizado (com bibliotecas como NumPy, Pandas, TensorFlow) |
| **Frameworks Populares (Banco de Dados)** | Hibernate, Spring Data JPA            | Sequelize, Mongoose                    | Django ORM, SQLAlchemy               |
| **Frameworks Populares (APIs)** | Spring Boot, Jersey                   | Express, Fastify                       | Django Rest Framework, Flask-RESTful |
| **Frameworks Populares (Web)**  | Spring MVC, Apache Struts             | React, Angular, Vue.js, Express        | Django, Flask                         |


# Principais comandos
| Sintaxe             | Java                          | JavaScript                  | Python                    |
|---------------------|-------------------------------|----------------------------- |---------------------------|
| Comentários         | `// Single-line, /* Multi-line */` | `// Single-line, /* Multi-line */` | `# Single-line, ''' Multi-line '''` |
| Variáveis           | `int x = 5;`                  | `let x = 5;`                 | `x = 5`                   |
| Estruturas de Controle | `if (condição) { // código }` | `if (condição) { // código }` | `if condição: # código`  |
|                     | `else if (outra) { // código }` | `else if (outra) { // código }` | `elif outra: # código`   |
|                     | `else { // código }`          | `else { // código }`         | `else: # código`         |
| Loops               | `for (int i=0; i<5; i++) { // código }` | `for (let i=0; i<5; i++) { // código }` | `for i in range(5): # código`  |
|                     | `while (condição) { // código }` | `while (condição) { // código }` | `while condição: # código`     |
| Funções            | `returnType functionName() { // código return value; }` | `function functionName() { // código return value; }` | `def functionName(): # código` |
| Listas/Arrays      | `int[] array = {1, 2, 3};`     | `let array = [1, 2, 3];`      | `array = [1, 2, 3]`       |
| Dicionários/Objetos | `Map<Key, Value> map = new HashMap<>();` | `let obj = {};`           | `dict = {}`              |
| Impressão na Tela  | `System.out.println();`        | `console.log();`             | `print()`                |


# Tipos de dados
| Tipo de Dado       | Java                       | JavaScript                        | Python                                 |
|-------------------- |--------------------------- |---------------------------------- |----------------------------------------|
| Números Inteiros    | `int x = 5;`                    | `let x = 5;`                      | `x = 5`                                |
| Números Longos      | `long y = 1000000000L;`         | Não aplicável                    | `y = 1000000000`                       |
| Números de Ponto Flutuante Simples | `float z = 3.14f;`          | `let z = 3.14;`                   | `z = 3.14`                             |
| Texto/String        | `String str = "Hello";`     | `let str = "Hello";`              | `str = "Hello"`                        |
| Booleano            | `boolean flag = true;`      | `let flag = true;`                | `flag = True`                          |
| Lista/Array         | `int[] numbers = {1, 2, 3};` | `let numbers = [1, 2, 3];`         | `numbers = [1, 2, 3]`                   |
| Dicionário/Objeto   | `Map<String, Integer> map = new HashMap<>();` | `let obj = {key: value};`   | `dict = {'key': value}`                |
| Null/Undefined      | `String str = null;`        | `let variable;`                   | `variable = None`                      |
| Data/Tempo          | `Date now = new Date();`     | `let now = new Date();`           | `from datetime import datetime`<br>`now = datetime.now()` |
| Conjunto            | `Set<String> set = new HashSet<>();` | `let set = new Set();`      | `set = set()`                         |
| Caractere           | `char letter = 'A';`         | `let letter = 'A';`               | `letter = 'A'`                         |
| Tipagem (Type)      | Estática                    | Dinâmica                          | Dinâmica                               |


# Manipulação de Strings
| Descrição | Java                  | JavaScript            | Python               |
|------------------------|-----------------------|------------------------|----------------------|
| Criar uma String       | `String str = "Hello";` | `let str = "Hello";`  | `str = "Hello"`       |
| Concatenação           | `String result = str + " World";` | `let result = str + " World";` | `result = str + " World"` |
| Comprimento            | `int length = str.length();` | `let length = str.length();` | `length = len(str)`   |
| Acessar Caractere      | `char firstChar = str.charAt(0);` | `let firstChar = str[0];` | `firstChar = str[0]`  |
| Substring              | `String substr = str.substring(start, end);` | `let substr = str.substring(start, end);` | `substr = str[start:end]` |
| Busca                  | `int index = str.indexOf("lo");` | `let index = str.indexOf("lo");` | `index = str.find("lo")` |
| Substituição           | `String newStr = str.replace("l", "w");` | `let newStr = str.replace("l", "w");` | `newStr = str.replace("l", "w")` |
| Maiúsculas             | `String upper = str.toUpperCase();` | `let upper = str.toUpperCase();` | `upper = str.upper()` |
| Minúsculas             | `String lower = str.toLowerCase();` | `let lower = str.toLowerCase();` | `lower = str.lower()` |
| Quebra por Delimitador | `String[] parts = str.split(" ");` | `let parts = str.split(" ");` | `parts = str.split(" ")` |
| Formatação             | `String formatted = String.format("Value: %d", 42);` | `let formatted = `Value: ${42}`;` | `formatted = "Value: {}".format(42)` |


# Manipulação de Listas
| Descrição         | Java                           | JavaScript                      | Python                                |
|--------------------------|--------------------------------|----------------------------------|---------------------------------------|
| Criar uma Lista          | `List<String> list = new ArrayList<>();` | `let list = [];`                 | `list = []`                           |
| Adicionar Elemento       | `list.add("item");`             | `list.push("item");`            | `list.append("item")`                 |
| Acessar Elemento por Índice | `list.get(0);`                 | `let element = list[0];`         | `element = list[0]`                   |
| Tamanho da Lista         | `int size = list.size();`        | `let size = list.length;`        | `size = len(list)`                    |
| Verificar Existência de um Elemento | `list.contains("item");`  | `let contains = list.includes("item");` | `contains = "item" in list`           |
| Remover por Índice       | `list.remove(0);`               | `list.splice(0, 1);`             | `element = list.pop(0)`               |
| Remover por Valor        | `list.remove("item");`          | `let index = list.indexOf("item"); if (index !== -1) list.splice(index, 1);` | `list.remove("item")`                  |
| Sublista/Subarray        | `List<String> subList = list.subList(start, end);` | `let subArray = list.slice(start, end);` | `subList = list[start:end]`            |
| Ordenação                | `Collections.sort(list);`       | `list.sort();`                  | `list.sort()`                         |
| Inverter Lista           | `Collections.reverse(list);`    | `list.reverse();`               | `list.reverse()`                      |
| Filtrar Elementos por Condição | `List<String> filtered = list.stream().filter(condition).collect(Collectors.toList());` | `let filtered = list.filter(item => condition);` | `filtered = [item for item in list if condition]` |
| Mapear Elementos por Função | `List<String> mapped = list.stream().map(transform).collect(Collectors.toList());` | `let mapped = list.map(item => transform(item));` | `mapped = [transform(item) for item in list]` |


# Manipulação de Dicionários
| Operação            | Java                       | JavaScript                | Python                   |
|--------------------- |----------------------------|--------------------------- |--------------------------|
| Criar Dicionário    | `Map<Key, Value> map = new HashMap<>();` | `let obj = {};`          | `dict = {}`              |
| Adicionar Chave-Valor | `map.put(key, value);`      | `obj[key] = value;`        | `dict[key] = value`       |
| Acessar Valor por Chave | `Value value = map.get(key);` | `let value = obj[key];`  | `value = dict[key]`      |
| Verificar Chave     | `map.containsKey(key);`    | `key in obj;`             | `key in dict`            |
| Remover Chave-Valor | `map.remove(key);`         | `delete obj[key];`         | `del dict[key]`          |
| Iterar sobre Chaves  | `for (Key key : map.keySet()) { // código usando key }` | `for (let key in obj) { // código usando key }` | `for key in dict: # código usando key` |
| Iterar sobre Valores | `for (Value value : map.values()) { // código usando value }` | `for (let value of Object.values(obj)) { // código usando value }` | `for value in dict.values(): # código usando value` |
| Iterar sobre Chave-Valor | `for (Map.Entry<Key, Value> entry : map.entrySet()) { // código usando entry.getKey(), entry.getValue() }` | `for (let [key, value] of Object.entries(obj)) { // código usando key, value }` | `for key, value in dict.items(): # código usando key, value` |
| Obter Todas as Chaves | `Set<Key> keys = map.keySet();` | `let keys = Object.keys(obj);` | `keys = dict.keys()`     |
| Obter Todas os Valores | `Collection<Value> values = map.values();` | `let values = Object.values(obj);` | `values = dict.values()` |
| Obter Todas as Chave-Valor | `Set<Map.Entry<Key, Value>> entries = map.entrySet();` | `let entries = Object.entries(obj);` | `entries = dict.items()` |

# Específicos Python
- [ ] Comprehension
- [ ] Map
- [ ] Filter
- [ ] Reduce 
