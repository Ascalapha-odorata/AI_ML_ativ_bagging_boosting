# Modelos Ensemble: Bagging, Boosting e Stacking

Este repositório contém um notebook Jupyter (Colab) focado na exploração de Modelos Ensemble em Machine Learning, especificamente as técnicas de Bagging, Boosting e Stacking.

## 📌 Objetivo

O principal objetivo deste projeto é demonstrar o funcionamento e a aplicação de diferentes estratégias de combinação de modelos preditivos, visando melhorar a performance, a generalização e a robustez das previsões em comparação a modelos individuais. O código utiliza a biblioteca `scikit-learn` em Python.

## 🚀 Tecnologias e Bibliotecas

*   Python 3
*   Google Colab
*   `scikit-learn` (Scikit-Learn)
*   Pandas (para manipulação de dados)
*   Vega Datasets (para o conjunto de dados de exemplo)

## 📁 Conteúdo do Notebook

O notebook `PUCSP_CS_AI_12_AI_ML_Baggin.ipynb` está dividido nas seguintes seções:

### 1. Introdução aos Ensemble Models
*   O que são métodos Ensemble e por que combinam múltiplos estimadores base.
*   Conceitos-chave: redução de variância e redução de viés.

### 2. Bagging (Bootstrap Aggregating)
*   **Conceito:** Treinamento de vários estimadores independentes em subconjuntos de dados gerados por amostragem com reposição (bootstrapping).
*   **Objetivo:** Reduzir a variância e evitar overfitting.
*   **Exemplos:** `RandomForestClassifier`, `BaggingRegressor`.
*   **Implementação:** Exemplo prático utilizando o dataset populacional do Vega, prevendo a população com base no ano, idade e sexo através de um `RandomForestRegressor`.
*   **Avaliação:** Análise do desempenho do modelo utilizando métricas como MAE (Erro Absoluto Médio), RMSE (Raiz do Erro Quadrático Médio), MAPE (Erro Percentual Absoluto Médio) e R².

### 3. Boosting
*   **Conceito:** Treinamento sequencial de estimadores, onde cada novo modelo foca em corrigir os erros dos modelos anteriores.
*   **Objetivo:** Reduzir o viés, combinando preditores "fracos" para formar um modelo forte.
*   **Exemplos:** `AdaBoostClassifier`, `GradientBoostingClassifier`.

### 4. Stacking (Generalização Empilhada)
*   **Conceito:** Combinação de previsões de modelos heterogêneos (diferentes tipos de algoritmos) utilizando um classificador final para a decisão.
*   **Treinamento:** Etapa 1 (treino dos estimadores base via *cross-validation*) e Etapa 2 (treino do estimador final usando as previsões da Etapa 1).

## 📊 Dataset Utilizado

A seção prática de Bagging utiliza o conjunto de dados `population` da biblioteca `vega_datasets`. O objetivo é prever a variável numérica `people` utilizando as variáveis independentes:
*   `year` (Ano)
*   `age` (Idade)
*   `sex` (Sexo)

O a seçãp de Boosting demonstra como transformar uma variável alvo contínua (número de pessoas) em um **problema de classificação binária** e, em seguida, como treinar e avaliar um modelo `GradientBoostingClassifier` usando o `scikit-learn`.

## 🏃 Como Executar

1.  Abra o notebook no Google Colab (ou no seu ambiente Jupyter local).
2.  Instale as bibliotecas necessárias, se não as tiver (ex: `pip install scikit-learn pandas vega_datasets`).
3.  Execute as células sequencialmente para ver as explicações teóricas, o código de treinamento do modelo e as métricas de avaliação.

## 🔗 Referências Úteis

*   [Scikit-Learn Ensemble Documentation](https://scikit-learn.org/stable/modules/ensemble.html)
*   [GeeksforGeeks: Bagging vs Boosting vs Stacking](https://www.geeksforgeeks.org/machine-learning/bagging-vs-boosting-vs-stacking/)
*   [GeeksforGeeks: Boosting in Machine Learning](https://www.geeksforgeeks.org/machine-learning/boosting-in-machine-learning/)
