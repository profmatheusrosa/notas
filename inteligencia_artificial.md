# Sumário

1. [Tipos de Algoritmos de Machine Learning](#tipos-de-algoritmos-de-machine-learning)
   1. [Aprendizado Supervisionado](#aprendizado-supervisionado)
      1. [Classificação](#classificação)
      2. [Regressão](#regressão)
   2. [Aprendizado Não Supervisionado](#aprendizado-não-supervisionado)
      1. [Agrupamento (Clustering)](#agrupamento-clustering)
      2. [Redução de Dimensionalidade](#redução-de-dimensionalidade)
   3. [Aprendizado por Reforço](#aprendizado-por-reforço)
      1. [Aprendizado Baseado em Política](#aprendizado-baseado-em-política)
      2. [Aprendizado Baseado em Valor](#aprendizado-baseado-em-valor)
2. Exploração e Preparação de Dados
    1. Exploração de Dados (EDA)
       1. Análise Exploratória de Dados
       2. Detecção de Outliers
       3. Análise de Correlação
    2. Limpeza de Dados
       1. Tratamento de Dados Ausentes
       2. Detecção e Tratamento de Outliers
       3. Imputação de Dados
3. [Pré-processamento](#pré-processamento)
   1. [Transformação dos dados](#transformação-dos-dados)
      1. [Normalização/Escalonamento](#normalizaçãoescalonamento)
      2. [Discretização ou Binarização](#discretização-ou-binarização)
      3. [Codificação de Variáveis Categóricas](#codificação-de-variáveis-categóricas)
      4. [Criação de Variáveis Derivadas](#criação-de-variáveis-derivadas)
4. [Feature Engineering](#feature-engineering)
   1. Criação de Variáveis Derivadas
   2. Seleção de Variáveis
      1. Seleção Automática de Features (RFE, Lasso)
      2. Importância de Variáveis
   3. Codificação de Variáveis Categóricas
      1. One-Hot Encoding, Label Encoding, Target Encoding
6. [Divisão de dados](#divisão-de-dados)
7. [Métricas de Avaliação de Modelos](#métricas-de-avaliação-de-modelos)
   1. [Modelos de Classificação](#modelos-de-classificação)
      1. [Acurácia](#acurácia)
      2. [Precisão](#precisão)
      3. [Recall (Sensibilidade)](#recall-sensibilidade)
      4. [Especificidade](#especificidade)
      5. [F1-Score](#f1-score)
      6. [Curva ROC e Área sob a Curva (AUC)](#curva-roc-e-área-sob-a-curva-auc)
   2. [Modelos de Regressão](#modelos-de-regressão)
      1. [Erro Quadrático Médio (MSE)](#erro-quadrático-médio-mse)
      2. [Raiz do Erro Quadrático Médio (RMSE)](#raiz-do-erro-quadrático-médio-rmse)
      3. [Coeficiente de Determinação (R²)](#coeficiente-de-determinação-r²)
      4. [Erro Absoluto Médio (MAE)](#erro-absoluto-médio-mae)
      5. [Erro Percentual Absoluto Médio (MAPE)](#erro-percentual-absoluto-médio-mape)
      6. [R² Ajustado](#r²-ajustado)

# Tipos de Algoritmos de Machine Learning

## Aprendizado Supervisionado

### Classificação
- Regressão Logística
- Árvores de Decisão
- Random Forest
- Support Vector Machines (SVM)
- K-Nearest Neighbors (KNN)
- Naive Bayes
- Gradient Boosting Machines (GBM)
- Redes Neurais Convolucionais (CNN)
- Redes Neurais Recorrentes (RNN)

### Regressão
- Regressão Linear
- Regressão de Ridge e Lasso
- Redes Neurais Artificiais
- Gradient Boosting Machines (GBM)
- Máquinas de Vetores de Suporte para Regressão (SVR)
- ElasticNet
- LightGBM
- XGBoost

## Aprendizado Não Supervisionado

### Agrupamento (Clustering)
- K-Means
- Agrupamento Hierárquico
- DBSCAN
- Mean Shift
- Gaussian Mixture Models (GMM)
- OPTICS
- Birch
- Affinity Propagation

### Redução de Dimensionalidade
- Análise de Componentes Principais (PCA)
- t-Distributed Stochastic Neighbor Embedding (t-SNE)
- Autoencoders
- Linear Discriminant Analysis (LDA)
- Independent Component Analysis (ICA)
- Sparse PCA

## Aprendizado por Reforço

### Aprendizado Baseado em Política
- Q-Learning
- SARSA
- Deep Q-Networks (DQN)
- Advantage Actor-Critic (A2C)
- Policy Gradient Methods

### Aprendizado Baseado em Valor
- Algoritmo de Iteração de Valor
- Monte Carlo Control
- Método de Temporal Difference Learning (TD-Learning)
- Deep Deterministic Policy Gradient (DDPG)
- Twin Delayed DDPG (TD3)
- Proximal Policy Optimization (PPO)

# Pré-processamento
O pré-processamento envolve a preparação dos dados brutos para que possam ser utilizados efetivamente em análises, modelagem e visualização. Aqui estão os principais passos envolvidos no pré-processamento de dados:

## Transformação dos dados
### Normalização/Escalonamento:
- Min-Max Scaling: Ajusta os valores para um intervalo específico, como [0, 1].
  
$$
X_{scaled} = \frac{X - X_{min}}{X_{max} - X_{min}}
$$
  
- Z-Score Normalization: Converte os valores para terem média 0 e desvio padrão 1.
  
$$
Z = \frac{X - \mu}{\sigma}
$$

### Discretização ou Binarização
A discretização é uma técnica que envolve a transformação de variáveis contínuas em variáveis categóricas, dividindo seus valores em intervalos ou "bins". Ela é particularmente útil em situações onde as relações entre as variáveis podem ser melhor capturadas ou interpretadas em termos de categorias em vez de valores contínuos.
  
### Codificação de Variáveis Categóricas:
- One-Hot Encoding: Transforma variáveis categóricas em vetores binários.
- Label Encoding: Atribui números inteiros a categorias.

### Criação de Variáveis Derivadas: 
Geração de novas variáveis a partir das existentes, como extrair ano e mês de uma data.

# Métricas de Avaliação de Modelos

## Modelos de Classificação

### Acurácia
A acurácia é a proporção de previsões corretas feitas pelo modelo em relação ao total de previsões. A fórmula é:

$$
\text{Acurácia} = \frac{\text{Número de previsões corretas}}{\text{Número total de previsões}}
$$

### Precisão
A precisão é a proporção de previsões positivas que foram corretamente identificadas. A fórmula é:

$$
\text{Precisão} = \frac{\text{Verdadeiros Positivos}}{\text{Verdadeiros Positivos + Falsos Positivos}}
$$

### Recall (Sensibilidade)
O recall é a proporção de valores positivos reais que foram corretamente identificados. A fórmula é:

$$
\text{Recall} = \frac{\text{Verdadeiros Positivos}}{\text{Verdadeiros Positivos + Falsos Negativos}}
$$

### Especificidade
A especificidade é a proporção de verdadeiros negativos em relação ao total de valores reais negativos. É o complemento do recall e indica a habilidade do modelo de evitar falsos alarmes em negativos.

$$
\text{Especificidade} = \frac{\text{Verdadeiros Negativos}}{\text{Verdadeiros Negativos + Falsos Positivos}}
$$

### F1-Score
O F1-Score é a média harmônica entre precisão e recall. A fórmula é:

$$
\text{F1-Score} = 2*\frac{\text{Precisão * Recall}}{\text{Precisão + Recall}}
$$

### Curva ROC e Área sob a Curva (AUC)
A Curva ROC é uma representação gráfica da sensibilidade versus especificidade para um sistema de classificação binário e AUC é a área sob a curva ROC. Quanto maior a AUC, melhor o modelo.

## Modelos de Regressão

### Erro Quadrático Médio (MSE)
O MSE é a média dos quadrados dos erros. Quanto menor o MSE, melhor o modelo. A fórmula é:

$$
\text{MSE} = \frac{1}{n}\sum_{i=1}^{n}(y_i - \hat{y}_i)^2
$$

### Raiz do Erro Quadrático Médio (RMSE)
O RMSE é a raiz quadrada do MSE. É uma medida de desvio padrão dos erros de previsão. A fórmula é:

$$
\text{RMSE} = \sqrt{\frac{1}{n}\sum_{i=1}^{n}(y_i - \hat{y}_i)^2}
$$

### Coeficiente de Determinação (R²)
O R² é uma medida estatística que representa a proporção da variância para uma variável dependente que é explicada por uma variável independente ou variáveis em um modelo de regressão. A fórmula é:

$$
R² = 1 - \frac{\text{Soma dos quadrados dos resíduos}}{\text{Soma total dos quadrados}}
$$

### Erro Absoluto Médio (MAE)
O MAE é a média das diferenças absolutas entre as previsões e os valores reais. Ele fornece uma ideia de quão erradas estão nossas previsões.

$$
\text{MAE} = \frac{1}{n}\sum_{i=1}^{n}|y_i - \hat{y}_i|
$$

### Erro Percentual Absoluto Médio (MAPE)
O MAPE é a média das diferenças percentuais absolutas entre as previsões e os valores reais.

$$
\text{MAPE} = \frac{1}{n}\sum_{i=1}^{n}\left|\frac{y_i - \hat{y}_i}{y_i}\right|
$$

### R² Ajustado
O R² ajustado é uma versão modificada do R² que ajusta o número de preditores no modelo. É útil quando comparamos modelos com diferentes números de preditores.
