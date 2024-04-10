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

## Teste t de Student
O teste t de Student é usado para determinar se a média de duas amostras é significativamente diferente. A fórmula é:

$$
t = \frac{\bar{x}_1 - \bar{x}_2}{\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}
$$

## Regressão Linear Simples
A regressão linear simples é usada para modelar a relação entre duas variáveis. As fórmulas são:

Coeficiente de inclinação (b1):
$$
b1 = \frac{\sum_{i=1}^{n}(x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^{n}(x_i - \bar{x})^2}
$$

Interceptação (b0):
$$
b0 = \bar{y} - b1*\bar{x}
$$

Equação da linha de regressão:
$$
y = b0 + b1*x
$$

## Coeficiente de Correlação de Pearson
O coeficiente de correlação de Pearson mede a força e a direção da associação entre duas variáveis contínuas. A fórmula é:

$$
r = \frac{\sum_{i=1}^{n}(x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum_{i=1}^{n}(x_i - \bar{x})^2 \sum_{i=1}^{n}(y_i - \bar{y})^2}}
$$
