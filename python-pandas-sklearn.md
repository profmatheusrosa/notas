# Súmario

1. [Series](#series)
   - [Funções](#funções)
3. [Dataframes](#dataframes)
   - [Funções](#funções)
   - [Filtros](#filtros)
- [Contribuição](#contribuição)
- [Licença](#licença)
---

# Series

Uma `Series` é uma estrutura de dados unidimensional do Pandas, uma das bibliotecas mais populares para manipulação e análise de dados em Python. Ela é fundamentalmente uma matriz unidimensional rotulada capaz de conter qualquer tipo de dado (inteiros, strings, números de ponto flutuante, objetos Python, etc.). Uma `Series` consiste em dois componentes principais:

1. **Dados**: Os dados são os elementos da série, que podem ser qualquer tipo de dado suportado pelo Python.
2. **Rótulos (Index)**: Os rótulos são os identificadores associados a cada elemento da série. Eles podem ser números inteiros, strings ou outros tipos de dados.

As `Series` do Pandas são semelhantes às listas do Python, mas com funcionalidades adicionais, como rótulos de índice, o que as torna muito mais poderosas e flexíveis para análise de dados.

Por exemplo, você pode criar uma série simples assim:

```python
import pandas as pd

# Criar uma série a partir de uma lista de valores
serie = pd.Series([10, 20, 30, 40, 50])

print(serie)
```
Isso resultará na seguinte saída:

```python
0    10
1    20
2    30
3    40
4    50
```

Observe que a série inclui automaticamente um índice numérico (0, 1, 2, ...) por padrão, mas você pode fornecer seus próprios rótulos de índice, se necessário. As séries podem ser acessadas por meio de seus índices, assim como as listas do Python:

### Funções
As principais funções de uma Series:

| Função | Descrição |
| --- | --- |
| `.head(n)` | Retorna as primeiras n linhas da série. |
| `.tail(n)` | Retorna as últimas n linhas da série. |
| `.describe()` | Retorna estatísticas descritivas da série. |
| `.value_counts()` | Conta a frequência de cada valor único na série. |
| `.unique()` | Retorna os valores únicos na série. |
| `.sort_values()` | Ordena os valores da série. |
| `.isnull() / .notnull()` | Retorna uma série booleana indicando valores nulos ou não nulos. |
| `.fillna(value)` | Preenche os valores nulos com um valor específico. |
| `.astype(dtype)` | Converte o tipo de dados da série para o especificado. |
| `.apply(func)` | Aplica uma função a cada elemento da série. |
| `.map(dict_or_func)` | Substitui cada valor da série por outro valor de acordo com um dicionário ou uma função. |
| `.iloc[]` | Permite acessar elementos da série por posição inteira. |
| `.loc[]` | Permite acessar elementos da série por rótulo. |
| `.between(left, right)` | Retorna uma série booleana indicando se os elementos estão entre os valores especificados. |
| `.clip(lower, upper)` | Limita os valores da série dentro de um intervalo especificado. |

# Dataframes

Um DataFrame é uma estrutura de dados bidimensional do Pandas, que é essencialmente uma tabela de dados organizada em linhas e colunas. Cada coluna em um DataFrame é uma Series, e todas as colunas compartilham o mesmo índice. Isso permite armazenar e manipular dados tabulares de forma eficiente em Python.
Um DataFrame consiste em três componentes principais:

1. **Dados**: Os dados são os elementos individuais da tabela, organizados em linhas e colunas.
2. **Rótulos de Linha (Index)**: Os rótulos de linha são os identificadores associados a cada linha do DataFrame. Eles podem ser números inteiros, strings ou outros tipos de dados.
3. **Rótulos de Coluna**: Os rótulos de coluna são os identificadores associados a cada coluna do DataFrame. Eles também podem ser números inteiros, strings ou outros tipos de dados.

É possível criar DataFrames de várias maneiras, uma das mais comuns é a partir de dicionários de listas:

```python
import pandas as pd

# Criar um DataFrame a partir de um dicionário de listas
data = {
    'Nome': ['Alice', 'Bob', 'Charlie', 'David'],
    'Idade': [25, 30, 35, 40],
    'Cidade': ['Nova York', 'Los Angeles', 'Chicago', 'Houston']
}

df = pd.DataFrame(data)

print(df)
```
Isso resultará na seguinte saída:

```python
      Nome  Idade       Cidade
0    Alice     25    Nova York
1      Bob     30  Los Angeles
2  Charlie     35      Chicago
3    David     40      Houston
```

## Funções
Os DataFrames do Pandas suportam uma variedade de operações de manipulação de dados, incluindo filtragem, seleção, agregação, mesclagem e muito mais. Aqui estão algumas das principais funções disponíveis para DataFrames:

| Função | Descrição |
| --- | --- |
| `.head(n)` | Retorna as primeiras n linhas do DataFrame. |
| `.tail(n)` | Retorna as últimas n linhas do DataFrame. |
| `.info()` | Fornece uma visão geral concisa do DataFrame. |
| `.describe()` | Calcula estatísticas descritivas para cada coluna numérica. |
| `.shape` | Retorna uma tupla representando a forma do DataFrame (número de linhas, número de colunas). |
| `.columns` | Retorna os rótulos das colunas do DataFrame. |
| `.index` | Retorna os rótulos das linhas do DataFrame. |
| `.loc[]` | Permite acessar um grupo de linhas e colunas pelo rótulo. |
| `.iloc[]` | Permite acessar um grupo de linhas e colunas por posição inteira. |
| `.drop(labels, axis=0/1)` | Remove linhas (quando axis=0) ou colunas (quando axis=1) especificadas pelo rótulo. |
| `.fillna(value)` | Preenche valores ausentes (NaN) com o valor especificado. |
| `.isnull() / .notnull()` | Retorna um DataFrame booleano indicando valores nulos ou não nulos. |
| `.groupby(by)` | Agrupa o DataFrame por uma ou mais colunas e aplica funções de agregação. |
| `.merge(right, how='inner', on=None)` | Combina o DataFrame atual com outro DataFrame usando uma lógica de junção semelhante ao SQL. |
| `.pivot_table(values, index, columns, aggfunc='mean')` | Cria uma tabela dinâmica a partir do DataFrame. |
| `.apply(func)` | Aplica uma função a cada elemento do DataFrame. |
| `.sort_values(by, ascending=True)` | Ordena os valores do DataFrame com base em uma ou mais colunas. |
| `.to_csv(path)` | Salva o DataFrame em um arquivo CSV. |
| `.plot()` | Gera visualizações básicas dos dados, como gráficos de linha, barras, histogramas, etc. |

Essas são apenas algumas das muitas funções disponíveis para DataFrames no Pandas. Elas fornecem uma ampla gama de ferramentas para análise e manipulação eficaz de dados tabulares.

---

### ⚠️ **Nota de Atenção: Compartilhamento de Referências em DataFrames do Pandas** ⚠️

Ao atribuir um DataFrame a outro DataFrame no Pandas, é importante estar ciente de que ambas as variáveis estão, na verdade, referenciando o mesmo objeto na memória. Isso significa que quaisquer alterações feitas no segundo DataFrame também serão refletidas no primeiro DataFrame, e vice-versa.

Por exemplo, considere o seguinte código:

```python
import pandas as pd

# Criar um DataFrame original
df_original = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

# Atribuir o DataFrame original a um novo DataFrame
df_novo = df_original

# Modificar o novo DataFrame
df_novo['C'] = [7, 8, 9]

print("DataFrame Original:")
print(df_original)
print("\nNovo DataFrame:")
print(df_novo)
```

Neste caso, ao adicionar a coluna 'C' ao `df_novo`, essa modificação também será refletida no `df_original`, pois ambos os DataFrames compartilham a mesma referência ao objeto DataFrame subjacente.

Para evitar esse comportamento e criar cópias independentes, é necessário utilizar o método `.copy()`:

```python
# Criar uma cópia independente do DataFrame original
df_copia = df_original.copy()

# Modificar a cópia do DataFrame
df_copia['D'] = [10, 11, 12]

print("DataFrame Original:")
print(df_original)
print("\nCópia do DataFrame:")
print(df_copia)
```

Ao utilizar `.copy()`, cada DataFrame terá sua própria cópia dos dados, garantindo que as alterações feitas em um DataFrame não afetem o outro.

Portanto, ao atribuir DataFrames no Pandas, sempre considere se deseja compartilhar referências ou criar cópias independentes, dependendo dos requisitos específicos do seu código.

---
## Filtros

Filtrar dados em um DataFrame no Pandas é uma operação comum e útil para selecionar apenas as linhas que atendem a determinados critérios. Existem várias maneiras de filtrar dados em um DataFrame. Algumas das abordagens mais comuns incluem o uso de:

1.  **Operadores de Comparação**: Você pode usar operadores de comparação, como igualdade (`==`), maior que (`>`), menor que (`<`), etc., para criar máscaras booleanas que indicam quais linhas satisfazem as condições especificadas.

```python
# Filtrar linhas onde a coluna 'idade' é maior que 30
df_filtrado = df[df['idade'] > 30]
```

2.  **Método .query()**: O método `.query()` permite filtrar um DataFrame usando expressões de consulta semelhantes ao SQL.

```python
# Filtrar linhas onde a coluna 'cidade' é igual a 'São Paulo'
df_filtrado = df.query("cidade == 'São Paulo'")
```

3.  **Método .loc\[\]**: O método `.loc[]` permite acessar linhas e colunas do DataFrame com base em rótulos de índice.

```python
# Filtrar linhas onde a coluna 'idade' é maior que 30 e 'cidade' é igual a 'São Paulo'
df_filtrado = df.loc[(df['idade'] > 30) & (df['cidade'] == 'São Paulo')]
```

4.  **Método .iloc\[\]**: O método `.iloc[]` permite acessar linhas e colunas do DataFrame com base em posições inteiras.
  
```python
# Filtrar linhas da posição 2 à 5
df_filtrado = df.iloc[2:6]
```

Essas são apenas algumas das maneiras de filtrar dados em um DataFrame no Pandas. A escolha do método de filtragem depende da complexidade do critério de filtragem e das preferências pessoais. É importante explorar e experimentar diferentes abordagens para encontrar a que melhor atenda às necessidades específicas de análise de dados.
