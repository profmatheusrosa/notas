# Programação Orientada a Objetos (POO)
A Programação Orientada a Objetos (POO) é um paradigma de programação que organiza o software em "objetos", que são instâncias de "classes". Uma classe pode ser vista como um molde ou template que define os atributos (dados) e métodos (funções) que os objetos criados a partir dela terão.

## Princípios Fundamentais da POO
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

## Classes e objetos
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
## Atributos e Métodos
### Atributos
Os atributos são variáveis que armazenam informações sobre o objeto. Eles podem ser divididos em dois tipos principais:

### Atributos de Instância: 
São atributos que pertencem a uma instância específica da classe.
### Atributos de Classe: 
São atributos que pertencem à própria classe, compartilhados por todas as instâncias da classe.

### Atributos de Instância
Cada objeto instanciado a partir de uma classe pode ter diferentes valores para seus atributos de instância. Eles são definidos dentro do método __init__, que é um método especial chamado quando um novo objeto é criado.

```python
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

# Criando instâncias da classe Pessoa
p1 = Pessoa("Alice", 30)
p2 = Pessoa("Bob", 25)

print(p1.nome)  # Output: Alice
print(p2.idade)  # Output: 25
```

### Atributos de Classe
Atributos de classe são definidos diretamente dentro da classe, fora de qualquer método. Eles são compartilhados por todas as instâncias da classe.

```python
class Pessoa:
    especie = "Homo sapiens"  # Atributo de classe

    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

print(Pessoa.especie)  # Output: Homo sapiens

p1 = Pessoa("Alice", 30)
print(p1.especie)  # Output: Homo sapiens
```
### Métodos
Métodos são funções definidas dentro de uma classe que descrevem os comportamentos dos objetos dessa classe. Eles podem acessar e modificar os atributos do objeto.

### Métodos de Instância
Métodos de instância são os mais comuns e têm acesso ao objeto que os chamou através do parâmetro self.

```python
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

    def saudacao(self):
        return f"Olá, meu nome é {self.nome} e eu tenho {self.idade} anos."

p1 = Pessoa("Alice", 30)
print(p1.saudacao())  # Output: Olá, meu nome é Alice e eu tenho 30 anos.
```

### Métodos de Classe
Métodos de classe operam sobre a classe em si, e não sobre instâncias individuais. Eles são definidos usando o decorador @classmethod e recebem a própria classe como primeiro argumento, geralmente chamado de cls.

```python
class Pessoa:
    especie = "Homo sapiens"

    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

    @classmethod
    def alterar_especie(cls, nova_especie):
        cls.especie = nova_especie

Pessoa.alterar_especie("Homo sapiens sapiens")
print(Pessoa.especie)  # Output: Homo sapiens sapiens
```
### Métodos Estáticos
Métodos estáticos não operam nem sobre instâncias nem sobre a classe em si. Eles são definidos usando o decorador @staticmethod.

```python
class Pessoa:
    @staticmethod
    def e_maior_idade(idade):
        return idade >= 18

print(Pessoa.e_maior_idade(20))  # Output: True
print(Pessoa.e_maior_idade(15))  # Output: False
```
### Propriedades (Properties)
Propriedades são uma forma de encapsular o acesso a atributos de instância, permitindo que métodos sejam chamados como se fossem atributos. São definidas usando o decorador @property.

```python
class Pessoa:
    def __init__(self, nome, idade):
        self._nome = nome
        self._idade = idade

    @property
    def nome(self):
        return self._nome

    @nome.setter
    def nome(self, novo_nome):
        self._nome = novo_nome

p1 = Pessoa("Alice", 30)
print(p1.nome)  # Output: Alice
p1.nome = "Bob"
print(p1.nome)  # Output: Bob
```
## Métodos Especiais
Métodos especiais, também conhecidos como "métodos mágicos" ou "dunder methods" (double underscore), são métodos com nomes que começam e terminam com dois sublinhados (__). Eles permitem a definição de comportamentos especiais em classes.

### Construtor (`__init__`)
O método __init__ é o construtor da classe. Ele é chamado quando uma nova instância da classe é criada.

```python
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

pessoa1 = Pessoa("Alice", 30)
print(pessoa1.nome)  # Saída: Alice
print(pessoa1.idade)  # Saída: 30
```

### Representação (`__str__` e `__repr__`)
* `__str__`: Define a representação "amigável" do objeto, usada pelas funções str() e print().
* `__repr__`: Define a representação "oficial" do objeto, usada pela função repr() e idealmente deve ser uma string que, se avaliada pelo interpretador, cria o mesmo objeto.
```python
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

    def __str__(self):
        return f"Pessoa(nome={self.nome}, idade={self.idade})"

    def __repr__(self):
        return f"Pessoa('{self.nome}', {self.idade})"

pessoa1 = Pessoa("Alice", 30)
print(str(pessoa1))  # Saída: Pessoa(nome=Alice, idade=30)
print(repr(pessoa1))  # Saída: Pessoa('Alice', 30)
```
### Outros Métodos Especiais 
* `__len__`: Define o comportamento da função `len()`.
* `__getitem__`: Permite o acesso a itens de uma coleção usando colchetes (`[]`).
* `__setitem__`: Permite a atribuição de valores a itens de uma coleção usando colchetes.
* `__delitem__`: Permite a exclusão de itens de uma coleção usando colchetes.
* `__iter__`: Define o comportamento do objeto.
* `__next__`: Define a iteração sobre o objeto.
* `__call__`: Permite que uma instância de uma classe seja chamada como uma função.

## Herança
É o mecanismo pelo qual uma classe (chamada de classe derivada ou subclasse) pode herdar atributos e métodos de outra classe (chamada de classe base ou superclasse). Isso permite a criação de uma hierarquia de classes e a reutilização de código.

### Vantagens:
* Reutilização de Código: Ao herdar de uma classe base, uma subclasse pode reutilizar os métodos e atributos da classe base sem precisar reescrever o código.
* Facilidade de Manutenção: Alterações no comportamento comum podem ser feitas na classe base e refletidas em todas as subclasses.
* Organização: Facilita a organização do código ao agrupar funcionalidades comuns em uma classe base.

### Implementação em Python:
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

## Polimorfismo
É a capacidade de diferentes classes de serem tratadas como instâncias de uma mesma classe base. Ele permite que métodos com o mesmo nome em diferentes classes tenham comportamentos distintos.

### Tipos de Polimorfismo:

### Polimorfismo em tempo de compilação (ou sobrecarga)
Python não suporta sobrecarga de métodos de forma nativa como em outras linguagens (por exemplo, C++). Em Python, métodos não podem ter o mesmo nome e diferentes assinaturas.

### Polimorfismo em tempo de execução
Python suporta polimorfismo em tempo de execução, permitindo que métodos sejam sobrescritos nas subclasses.

### Implementação em Python:
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

## Encapsulamento e Abstração
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
