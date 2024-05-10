# Sumário

1. [Notações](#notações)
    - [População](#população)
    - [Amostra](#amostra)
2. [Estatística Descritiva](#dataframe)

# Notações
### População:

*   **μ (mi)**: Média populacional.
*   **σ (sigma)**: Desvio padrão populacional.
*   **N**: Tamanho da população.
*   **p**: Proporção populacional.
*   **Σ (sigma)**: Soma (somatório) dos valores de uma população.

### Amostra:

*   **x̄ (x-barra)**: Média da amostra.
*   **s**: Desvio padrão da amostra.
*   **n**: Tamanho da amostra.
*   **p̂ (p-chapéu)**: Estimativa da proporção populacional com base na amostra.
*   **Σ (sigma)**: Soma (somatório) dos valores de uma amostra.

### Outros Símbolos:

*   **α (alfa)**: Nível de significância (probabilidade de cometer um erro do Tipo I).
*   **β (beta)**: Probabilidade de cometer um erro do Tipo II.
*   **H₀**: Hipótese nula.
*   **H₁ ou Hₐ**: Hipótese alternativa.
*   **Z**: Estatística de teste para distribuição normal.
*   **t**: Estatística de teste para distribuição t de Student.
*   **χ² (qui-quadrado)**: Estatística de teste para distribuição qui-quadrado.
*   **F**: Estatística de teste para distribuição F de Fisher.
*   **R²**: Coeficiente de determinação.

# Fórmulas Estatísticas Principais

## Média
A média de um conjunto de números é a soma de todos os números dividida pelo número total de números. A fórmula é:

$$
\bar{x} = \frac{1}{n}\sum_{i=1}^{n}x_i
$$

## Média da Amostra
A média de uma amostra é a soma de todos os números na amostra dividida pelo número total de números na amostra. A fórmula é:

$$
\bar{x} = \frac{1}{n}\sum_{i=1}^{n}x_i
$$

## Mediana
A mediana é o valor do meio em um conjunto de dados quando os dados são organizados em ordem. 

## Moda
A moda é o valor que ocorre com mais frequência em um conjunto de dados.

## Variância
A variância é uma medida de dispersão que mostra o quão longe os números estão da média. A fórmula é:

$$
\sigma^2 = \frac{1}{n}\sum_{i=1}^{n}(x_i - \bar{x})^2
$$

## Variância da Amostra
A variância de uma amostra é uma medida de dispersão que mostra o quão longe os números na amostra estão da média da amostra. A fórmula é:

$$
s^2 = \frac{1}{n-1}\sum_{i=1}^{n}(x_i - \bar{x})^2
$$

## Desvio Padrão
O desvio padrão é a raiz quadrada da variância. A fórmula é:

$$
\sigma = \sqrt{\frac{1}{n}\sum_{i=1}^{n}(x_i - \bar{x})^2}
$$

## Desvio Padrão da Amostra
O desvio padrão de uma amostra é a raiz quadrada da variância da amostra. A fórmula é:

$$
s = \sqrt{\frac{1}{n-1}\sum_{i=1}^{n}(x_i - \bar{x})^2}
$$

## Escore Z

O escore Z é uma medida estatística que descreve a posição de uma pontuação bruta em relação à média da população. Ele é usado para entender se uma determinada pontuação é típica para uma determinada distribuição ou se é atípica. O escore Z também pode ser usado para comparar pontuações de diferentes distribuições.

Em uma distribuição normal, um escore Z de 0 indica que a pontuação é igual à média da população. Um escore Z de 1.0 indica uma pontuação que é um desvio padrão acima da média. Um escore Z de -1.0 indica uma pontuação que é um desvio padrão abaixo da média.

A fórmula para calcular o escore Z é:

$$
Z = \frac{X - \mu}{\sigma}
$$

Onde:
- `Z` é o escore Z (número de desvios padrões),
- `X` é o valor que você está tentando encontrar o número de desvios padrões para,
- `μ` é a média da população, e
- `σ` é o desvio padrão da população.

# Distribuição Binomial

A distribuição binomial é uma distribuição de probabilidade discreta que descreve o número de sucessos em uma sequência de n tentativas independentes de um experimento binomial (um experimento com exatamente dois resultados possíveis, sucesso e fracasso). 

A fórmula para a probabilidade binomial é:

$$
P(X=k) = C(n, k) * (p^k) * ((1-p)^(n-k))
$$

Onde:
- `P(X=k)` é a probabilidade de `k` sucessos em `n` tentativas,
- `C(n, k)` é o número de combinações de `n` itens tomados `k` a `k`,
- `p` é a probabilidade de sucesso em uma única tentativa, e
- `(1-p)` é a probabilidade de fracasso (ou seja, 1 menos a probabilidade de sucesso).

# Intervalo de Confiança para a Média

Um intervalo de confiança para a média é um intervalo de valores que é provável que contenha a verdadeira média da população com um certo nível de confiança. É uma maneira de quantificar a incerteza sobre a estimativa de uma média da população com base em dados de amostra.

A fórmula para um intervalo de confiança de 95% para a média é:

$$
CI = \bar{x} ± (1.96 * (s/√n))
$$

Onde:
- `CI` é o intervalo de confiança,
- `\bar{x}` é a média da amostra,
- `s` é o desvio padrão da amostra, e
- `n` é o tamanho da amostra.

O número 1.96 é o valor Z para um intervalo de confiança de 95%. Para outros níveis de confiança, você usaria o valor Z correspondente.


## Teste t de Student

O Teste t de Student é um método estatístico que é usado para determinar se há uma diferença significativa entre as médias de dois grupos. Este teste é aplicado quando os dados são normalmente distribuídos, mas o tamanho da amostra é pequeno, e o desvio padrão da população é desconhecido.

O Teste t de Student é frequentemente usado em experimentos científicos e pesquisas médicas para comparar dois grupos diferentes. Por exemplo, pode ser usado para comparar a eficácia de dois medicamentos diferentes.

A fórmula para o Teste t de Student é:

$$
t = \frac{\bar{x}_1 - \bar{x}_2}{\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}
$$

Onde:
- `t` é o valor t,
- `x̄1` e `x̄2` são as médias das duas amostras,
- `s1` e `s2` são os desvios padrão das duas amostras, e
- `n1` e `n2` são os tamanhos das duas amostras.

Um valor t grande (ou pequeno) indica que as médias dos dois grupos são significativamente diferentes, enquanto um valor t próximo de zero indica que as médias dos dois grupos são semelhantes.


## Regressão Linear

A regressão linear é uma abordagem estatística para modelar a relação entre uma variável dependente e uma ou mais variáveis independentes. A regressão linear simples, que usa apenas uma variável independente, é a forma mais básica de regressão linear. Ela é útil para prever resultados com base em novos dados de entrada.

A fórmula para a regressão linear simples é:

$$
y = b0 + b1*x
$$

Onde:
- `y` é a variável dependente (a variável que estamos tentando prever ou estimar),
- `x` é a variável independente (a variável que estamos usando para fazer a previsão),
- `b0` é a interceptação do eixo y (o valor de `y` quando `x` é 0), e
- `b1` é o coeficiente de inclinação (a mudança em `y` para uma mudança de uma unidade em `x`).

Os coeficientes `b0` e `b1` são determinados usando o método dos mínimos quadrados, que minimiza a soma dos quadrados das diferenças entre os valores observados e previstos de `y`.

## Coeficiente de Inclinação (b1)

O coeficiente de inclinação, também conhecido como coeficiente de regressão, é uma medida da inclinação da linha de regressão. Ele representa a mudança na variável dependente `y` para uma mudança de uma unidade na variável independente `x`. Em outras palavras, o coeficiente de inclinação é a quantidade que `y` aumenta (ou diminui) para cada aumento de uma unidade em `x`.

A fórmula para calcular o coeficiente de inclinação é:

$$
b1 = \frac{\sum_{i=1}^{n}(x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^{n}(x_i - \bar{x})^2}
$$

## Interceptação (b0)

A interceptação, também conhecida como constante de regressão, é o valor da variável dependente `y` quando a variável independente `x` é 0. Em outras palavras, a interceptação é o ponto onde a linha de regressão cruza o eixo y.

A fórmula para calcular a interceptação é:

$$
b0 = \bar{y} - b1*\bar{x}
$$


## Coeficiente de Correlação de Pearson
O coeficiente de correlação de Pearson mede a força e a direção da associação entre duas variáveis contínuas. A fórmula é:

$$
r = \frac{\sum_{i=1}^{n}(x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum_{i=1}^{n}(x_i - \bar{x})^2 \sum_{i=1}^{n}(y_i - \bar{y})^2}}
$$
