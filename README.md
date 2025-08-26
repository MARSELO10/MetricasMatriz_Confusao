<img width="1000" height="447" alt="FlorIris" src="https://github.com/user-attachments/assets/9572cfa0-fe35-4214-84f4-6d477b0cc096" />

---

# 🟣🌹 Matrix Confusion - Métricas - Íris

[![Python](https://img.shields.io/badge/Python-3.12.6-blue.svg)](https://python.org)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen.svg)]()

---

## 📋 - Descrição 
Este projeto é uma tarefa dada aos estudantes do BairesDev - Machine Learning Training, um bootcamp da plataforma [DIO](https://www.dio.me/).

---

## 🎯 - Sobre o Projeto de Métricas de Matriz de Confusão

Este projeto implementa uma análise comparativa de modelos de aprendizado de máquina utilizando o conjunto de dados Iris.

Múltiplos algoritmos de classificação são treinados — Regressão Logística, Árvore de Decisão, Floresta Aleatória, KNN e SVM - para distinguir entre três espécies de flores: Setosa, Versicolor e Virginica.

Para cada modelo, são calculadas as principais métricas de classificação: Acurácia, Precisão, Recall, Especificidade e F-score. Os resultados são comparados por meio de tabelas e visualizações, incluindo gráficos de barras e matrizes de confusão, para melhor compreender o desempenho de cada abordagem.

O projeto também inclui uma classe ClassificationMetrics reutilizável, que pode calcular métricas de qualquer matriz de confusão, tornando-a flexível para diferentes conjuntos de dados e problemas binários/multiclasse.

---

## 🚀 Funcionalidades

* ✅Carregamento automático do dataset Iris
* ✅Divisão do dataset em treino e teste
* ✅Implementação da classe ClassificationMetrics para cálculo de métricas
* ✅Função auxiliar para gerar métricas e matriz de confusão
* ✅Treinamento e avaliação de múltiplos classificadores
* ✅Comparação dos resultados em tabela
* ✅Visualização gráfica de métricas comparativas em gráfico de barras
* ✅Geração de matrizes de confusão individuais para cada modelo
* ✅Suporte a análise binária e multiclasse

---

## 📊 Métricas Implementadas

| Métrica | Fórmula | Descrição |
|---------|---------|-----------|
| **Sensibilidade** | `VP / (VP + FN)` | Capacidade de identificar positivos |
| **Especificidade** | `VN / (FP + VN)` | Capacidade de identificar negativos |
| **Acurácia** | `(VP + VN) / N` | Proporção total de acertos |
| **Precisão** | `VP / (VP + FP)` | Confiabilidade das predições positivas |
| **F-score** | `2 × (P × S) / (P + S)` | Equilíbrio entre precisão e sensibilidade |

**Legenda:**
- `VP`: Verdadeiros Positivos
- `VN`: Verdadeiros Negativos
- `FP`: Falsos Positivos
- `FN`: Falsos Negativos
- `N`: Total de elementos
- `P`: Precisão
- `S`: Sensibilidade

---

## 📊 Classificadores Implementados

* `Regressão Logística`
* `Árvore de Decisão`
* `Floresta Aleatória`
* `KNN`
* `SVM`

---

## 🛠️ Tecnologias Utilizadas

* Python 
* Scikit-learn (datasets, model_selection, linear_model, tree, ensemble, neighbors, svm, metrics)
* Pandas (armazenamento e comparação de métricas em DataFrame)
* Matplotlib (visualização de métricas em gráficos)
* Seaborn (heatmap das matrizes de confusão)
* Jupyter Notebook / Google Colab (ambiente de execução e experimentação)

---

## 📁 Instrução de Uso Google Collab

1. **Todas as instruções estão documentadas no próprio arquivo do Colab.**

2. **Execução passo a passo: Execute as células em ordem numérica (1 → 8).**

   **O dataset Iris será carregado automaticamente.**

   **O conjunto de dados será dividido em treino (70%) e teste (30%).**

   **- Vários modelos de classificação serão treinados e avaliados.**

  <img width="193" height="159" alt="image" src="https://github.com/user-attachments/assets/787c21a3-27bf-45e8-824f-c7e16c1bbe46" />

  Accuracy de cada modelo

   **- As métricas e as matrizes de confusão serão exibidas automaticamente.**

   <img width="353" height="319" alt="image" src="https://github.com/user-attachments/assets/de20ea93-1aaa-4a84-9163-d3c80601afc0" />

   Nesta Matriz de confusão podemos ver na Vertical os valores atuais e na Horizontal os valores preditos, Com isso podemos ver oque o modelo está escolhendo.

   Por exemplo na Setosa era 15 valores e acertou todos, no Versicolor acertou 14 mas errou 2 confundindo com Virginica, no Virginica acertou 13 mas errou 1 confundindo com Versicolor. 

---

## 📁 Estrutura do Projeto

```
projeto
├── ClassificationMetrics (class)     # Classe para calcular métricas de avaliação
│   ├── __init__()                     # Inicializa TP, TN, FP, FN
│   ├── recall()                       # Calcula recall
│   ├── specificity()                  # Calcula especificidade
│   ├── accuracy()                      # Calcula acurácia
│   ├── precision()                     # Calcula precisão
│   ├── f_score()                       # Calcula F-score
│   └── calculate_all()                 # Retorna todas as métricas em um dicionário
│
├── calculate_metrics()                 # Função auxiliar para gerar métricas e matriz de confusão
├── load_and_split_data()               # Carrega dataset Iris e divide em treino/teste
├── train_models()                      # Treina múltiplos modelos de classificação
├── compare_results()                   # Cria tabela comparativa de métricas
├── plot_metrics()                      # Gera gráficos de comparação de métricas
├── plot_confusion_matrices()           # Gera heatmaps das matrizes de confusão
└── main (sequência do script)          # Chama funções na ordem correta para execução completa

```

---

## 📊 Aplicações em Machine Learning

* Classificação de flores em múltiplas classes (3 tipos de Iris: setosa, versicolor e virginica)

* Comparação de diferentes modelos de classificação (Regressão Logística, Árvore de Decisão, Random Forest, KNN, SVM)

* Extração de métricas de desempenho (Accuracy, Recall, Specificity, Precision, F-score)

* Treinamento supervisionado com rótulos fornecidos pelo dataset

* Avaliação de desempenho em conjunto de teste e análise via matrizes de confusão

* Aplicação prática em problemas de classificação multiclasse e validação de modelos de machine learning

---

## 🤝 Patrocinadores ou Afins

Estes são os *links* das empresas/projetos ligados a este trabalho:

- [DIO](https://www.dio.me/): plataforma de cursos e bootcamps online.
- [Baires Dev](https://www.bairesdev.com/): A BairesDev é uma empresa multinacional americana de outsourcing de TI e desenvolvimento de software
- [Scikit-Learn](https://scikit-learn.org/stable/): Biblioteca de Python para machine learning, usada para carregar o dataset Iris, treinar e avaliar modelos de classificação.
- [Pandas](https://pandas.pydata.org/): Biblioteca para manipulação e análise de dados em DataFrames.
- [Matplotlib](https://matplotlib.org/): Biblioteca para criação de gráficos de métricas e comparação de modelos.
- [Seaborn](https://seaborn.pydata.org/): Biblioteca para visualização de matrizes de confusão em heatmaps.
- [Python](https://www.python.org/): Linguagem de programação utilizada em todo o projeto.
- [Google Collab](https://colab.google/): O Google Colab (ou Colaboratory) é um ambiente de desenvolvimento integrado (IDE) gratuito e baseado em nuvem que permite escrever e executar código Python diretamente no navegador, sem necessidade de instalação ou configuração.

---

# Contribuição

Contribuições são bem-vindas!\
Se você encontrar algum problema ou tiver sugestões de melhorias, por favor abra uma **issue** ou envie um **pull request** para o repositório.\
Ao contribuir para este projeto, siga as convenções de commits e envie suas alterações em um **branch** ou **file** separado.\
Saiba mais sobre o código de conduta acessando o link: [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

---

# Licença

Este repositório possui licença [MIT](https://github.com/MARSELO10/MetricasMatriz_Confusao)

